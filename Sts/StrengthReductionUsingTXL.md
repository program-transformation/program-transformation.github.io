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
    Page](http://www.program-transformation.org/edit/Sts/StrengthReductionUsingTXL?t=1536827754)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/StrengthReductionUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/StrengthReductionUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/StrengthReductionUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/StrengthReductionUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/StrengthReductionUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/StrengthReductionUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/StrengthReductionUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/StrengthReductionUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Strength Reduction Using TXL {#strength-reduction-using-txl .twikiTopicTitle}
============================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#3.3,
Strength reduction, recognize opportunities to reduce multiplication by
an iterator to iterative addition.

Thie simple example demonstrates the basics of strength reduction
optimizations using TXL. Strength reduction is normally a part of
optimization for high performance numerical applications on modest
processors such as ARM.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 03 Jan 2008

*File \"TILstrengthred.Txl\"*

    % Basic strength reduction in TIL programs using TXL
    % Jim Cordy, January 2008

    % Given a TIL program, look for opportunities to leverage loops to
    % reduce multiplications to additions (strength reduction).

    % This program could be combined with other optimization rules
    % to form a comprehensive source optimizer.


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
            P [strengthReduceMultiplications]
    end function


    % Strength reduction in for loops - recognize expresssions of the form
    % "x+*i" in for loops iterating "i", and reduce to addition.

    rule strengthReduceMultiplications
        % Find a for statement
        replace [repeat statement]
            'for I [id] := Low [expression] 'to High [expression] 'do
                InnerStatements [repeat statement]
            'end
            Rest [repeat statement]

        % That has an expression multiplied by the iterator 
        % (for simplicity we assume a simple variable reference in this example)
        deconstruct * [term] InnerStatements
            J [id] * I

        % Where the expression is not changed in the loop
        deconstruct not * [statement] InnerStatements
            J := _ [expression] ;
        deconstruct not * [statement] InnerStatements
            'for J := _ [expression] 'to _ [expression] 'do
                _ [repeat statement]
            'end

        % Construct a unique new variable name
        construct JI [id]
            J [_ I] [!]

        % And convert to additive form
        by
            var JI;
            '// can be constant-folded later
            JI := ((Low)-1) * J; 
            'for I := Low 'to High 'do
                JI := JI + J;
                InnerStatements [replaceMultiply J I JI] 
            'end
            Rest 
    end rule


    rule replaceMultiply J [id] I [id] JI [id]
        replace [term]
            J * I
        by
            JI
    end rule

*Example run:* \"strength.til\" is the simple TIL multiplies example
program that happens to have an embedded opportunity for strength
reduction.

    <linux> cat strength.til
    // Test of strength reduction
    for i := 1 to 9 do
        for j := 1 to 10 do
            write i*j;
        end 
    end

    <linux> txl strength.til TILstrengthred.Txl
    TXL v10.5 (11.12.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILstrengthred.Txl ... 
    Parsing strength.til ...
    Transforming ...

    // Test of strength reduction
    for i := 1 to 9 do
        var i_j1;
        // can be constant-folded later
        i_j1 := ((1) - 1) * i;
        for j := 1 to 10 do
            i_j1 := i_j1 + i;
            write i_j1;
        end
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
