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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationAndReverseEngineering?t=1536826290)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationAndReverseEngineering)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationAndReverseEngineering)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationAndReverseEngineering?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationAndReverseEngineering?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Transform/DecompilationAndReverseEngineering?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Transform/DecompilationAndReverseEngineering?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Transform/DecompilationAndReverseEngineering?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/DecompilationAndReverseEngineering?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/DecompilationAndReverseEngineering?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/DecompilationAndReverseEngineering?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationAndReverseEngineering)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationAndReverseEngineering?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationAndReverseEngineering?template=oopsmore&param1=1.8&param2=1.8)
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
Decompilation And Reverse Engineering {#decompilation-and-reverse-engineering .twikiTopicTitle}
=====================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The colloquial use of \"reverse engineering\" and the formal one are
somewhat different. Crackers speak of \"reversing\" a program, when they
are talking about a quick, focused exploration of an executable program,
not the in-depth analysis (usually starting with source code) that is
traditional reverse engineering.

Here is a diagram of the most traditional form of reverse engineering,
architecture abstraction. It was for a long time featured on the
[ReEngineering](ReEngineering){.twikiLink} page, and comes originally
from E. J. Byrne (*A Conceptual Foundation for Software Re-Engineering*,
[ICSM](ICSM){.twikiLink} 1992, pp. 226-235):

![byrne.gif](../pub/Transform/ReEngineering/byrne.gif)

I have my own diagram for the position of decompilation within
traditional reverse engineering:

![Overview of decompilation and reverse
engineering](../pub/Transform/DecompilationAndReverseEngineering/decompOverview6.png){width="439"
height="513"}

As you can see, decopilation stops where architecture abstraction starts
(with the implementation, i.e. the source code). Decompilation is
certainly reverse engineering, since it is increasing the level of
abstraction. It\'s just that it starts lower and ends lower than most
reverse engineering. If a decompiler was used to recover old machine
code into a new system, then decompilation would be part of this
reengineering; the horseshoe would be a bit taller (at least on one
side; usually compilation is not considered part of forward engineering,
since it is a totally automatic step).

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
