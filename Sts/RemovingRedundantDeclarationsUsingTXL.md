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
    Page](http://www.program-transformation.org/edit/Sts/RemovingRedundantDeclarationsUsingTXL?t=1536827757)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/RemovingRedundantDeclarationsUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/RemovingRedundantDeclarationsUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/RemovingRedundantDeclarationsUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/RemovingRedundantDeclarationsUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/RemovingRedundantDeclarationsUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/RemovingRedundantDeclarationsUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/RemovingRedundantDeclarationsUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/RemovingRedundantDeclarationsUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Removing Redundant Declarations Using TXL {#removing-redundant-declarations-using-txl .twikiTopicTitle}
=========================================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#4.1:
Removing redundant declarations.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 04 Jul 2006

*File \"TILredundant.Txl\"*

    % TXL transformation to remove unused declarations in a TIL program
    % Jim Cordy, July 2006

    % Based on the TIL base grammar
    include "TIL.Grm"

    % Preserve comments, we're probably going to maintain the result
    include "TILCommentOverrides.Grm"

    % Transformation rule to remove all redundant variable declarations from a program.
    % If a declared variable is not mentioned by the following statements, it is not used.

    rule main
        % Find each variable declaration
        replace [statement*]
            'var Id [id] ';
            FollowingStatements [statement*]

        % Check to see if the declared identifier does not appear in the following statements
        deconstruct not * [id] FollowingStatements
            Id

        % If not, the declaration is redundant so we remove it
        by
            FollowingStatements
    end rule

*Example run:*

    <linux> cat redundantvareg.til
    // Meaningless example TIL program with some redundant declarations
    // (the ones with names like rr, rx, ry, rm)
    var d;
    var y;
    d := 17;
    read y;
    var rr;
    while y != 0 do
        var rx;
        var a;
        a := 3;
        var j;
        j := 1;
        while j != 100 do
            a := a * 2;
            var ry;
            j := j + 1;
        end
        var c;
        c := a + j;
        var n;
        n := c * y;
        write n;
        y := y - 1;
        var rm;
    end
    <linux> txl redundantvareg.til TILredundant.Txl 
    TXL v10.4c (15.3.06) (c)1988-2006 Queen's University at Kingston
    Compiling TILredundant.Txl ... 
    Parsing redundantvareg.til ...
    Transforming ...
    // Meaningless example TIL program with some redundant declarations 
    // (the ones with names like rr, rx, ry, rm)
    var d;
    var y;
    d := 17;
    read y;
    while y != 0 do
        var a;
        a := 3;
        var j;
        j := 1;
        while j != 100 do
            a := a * 2;
            j := j + 1;
        end
        var c;
        c := a + j;
        var n;
        n := c * y;
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
