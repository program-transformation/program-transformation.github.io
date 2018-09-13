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
    Page](http://www.program-transformation.org/edit/Sts/StatementStatisticsUsingTXL?t=1536827759)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/StatementStatisticsUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/StatementStatisticsUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/StatementStatisticsUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/StatementStatisticsUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/StatementStatisticsUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/StatementStatisticsUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/StatementStatisticsUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/StatementStatisticsUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Statement Statistics Using TXL {#statement-statistics-using-txl .twikiTopicTitle}
==============================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#4.2:
Collecting statement statistics.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 28 Oct 2005

*File \"TILstats.Txl\"*

    % Gather statement statistics for a Tiny Imperative Language program
    % Jim Cordy, October 2005

    % Gathers and outputs statistics on the number of each kind of statement
    % in a program.  Replaces the program itself with an empty one.

    % Begin with the TIL base grammar
    include "TIL.Grm"

    % Compute and output statement kind statistics, replace program with an empty one.
    % There are many different ways to do this - this naive way is simple and
    % obvioulsy correct, but exposes TXL's need for generics.  
    % Another less clear solution could use polymorphism to avoid the repetition.

    function main
        replace [program]
            Program [program]

        % Count each kind of statement we're interested in
        % by extracting all of each kind from the program

        construct Statements [statement*]
            _ [^ Program]
        construct StatementCount [number]
            _ [length Statements] [putp "Total: %"]

        construct Declarations [declaration*]
            _ [^ Program]
        construct DeclarationsCount [number]
            _ [length Declarations] [putp "Declarations: %"]

        construct Assignments [assignment_statement*]
            _ [^ Program]
        construct AssignmentsCount [number]
            _ [length Assignments] [putp "Assignments: %"]

        construct Ifs [if_statement*]
            _ [^ Program]
        construct IfCount [number]
            _ [length Ifs] [putp "Ifs: %"]

        construct Whiles [while_statement*]
            _ [^ Program]
        construct WhileCount [number]
            _ [length Whiles] [putp "Whiles: %"]

        construct Fors [for_statement*]
            _ [^ Program]
        construct ForCount [number]
            _ [length Fors] [putp "Fors: %"]

        construct Reads [read_statement*]
            _ [^ Program]
        construct ReadCount [number]
            _ [length Reads] [putp "Reads: %"]

        construct Writes [write_statement*]
            _ [^ Program]
        construct WriteCount [number]
            _ [length Writes] [putp "Writes: %"]

        by
            % nothing
    end function

*Example run:*

    <linux> cat factors.til
    // Factor an input number
    var n;
    write "Input n please";
    read n;
    write "The factors of n are";
    var f;
    f := 2;
    while n != 1 do
        while (n / f) * f = n do
            write f;
            n := n / f;
        end
        f := f + 1;
    end
    <linux> txl factors.til TILstats.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILstats.Txl ... 
    Parsing factors.til ...
    Transforming ...
    Total: 11
    Declarations: 2
    Assignments: 3
    Ifs: 0
    Whiles: 2
    Fors: 0
    Reads: 1
    Writes: 3
    <linux> 

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
