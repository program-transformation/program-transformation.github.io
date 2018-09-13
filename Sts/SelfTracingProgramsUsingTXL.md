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
    Page](http://www.program-transformation.org/edit/Sts/SelfTracingProgramsUsingTXL?t=1536827752)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/SelfTracingProgramsUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/SelfTracingProgramsUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/SelfTracingProgramsUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/SelfTracingProgramsUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Sts/SelfTracingProgramsUsingTXL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/SelfTracingProgramsUsingTXL?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sts/SelfTracingProgramsUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/SelfTracingProgramsUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/SelfTracingProgramsUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sts/SelfTracingProgramsUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
Self Tracing Programs Using TXL {#self-tracing-programs-using-txl .twikiTopicTitle}
===============================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#4.3:
Self-tracing program transformation.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 10 Oct 2005

*File \"TILtrace.Txl\"*

    % Simple transform to make a Tiny Imperative Language program self-tracing
    % Jim Cordy, August 2005

    % Replaces every statement in the program with a write statement of its text
    % followed by itself.  For example:
    %
    %    write ("x := 5;");
    %    x := 5;

    % Begin with the TIL base grammar
    include "TIL.Grm"

    % We don't bother preserving comments in this transformation
    % since we're not interested in maintaining the result, just running it

    % Tell TXL what our string escape convention is
    #pragma -esc "\"

    % Allow for concise elided structured statements
    redefine statement
            ... 
        |     [SP] '... [SP]
    end redefine

    % Allow for traced statements - the attribute TRACED marks statements already done
    redefine statement
            ...
        |    [traced_statement]
    end redefine

    define traced_statement
        [statement] [attr 'TRACED]
    end define

    % Replace every statement by a tracing write statement followed by itself
    rule main
        % Since our result requires two statements where one was before,
        % we work on the statement sequence one level up
        replace [repeat statement]
            S [statement]
            Rest [repeat statement]
        % Semantic guard: if it's already done don't do it again
        deconstruct not S
            _ [statement] 'TRACED
        % Make a concise version of structured statements
        construct ConciseS [statement]
            S [deleteBody]
        % Make a string literal of the text of the concise statement
        construct QuotedS [stringlit]
            _ [+ "Trace: "] [quote ConciseS] 
        by
            'write QuotedS;    'TRACED
            S                  'TRACED
            Rest
    end rule

    % Replace any embedded statement sequence in the printed version of 
    % a traced statement with an elision symbol for conciseness
    function deleteBody
        replace * [statement*]
            _ [statement*]
        by
            '...
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
    <linux> txl factors.til TILtrace.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILtrace.Txl ... 
    Parsing factors.til ...
    Transforming ...
    write "Trace: var n;";
    var n;
    write "Trace: write \"Input n please\";";
    write "Input n please";
    write "Trace: read n;";
    read n;
    write "Trace: write \"The factors of n are\";";
    write "The factors of n are";
    write "Trace: var f;";
    var f;
    write "Trace: f := 2;";
    f := 2;
    write "Trace: while n != 1 do ... end";
    while n != 1 do
        write "Trace: while (n / f) * f = n do ... end";
        while (n / f) * f = n do
            write "Trace: write f;";
            write f;
            write "Trace: n := n / f;";
            n := n / f;
        end
        write "Trace: f := f + 1;";
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
