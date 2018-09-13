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
    Page](http://www.program-transformation.org/edit/Sts/Declarations-to-GlobalUsingTXL?t=1536827758)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/Declarations-to-GlobalUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/Declarations-to-GlobalUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/Declarations-to-GlobalUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/Declarations-to-GlobalUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/Declarations-to-GlobalUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/Declarations-to-GlobalUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/Declarations-to-GlobalUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/Declarations-to-GlobalUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Declarations-to-GlobalUsingTXL {#declarations-to-globalusingtxl .twikiTopicTitle}
==============================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#2.3,
Declarations-to-global, move all declarations from any nesting level to
the global scope.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 02 Nov 2005

*File \"TILtoglobal.Txl\"*

    % TXL transformation to move all declarations in a TIL program to the 
    % beginning of the program, making their meaning explicit

    % Jim Cordy, October 2005

    % Based on the TIL base grammar
    include "TIL.Grm"

    % Preserve comments, we're probably going to maintain the result
    include "TILCommentOverrides.Grm"

    % Transformation rule to move all declarations to the beginning of the program -
    % does it the easy obvious way, extracting them all, deleting them all, then
    % putting the extracted ones first.  

    function main
        % This is a function transformer, so it applies only once 
        replace [program]
            Program [statement*]

        % Use the type extractor to get all statements as a flat sequence,
        % then filter for declarations only
        construct Declarations [statement*]
                _ [^ Program] [removeNonDeclarations]

        % Make a copy of the program with all declarations removed
        construct ProgramSansDeclarations [statement*]
                Program [removeDeclarations]

        % The result is a program consisting of the sequence of all the
        % declarations concatenated with the original program without declarations
        by
                Declarations [. ProgramSansDeclarations]
    end function

    rule removeDeclarations
        % Rule to remove every declaration at every level from statements
        replace [statement*]
            Declaration [declaration]
            FollowingStatements [statement*]
        by
            FollowingStatements
    end rule

    rule removeNonDeclarations
        % Rule to remove all statements that are not declarations from statements
        replace [statement*]
            NonDeclaration [statement]
            FollowingStatements [statement*]

        % Check that the statement isn't a declaration 
        deconstruct not NonDeclaration
                _ [declaration]

        % If so, take it out
        by
            FollowingStatements
    end rule

*Example run:* \"vareg.til\" is a meaningless little program with lots
of data dependencies for demonstration purposes.

    <linux> cat vareg.til
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
    <linux> txl vareg.til TILtoglobal.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILtoglobal.Txl ... 
    Parsing vareg.til ...
    Transforming ...
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
    <linux> 

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
