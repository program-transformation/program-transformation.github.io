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
    Page](http://www.program-transformation.org/edit/Sts/TILPrettyPrinterUsingTXL?t=1536827761)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/TILPrettyPrinterUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/TILPrettyPrinterUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/TILPrettyPrinterUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/TILPrettyPrinterUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Sts/TILPrettyPrinterUsingTXL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/TILPrettyPrinterUsingTXL?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sts/TILPrettyPrinterUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/TILPrettyPrinterUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/TILPrettyPrinterUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sts/TILPrettyPrinterUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
TILPretty Printer Using TXL {#tilpretty-printer-using-txl .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Software Transformation Systems
:::

In TXL, all parsers are also pretty printers, so see the [TIL Parser
Using TXL](TILParserUsingTXL){.twikiLink} if comments are not an issue.
Because the TXL solution to preserving formatting and comments in a
transformation is [Source Factoring](SourceFactoring){.twikiLink},
comments are not normally handled using TXL itself.

However, in TXL it is also possible to handle comments by parsing them,
either as disciplined comments (those appearing in predicted places,
which of course is possible using any system), or using [Robust
Parsing](RobustParsing){.twikiLink} techniques.

TXL allows for the addition of disciplined comments to an existing base
grammar using [Grammar Overrides](GrammarOverrides){.twikiLink}. The
example below is based on the TXL base grammar for TIL given on the [TIL
Parser Using TXL](TILParserUsingTXL){.twikiLink} page, and implements a
pretty printer for TIL with discplined comment handling.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 17 Aug 2005 (revised
[JamesCordy](../Main/JamesCordy){.twikiLink} - 10 Oct 2005)

*File \"TILpretty.Txl\"*

    % TXL parser / pretty-printer for Tiny Imperative Language,
    % with disciplined comment handling
    include "TIL.Grm"

    #define COMMENTS

    % Add optional grammar overrides for disciplined end-of-line comments
    % in the C++ style.  You can either control this either by commenting/uncommenting
    % the #define above, or by using -d COMMENTS on the TXL command line
    #if COMMENTS then
        include "TILCommentOverrides.Grm"
    #end if

    % No need to do anything except recognize the input, since the grammar
    % includes the formatting cues
    function main
        match [program]
            _ [program]
    end function

*File \"TILCommentOverrides.Grm\"*

    % Grammar overrides to allow for disciplined TIL comments in the C++ style.
    % (Handling more general undisciplined comments is more complicated,
    %  see the TXL C grammar.)

    #pragma -comment

    comments
        //
    end comments

    redefine statement
            ...
        |  [comment_statement]
    end redefine

    define comment_statement
        [repeat comment_NL+]
    end define

    define comment_NL
        [comment] [NL]
    end define

*Example run:*

    <linux> cat factors.til
    // Factor an input number
    var n; write "Input n please"; read n;
    write 
    "The factors of n are"; var f; f := 2;
    while n != 1 do while (n / f) * f = n do
            // Got one - print it!
            write f; n := n / f;
    end
        f := f + 1;
            end
    <linux> txl factors.til TILpretty.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILpretty.Txl ... 
    Parsing factors.til ...
    Transforming ...
    // Factor an input number
    var n;
    write "Input n please";
    read n;
    write "The factors of n are";
    var f;
    f := 2;
    while n != 1 do
        while (n / f) * f = n do
            // Got one - print it!
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
