::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

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
    Page](http://www.program-transformation.org/edit/Transform/ProcedureSplitting?t=1536825811)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ProcedureSplitting)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ProcedureSplitting)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ProcedureSplitting?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ProcedureSplitting?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/ProcedureSplitting?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ProcedureSplitting)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ProcedureSplitting?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/ProcedureSplitting?template=oopsmore&param1=1.1&param2=1.1)
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
Procedure Splitting {#procedure-splitting .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

With this technique, procedures are split into two parts, the main part
(predicted to be executed frequently), and the \"fluff\" (code such as
error recovery that is predicted to be executed infrequently). The fluff
for several procedures is collected into one special procedure; special
precautions are taken to avoid the usual procedure invocation overhead.

The idea is to keep as many of the hot parts of procedures in the
machine\'s instruction cache, and to keep the cold code away from that
cache. Ideally, the cold code will never even be paged into memory, and
the machine\'s cache contains most of the hot code.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 01 Dec 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
