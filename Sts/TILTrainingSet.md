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
    Page](http://www.program-transformation.org/edit/Sts/TILTrainingSet?t=1536827760)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/TILTrainingSet)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/TILTrainingSet)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/TILTrainingSet?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/TILTrainingSet?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Sts/TILTrainingSet?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Sts/TILTrainingSet?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Sts/TILTrainingSet?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/TILTrainingSet?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sts/TILTrainingSet?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/TILTrainingSet)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/TILTrainingSet?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Sts/TILTrainingSet?template=oopsmore&param1=1.3&param2=1.3)
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
TILTraining Set {#tiltraining-set .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Software Transformation Systems
:::

**[Tiny Imperative Language](TinyImperativeLanguage){.twikiLink} (TIL)
Example Programs**

Only a couple so far, hopefully many more to come. We\'ve assumed a C++
style commenting convention for the TIL language to make these more
readable.

**factors.til**

Note: This program uses an unspecified assumption (that the \"write\"
statement outputs a full line) \-- JRC

    // Find all factors of a given input number - J.R. Cordy August 2005
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

**factorial.til**

Note: this program, from the Stratego manual, has an error (declaring x)
and uses a couple of unspecified assumptions (that the \"write\"
statement does not output a full line, and that \"\\n\" is allowed and
outputs a newline) \-- JRC

    // TIL program computing the factorial - Eelco Visser 
    var n;
    read n;
    var x;
    var fact;
    fact := 1;
    for x := 1 to n do
        fact := x * fact;
    end
    write "factorial of ";
    write n;
    write " is ";
    write fact;
    write "\n";

**multiples.til**

A for loop testing program.

    // Test of declaring for loop in TIL
    // Output first 10 multiples of numbers 1 through 9
    for i := 1 to 9 do
    for j := 1 to 10 do
        write i*j;
    end end

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 22 Aug 2005 (revised
[JamesCordy](../Main/JamesCordy){.twikiLink} - 10 Oct 2005)\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
