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
    Page](http://www.program-transformation.org/edit/Transform/TailCallElimination?t=1536825811)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/TailCallElimination)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/TailCallElimination)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/TailCallElimination?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/TailCallElimination?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/TailCallElimination?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/TailCallElimination?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/TailCallElimination?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/TailCallElimination)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/TailCallElimination?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/TailCallElimination?template=oopsmore&param1=1.2&param2=1.2)
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
Tail Call Elimination {#tail-call-elimination .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

A function call as the last action of function body can be optimized by
overwriting the stack frame of the caller. The callee returns directly
to the caller of its caller. The gain of this [program
optimization](ProgramOptimization){.twikiLink} is the stack space that
is saved and a few instructions for restoring the return address and
jumping to it. It can be as simple as replacing the call and return
instructions with a jump instruction. [Tail recursion
elimination](TailRecursionElimination){.twikiLink} is a special case.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 06 Dec 2001\

------------------------------------------------------------------------

[CategoryOptimization](CategoryOptimization){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
