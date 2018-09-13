::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[Home](WebHome){.twikiLink}**\
[STS\'08](STS08){.twikiLink}\
[STS\'06](http://www.program-transformation.org/Sts/STS06){.twikiLink}\
[STS\'04](STS04){.twikiLink}\
[StsBench](StsBench){.twikiLink}\
\
**[News](WebNews){.twikiLink}**\
[Recent Changes](WebChanges){.twikiLink}\
[Mailinglist](MailingList){.twikiLink}\
\
[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Sts/Declarations-to-LocalUsingTXL?t=1536827758)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/Declarations-to-LocalUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/Declarations-to-LocalUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/Declarations-to-LocalUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/Declarations-to-LocalUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/Declarations-to-LocalUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/Declarations-to-LocalUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/Declarations-to-LocalUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
:::
:::

::: {.flexMenu onmouseover="return showMenu(event, 102);" onmouseout="return hideMenu(event, 102);"}
Web

::: {#flexMenuContent102 .flexMenuContent}
-   [Recent Changes](WebChanges){.twikiLink}
-   [Notify Service](WebNotify){.twikiLink}
-   [News](WebNews){.twikiLink}

<!-- -->

-   [Page Index](WebIndex){.twikiLink}
-   [Search](WebSearch){.twikiLink}

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/Declarations-to-LocalUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
:::
:::

::: {.flexMenu onmouseover="return showMenu(event, 103);" onmouseout="return hideMenu(event, 103);"}
Wiki

::: {#flexMenuContent103 .flexMenuContent}
-   [About
    TWiki](http://www.program-transformation.org/view/TWiki/WebHome)
-   [Text
    Formatting](http://www.program-transformation.org/view/TWiki/TextFormattingRules)

<!-- -->

-   [Registration](http://www.program-transformation.org/view/TWiki/TWikiRegistration)
-   [Change
    Password](http://www.program-transformation.org/view/TWiki/ChangePassword)
-   [Reset
    Password](http://www.program-transformation.org/view/TWiki/ResetPassword)

<!-- -->

-   [Users](http://www.program-transformation.org/view/Main/TWikiUsers)
-   [Groups](http://www.program-transformation.org/view/Main/TWikiGroups)
:::
:::
:::
:::

::: {.twikiTopic}
Declarations-to-LocalUsingTXL {#declarations-to-localusingtxl .twikiTopicTitle}
=============================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#2.4,
Declarations-to-local, move all declarations to their most local
location.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 02 Nov 2005

*File \"TILtolocal.Txl\"*

    % TXL transformation to move all declarations in a TIL program to their most local location

    % Jim Cordy, October 2005

    % Based on the TIL base grammar
    include "TIL.Grm"

    % Preserve comments, we're probably going to maintain the result
    include "TILCommentOverrides.Grm"

    % Transformation to move all declarations to their most local location -
    % immediately before their first use, in the innermost block they can be.
    % It is done as two rules - one that moves declarations across statements
    % that do not depend on them, and one that moves declarations inside statements
    % they are not used outside of.

    rule main
        % Since this rule's pattern matches its result, it has no natural termination point
        replace [program]
            Program [program]

        % We therefore add an explicit fixed-point guard - after each application 
        % of the two base transformations, we check to see that something more was actually done
        construct NewProgram [program]
                Program [immediatizeDeclarations]
                    [localizeDeclarations]
        deconstruct not NewProgram
                Program
        by
            NewProgram 
    end rule

    rule immediatizeDeclarations
        % Move all declarations past statements that don't depend on them
        % This rule uses a one-pass traversal ($) since the case of two declarations in a row
        % has no natural fixed point for this rule
        replace $ [statement*]
            'var V [id];
            Statement [statement]
            MoreStatements [statement*]

        % We can move the declaration past a statement if the statement does
        % not refer to the declared variable
        deconstruct not * [id] Statement
                V
        by
            Statement 
            'var V;
            MoreStatements
    end rule

    rule localizeDeclarations
        % Move any declarations outside a structured statement inside it if
        % the statements following it do not depend on the declared variable
        % Again, use a one pass ($) traversal
        replace $ [statement*]
            Declaration [declaration]
            CompoundStatement [statement]
            MoreStatements [statement*]

        % Check that it is some kind of compound statement (one with a statement list inside)
        deconstruct * [statement*] CompoundStatement
                _ [statement*]

        % Check that the following statements don't depend on the declaration
        deconstruct * [id] Declaration
                V [id]
        deconstruct not * [id] MoreStatements
                V

        % Alright, then maybe we can move it in.  This transformation uses the natural
        % example-base style of TXL, and thus does each kind of compound statement separately
        % Another solution might use agile parsing to abstract similar cases into one
        by
            CompoundStatement [injectDeclarationWhile Declaration] 
                              [injectDeclarationFor Declaration]
                              [injectDeclarationIfThen Declaration]
                              [injectDeclarationIfElse Declaration]
            MoreStatements 
    end rule

    function injectDeclarationWhile Declaration [declaration]
        % Note that there is no legal way that the while Expn can depend on the declaration,
        % since there are no assignments between the declaration and the Expn
        replace [statement]
                'while Expn [expression] 'do
                Statements [statement*]
            'end
        by
                'while Expn 'do
                Declaration
                Statements 
            'end
    end function

    function injectDeclarationFor Declaration [declaration]
        % Note that there is no legal way that the while Expn can depend on the declaration,
        % since there are no assignments between the declaration and the Expn
        replace [statement]
                'for Id [id] := Expn1 [expression] 'to Expn2 [expression] 'do
                Statements [statement*]
            'end
        by
                'for Id := Expn1 'to Expn2 'do
                Declaration
                Statements 
            'end
    end function

    function injectDeclarationIfThen Declaration [declaration]
        % Note that there is no legal way that the if Expn can depend on the declaration,
        % since there are no assignments between the declaration and the Expn
        replace [statement]
            'if Expn [expression] 'then
                ThenStatements [statement*]
             OptionalElse [opt else_statement]
            'end
        deconstruct Declaration
                'var V [id];
        deconstruct not * [id] OptionalElse
                V
        by
            'if Expn 'then
                Declaration
                ThenStatements 
             OptionalElse
            'end
    end function

    function injectDeclarationIfElse Declaration [declaration]
        % Note that there is no legal way that the if Expn can depend on the declaration,
        % since there are no assignments between the declaration and the Expn
        replace [statement]
            'if Expn [expression] 'then
                ThenStatements [statement*]
            'else
                ElseStatements [statement*]
            'end
        deconstruct Declaration
                'var V [id];
        deconstruct not * [id] ThenStatements
                V
        by
            'if Expn 'then
                ThenStatements 
            'else
                Declaration
                ElseStatements 
            'end
    end function

*Example run:* \"gvareg.til\" is a meaningless little program with lots
of data dependencies and all global declarations for demonstration
purposes.

    <linux> cat gvareg.til
    // Meaningless example TIL program with lots of data dependencies
    var d;
    var r;
    var y;
    var z;
    var x;
    var a;
    var j;
    var b;
    var k;
    var e;
    var c;
    var m;
    var n;
    d := 17;
    r := 5;
    read y;
    read z;
    while y != 0 do
        x := y + z;
        a := 3;
        j := 1;
        while j != 100 do
            k := a + z;
            b := j * z;
            d := (y + z) * d;
            e := (x + z) * r;
            j := j + 1;
        end
        c := a + y;
        m := y * b;
        n := r * y;
        write n;
        y := y - 1;
    end
    <linux> txl gvareg.til TILtolocal.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILtolocal.Txl ... 
    Parsing gvareg.til ...
    Transforming ...
    // Meaningless example TIL program with lots of data dependencies
    var d;
    d := 17;
    var r;
    r := 5;
    var y;
    read y;
    var z;
    read z;
    while y != 0 do
        var x;
        x := y + z;
        var a;
        a := 3;
        var j;
        j := 1;
        var b;
        while j != 100 do
            var k;
            k := a + z;
            b := j * z;
            d := (y + z) * d;
            var e;
            e := (x + z) * r;
            j := j + 1;
        end
        var c;
        c := a + y;
        var m;
        m := y * b;
        var n;
        n := r * y;
        write n;
        y := y - 1;
    end
    <linux> 

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
