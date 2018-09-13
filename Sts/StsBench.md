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
    Page](http://www.program-transformation.org/edit/Sts/StsBench?t=1536827700)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/StsBench)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/StsBench)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/StsBench?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/StsBench?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Sts/StsBench?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Sts/StsBench?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Sts/StsBench?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Sts/StsBench?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Sts/StsBench?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Sts/StsBench?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/StsBench)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/StsBench?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Sts/StsBench?template=oopsmore&param1=1.7&param2=1.7)
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
Sts Bench {#sts-bench .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Software Transformation Systems
:::

The goals of benchmarking Software Transformations Systems are:

-   Increase communication on a technical level between designers of
    these systems
-   Provide a quick overview of the languages and tools in this field to
    outsiders
-   Inform people such that they can select the tools that fit best with
    their requirements

Benchmark proposals:

A Tiger compiler has been proposed as a benchmark. Although compilation
is not a profile of source transformation in general, such a benchmark
would bring a number of typical features of STSs to the surface. Tiger
is a small procedural language. Extensions to Tiger might include
object-oriented and aspect-oriented features in order to benchmark other
kinds of transformations.

-   -   [TigerBenchmark](TigerBenchmark){.twikiLink}

Another proposal is to select some small subset of the desk calculator
language that the Synthesizer Generator people defined. By starting out
with such a small language, more people might get involved sooner in the
benchmarking.

The next proposal: automated maintenance on a small subset of Cobol
([MiniCobol[^?^](http://www.program-transformation.org/edit/Sts/MiniCobol?topicparent=Sts.StsBench)]{.twikiNewLink
style="background : #FFFFCE;"}). Somebody would provide a highly trimmed
down COBOL-like grammar, and we could then implement a number of very
simple to reasonable complex maintenance jobs. For example:

-   -   Adding scope terminators to conditional and evaluate statements
    -   A Y2K fix

[Tiny Imperative Language](TinyImperativeLanguage){.twikiLink}: this is
a very small imperative language with assignments, conditional, and
loops. Should be possible to make very small transformation
specifications for this one.

-   The [TIL Chairmarks](TILChairmarks){.twikiLink}
    ([JamesCordy](../Main/JamesCordy){.twikiLink} - 29 Apr 2005): A
    small set of little tiny tasks based on TIL designed to help
    demonstrate the basics of how to use different tools to achieve
    common simple transformation tasks. (Not big enough to be benchmarks
    :-)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
