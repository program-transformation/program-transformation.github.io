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
    Page](http://www.program-transformation.org/edit/Sts/TILBegin-EndExtensionUsingTXL?t=1536827760)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/TILBegin-EndExtensionUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/TILBegin-EndExtensionUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/TILBegin-EndExtensionUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/TILBegin-EndExtensionUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/TILBegin-EndExtensionUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/TILBegin-EndExtensionUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/TILBegin-EndExtensionUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/TILBegin-EndExtensionUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
TILBegin-EndExtensionUsingTXL {#tilbegin-endextensionusingtxl .twikiTopicTitle}
=============================

::: {.twikiWebTitle}
Software Transformation Systems
:::

A TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#1.3, the
begin-end syntax extension for the [Tiny Imperative
Language](TinyImperativeLanguage){.twikiLink}.

TXL is designed for implementing language extensions, so adding a new
syntactic feature is simple in TXL using [Grammar
Overrides](GrammarOverrides){.twikiLink}. The \"\...\" in the
\"redefine\" is not a shorthand in this example, rather a language
feature of TXL that denotes an extension to the existing nonterminal
alternatives.

Since there is no semantics for begin-end in TIL, we don\'t add any
transform for this yet.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 10 Oct 2005

*File \"TILbeginparser.Txl\"*

    % TXL parser for begin-end language extenssion to Tiny Imperative Language
    % Jim Cordy, October 2005

    % Begin with the standard TIL grammar
    include "TIL.Grm"

    % Add begin-end statements using grammar overrides
    redefine statement
            ...                  % refers to all existing forms for [statement]
        |   [begin_statement]    % add alternative for our new form
    end redefine

    define begin_statement
        'begin                   [IN][NL]
            [statement*]         [EX]
        'end                     [NL]
    end define

    % No need to do anything except recognize the input, since the grammar
    % includes the output formatting cues
    function main
       match [program]
          _ [program]
    end function

*Example run:*

    <linux> cat begintest.til 
    // Factor an input number
    begin
    var n; 
    write "Input n please"; read n;
    write "The factors of n are"; 
    begin
    var f; f := 2;
    while n != 1 do 
        while (n / f) * f = n do
            // Got one - print it!
            write f; 
            n := n / f;
        end
        f := f + 1;
    end end end
    <linux> txl begintest.til TILbeginparser.Txl 
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILbeginparser.Txl ... 
    Parsing begintest.til ...
    Transforming ...
    begin
        var n;
        write "Input n please";
        read n;
        write "The factors of n are";
        begin
            var f;
            f := 2;
            while n != 1 do
                while (n / f) * f = n do
                    write f;
                    n := n / f;
                end
                f := f + 1;
            end
        end
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
