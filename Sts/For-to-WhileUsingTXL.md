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
    Page](http://www.program-transformation.org/edit/Sts/For-to-WhileUsingTXL?t=1536827759)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/For-to-WhileUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/For-to-WhileUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/For-to-WhileUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/For-to-WhileUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Sts/For-to-WhileUsingTXL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/For-to-WhileUsingTXL?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sts/For-to-WhileUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/For-to-WhileUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/For-to-WhileUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sts/For-to-WhileUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
For-to-WhileUsingTXL {#for-to-whileusingtxl .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#2.2,
transform all \"for\" statements to their equivalent \"while\" statement
form.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 10 Oct 2005

*File \"TILfortowhile.Txl\"*

    % Convert Tiny Imperative Language "for" statements to "while" form
    % Jim Cordy, August 2005

    % This program converts all "for" statements in a TIL program to
    % their equivalent "while" form

    % Some details assumed:
    %
    % - It is not clear whether TIL is scoped or not.  We assume not
    %   since there is no explicit scoping statement in the language.
    %
    % - The "for" statement of TIL is a "declaring for".
    %   We assume this means it automatically declares its control variable.
    %
    % These assumptions can be trivially changed here if TIL changes.

    % Based on the TIL grammar
    include "TIL.grm"

    % Preserve comments in output
    include "TILCommentOverrides.Grm"

    % Rule to convert every "for" statement
    rule main
        % Capture each "for" statement, in its statement sequence context
        % so that we can replace it with multiple statements
        replace [statement*]
            'for Id [id] := Expn1 [expression] 'to Expn2 [expression] 'do
                Statements [statement*]
            'end
            MoreStatements [statement*]

        % Need a unique new identifier for the upper bound
        construct UpperId [id]
            Id [_ 'Upper] [!]

        % Construct the iterator
        construct IterateStatement [statement]
            Id := Id + 1;

        % Replace the whole thing
        by
            'var Id;
            Id := Expn1;
            'var UpperId;
            UpperId := (Expn2) + 1;
            'while Id - UpperId 'do
                Statements [. IterateStatement]
            'end
            MoreStatements
    end rule

*Example run:*

    <linux> cat multiples.til
    // Test of declaring for loop in TIL
    // Output first 10 multiples of numbers 1 through 9
    for i := 1 to 9 do
    for j := 1 to 10 do
        write i*j;
    end end
    <linux> txl multiples.til TILfortowhile.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILfortowhile.Txl ... 
    Parsing multiples.til ...
    Transforming ...
    // Test of declaring for loop in TIL
    // Output first 10 multiples of numbers 1 through 9
    var i;
    i := 1;
    var i_Upper1;
    i_Upper1 := (9) + 1;
    while i - i_Upper1 do
        var j;
        j := 1;
        var j_Upper1;
        j_Upper1 := (10) + 1;
        while j - j_Upper1 do
            write i * j;
            j := j + 1;
        end
        i := i + 1;
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
