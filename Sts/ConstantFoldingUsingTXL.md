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
    Page](http://www.program-transformation.org/edit/Sts/ConstantFoldingUsingTXL?t=1536827755)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/ConstantFoldingUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/ConstantFoldingUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/ConstantFoldingUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/ConstantFoldingUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/ConstantFoldingUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/ConstantFoldingUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/ConstantFoldingUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/ConstantFoldingUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Constant Folding Using TXL {#constant-folding-using-txl .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#3.4,
Constant folding, recognize and resolve opportunities to fold constant
expressions.

Thie simple example demonstrates constant propagation and expression
folding using TXL.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 03 Jan 2008

*File \"TILconst.Txl\"*

    % Constant propagation and folding for TIL
    % Jim Cordy, January 2008

    % Given a TIL program, recognize constant assignments to variables,
    % and replace references to the variable with the constant (constant propagation),
    % then recognize and compute constant expressions (constant folding).

    % This program could be combined with other optimization rules such as
    % code motion and redundant variable elimination to further optimize the result.


    % Begin with the TIL base grammar, using precedence
    #define PRIORITY
    include "TIL.Grm"

    % Preserve comments in this transformation
    #pragma -comment

    redefine statement
            ...
        |   [comment] [NL]
    end redefine


    % Main function - just apply stages of the transformation

    function main
        replace [program]
            P [program]
        by
            P [propagateConstants]
              [foldConstantExpressions]
    end function


    % Constant propagation - find each constant assignment to a variable, 
    % and if it is not assigned again then replace references with the constant

    rule propagateConstants
        replace [repeat statement]
            Var [id] := Const [literal] ;
            Rest [repeat statement]
        deconstruct not * [statement] Rest
            Var := _ [expression] ;
        deconstruct * [primary] Rest
            Var
        by
            Var := Const;
            Rest [replaceExpn Var Const]
    end rule

    rule replaceExpn Var [id] Const [literal]
        replace [primary]
            Var
        by
            Const
    end rule


    % Constant folding - find and evaluate constant expressions

    rule foldConstantExpressions
        replace [expression]
            E [expression]

        construct NewE [expression]
            E % Generic folding of pure constant expressions
              [resolveAddition] 
              [resolveSubtraction] 
              [resolveMultiplication] 
              [resolveDivision] 

              % Other special cases involving constants (examples only, could be others)
              [resolveAdd0]
              [resolveSubtract0]
              [resolveMultiply1Right]
              [resolveMultiply1Left]
              [resolveParentheses]

        % Continue until we don't find anything to fold
        deconstruct not NewE
            E
        by
            NewE
    end rule

    rule resolveAddition
        replace [expression]
            N1 [integernumber] + N2 [integernumber]
        by
            N1 [+ N2]
    end rule

    rule resolveSubtraction
        replace [expression]
            N1 [integernumber] - N2 [integernumber]
        by
            N1 [- N2]
    end rule 

    rule resolveMultiplication
        replace [term]
            N1 [integernumber] * N2 [integernumber]
        by
            N1 [* N2]
    end rule 

    rule resolveDivision
        replace [term]
            N1 [integernumber] / N2 [integernumber]
        by
            N1 [/ N2]
    end rule

    rule resolveParentheses
        replace [primary]
            ( N [integernumber] )
        by
            N
    end rule

    rule resolveAdd0
        replace [expression]
            P [primary] + 0
        by
            P
    end rule

    rule resolveSubtract0
        replace [expression]
            P [primary] - 0
        by
            P
    end rule

    rule resolveMultiply1Right
        replace [expression]
            P [primary] * 1
        by
            P
    end rule

    rule resolveMultiply1Left
        replace [expression]
            1 * P [primary]
        by
            P
    end rule

*Example run:* \"const.til\" is a meaningless little program with lots
of opportunities for constant propagation and folding.

    <linux> cat const.til
    // Silly meaningless example with opportunities to fold constants
    var x; var y; var z; var a; var b; var c;
    var d; var e; var j; var k; var m; var n; var r;
    y := 1;
    z := 2;
    while 1 do
        x := y + z;
        a := 3;
        z := 5;
        j := 0;
        while j != 100 do
            r := 99;
            d := 7;
            k := a + z;
            b := j * z;
            d := (y + z) * d;
            e := (x + z) * r;
            j := j + 1;
        end 
        // This one is constant for sure!
        c := a + y;
        m := y * b;
        n := r * y;
    end 

    <linux> txl const.til TILconst.Txl
    TXL v10.5 (11.12.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILconst.Txl ... 
    Parsing const.til ...
    Transforming ...

    // Silly meaningless example with opportunities to fold constants
    var x;
    var y;
    var z;
    var a;
    var b;
    var c;
    var d;
    var e;
    var j;
    var k;
    var m;
    var n;
    var r;
    y := 1;
    z := 2;
    while 1 do
        x := 1 + z;
        a := 3;
        z := 5;
        j := 0;
        while j != 100 do
            r := 99;
            d := 7;
            k := 8;
            b := j * 5;
            d := 6 * d;
            e := (x + 5) * 99;
            j := j + 1;
        end
        // This one is constant for sure!
        c := 4;
        m := b;
        n := r;
    end
    <linux> 

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 03 Jan 2008\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
