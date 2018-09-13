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
    Page](http://www.program-transformation.org/edit/Sts/For-to-Nondeclaring-ForUsingTXL?t=1536827760)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/For-to-Nondeclaring-ForUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/For-to-Nondeclaring-ForUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/For-to-Nondeclaring-ForUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/For-to-Nondeclaring-ForUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/For-to-Nondeclaring-ForUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/For-to-Nondeclaring-ForUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/For-to-Nondeclaring-ForUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/For-to-Nondeclaring-ForUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
For-to-Nondeclaring-ForUsingTXL {#for-to-nondeclaring-forusingtxl .twikiTopicTitle}
===============================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#2.1,
declaring \"for\" statement to nondeclaring \"for\" statement.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 10 Oct 2005

*File \"TILfordeclare.Txl\"*

    % TXL transformation to adapt existing "declaring for" semantics TIL programs
    % to a proposed new semantics in which "for" control variables must be declared
    % Jim Cordy, October 2005

    % Note: In this program all keywords of TIL are quoted in patterns and replacements -
    % this is not strictly necessary, but is conventional style in modern TXL programs.

    % Based on the TIL base grammar
    include "TIL.Grm"

    % Preserve comments, we're probably going to maintain the result
    include "TILCommentOverrides.Grm"

    % Transformation rule to correct all for loops.

    % Default rewrite rule semantics in TXL are compositional fixed point,
    % which for most transformations is the desired semantics.  However,
    % this transformation has no syntactic compositional fixed point.
    % So the alternatives are either a semantically-guarded transformation,
    % a grammar override, or an explicit once-over traversal.
    % This solution uses the last of these, not because it is the best solution
    % but because this example gives us an opportunity to demonstrate that possibility.

    function main
        % This is a function transformer, so it applies only once unless explicitly
        % reapplied.  The "replace *" allows it to search deeply for its pattern.
        % The replacement reapplies it twice to implement an explicit traversal.

        replace * [statement*]
            'for Id [id] := Expn1 [expression] 'to Expn2 [expression] 'do
                Statements [statement*]
            'end
            MoreStatements [statement*]
        by
            'var Id;
            'for Id := Expn1 'to Expn2 'do
                Statements [main]
            'end
            MoreStatements [main]
    end function

*Example run:*

    <linux> cat multiples.til 
    // Test of declaring for loop in TIL
    // Output first 10 multiples of numbers 1 through 9
    for i := 1 to 9 do
    for j := 1 to 10 do
        write i*j;
    end end
    <linux> txl multiples.til TILfordeclare.Txl 
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILfordeclare.Txl ... 
    Parsing multiples.til ...
    Transforming ...
    // Test of declaring for loop in TIL
    // Output first 10 multiples of numbers 1 through 9
    var i;
    for i := 1 to 9 do
        var j;
        for j := 1 to 10 do
            write i * j;
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
