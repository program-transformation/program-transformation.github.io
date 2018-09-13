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
    Page](http://www.program-transformation.org/edit/Sts/GotoEliminationUsingTXL?t=1536827754)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/GotoEliminationUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/GotoEliminationUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/GotoEliminationUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/GotoEliminationUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Sts/GotoEliminationUsingTXL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/GotoEliminationUsingTXL?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sts/GotoEliminationUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/GotoEliminationUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/GotoEliminationUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sts/GotoEliminationUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
Goto Elimination Using TXL {#goto-elimination-using-txl .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#2.5, Goto
elimination, recognize and transform while-equivalent goto structures.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 31 Dec 2007

*File \"TILgotoelim.Txl\"*

    % Goto elimination in TIL programs
    % Jim Cordy, January 2008

    % Given a TIL program in an extended dialect that includes labelled statements 
    % and goto statements, recognize and resolve while-equivalent goto structures.

    % Begin with the TIL base grammar
    include "TIL.Grm"

    % Preserve comments in this transformation
    #pragma -comment

    % Add labels and goto statements to TIL 
    redefine statement
            ...
        |        [labelled_statement]
        |        [goto_statement]
        |        [null_statement]
        |        [comment_statement]
    end redefine

    define labelled_statement
            [label] ': [statement] 
    end define

    define goto_statement
            'goto [label] ';  [NL]
    end define

    % Allow for trailing labels
    define null_statement
            [NL]
    end define

    define comment_statement
            [comment]  [NL]
    end define

    define label 
            [id]
    end define


    % Main program - just applies the rules for cases we know how to transform 

    function main
        replace [program]
            P [program]
        by
            P [transformForwardWhile]
              [transformBackwardWhile]
    end function


    % Case 1 - structures of the form
    %        loop:
    %            if Cond then goto endloop; end
    %            LoopStatements
    %            goto loop;
    %        endloop:
    %            TrailingStatements

    rule transformForwardWhile
        replace [repeat statement]
            L0 [label] ': 
                'if X [expression] Op [op] Y [expression] 'then
                    'goto L1 [label] ';
                'end
            Rest [repeat statement]
        skipping [statement]
        deconstruct * Rest
            'goto L0 ';
            L1 ':
                Follow [statement]
            FinalRest [repeat statement]
        construct NonRest [repeat statement]
            Rest [truncateGoto L0 L1]
        by
            'while X Op [invertOp] Y 'do
                NonRest
            'end
            Follow
            FinalRest
    end rule

    function truncateGoto L0 [label] L1 [label]
        replace * [repeat statement]
            'goto L0 ';
            L1 ':
                Follow [statement]
            FinalRest [repeat statement]
        by
            % nothing
    end function

    % Since TIL doesn't have a not operator, we need to invert comparisons
    function invertOp
        construct Ops [repeat op]
            '= '!=
        construct InvertOps [repeat op]
            '!= '=
        replace [op]
            Op [op]
        by
            Op [replaceOriginalOp Op each Ops InvertOps]
    end function

    function replaceOriginalOp OriginalOp [op] PatternOp [op] ReplacementOp [op]
        replace [op]
            OriginalOp 
        by
            OriginalOp [$ PatternOp ReplacementOp]
    end function


    % Case 2 - structures of the form
    %        loop:
    %            LoopStatements
    %            if Cond then goto loop; end
    %        TrailingStatements

    rule transformBackwardWhile
        replace [repeat statement]
            L0 [label] ': 
                First [statement]
            Rest [repeat statement]
        skipping [statement]
        deconstruct * Rest
            'if C [expression] 'then
                'goto L0 ';
            'end
            FinalRest [repeat statement]
        construct NonRest [repeat statement]
            Rest [truncateIfGoto L0]
        construct WhileStatement [repeat statement]
            'while C 'do
                First
                NonRest
            'end
        by
            First
            NonRest [. WhileStatement]
                    [. FinalRest]
    end rule

    function truncateIfGoto L0 [label]
        skipping [statement]
        replace * [repeat statement]
            'if C [expression] 'then
                'goto L0 ';
            'end
            FinalRest [repeat statement]
        by
            % nothing
    end function

*Example run:* \"gotofactors.til\" is a goto-based version of the
factors.til example program.

    <linux> cat gotofactors.til
    // Factor an input number - goto version
    var n;
    var f;
    write "Input n please";
    read n;
    write "The factors of n are";
    f := 2;
    // Outer loop over potential factors
    factors:
        if  n = 1 then
            goto endfactors;
        end
    // Inner loop over multiple instances of same factor
    multiples: 
        if (n / f) * f != n then
            goto endmultiples;
        end
        write f;
        n := n / f;
        goto multiples;
    endmultiples:
        f := f + 1;
        goto factors;
    endfactors:

    <linux> txl gotofactors.til TILgotoelim.Txl 
    TXL v10.5 (11.12.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILgotoelim.Txl ... 
    Parsing gotofactors.til ...
    Transforming ...

    // Factor an input number - goto version
    var n;
    var f;
    write "Input n please";
    read n;
    write "The factors of n are";
    f := 2;
    // Outer loop over potential factors
    while n != 1 do
        // Inner loop over multiple instances of same factor
        while (n / f) * f = n do
            write f;
            n := n / f;
        end
        f := f + 1;
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
