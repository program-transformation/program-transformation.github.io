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
    Page](http://www.program-transformation.org/edit/Transform/DeForestation?t=1536825742)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DeForestation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DeForestation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DeForestation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DeForestation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/DeForestation?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DeForestation?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DeForestation?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DeForestation?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DeForestation?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DeForestation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DeForestation?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/DeForestation?template=oopsmore&param1=1.3&param2=1.3)
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
De Forestation {#de-forestation .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Deforestation is a
[ProgramTransformation](ProgramTransformation){.twikiLink} that
eliminates intermediate data-structures (trees). The technique was
invented by [PhilipWadler](PhilipWadler){.twikiLink} for optimization of
functional programs.

The idea is to fuse the composition of two functions `f(g(x))` into a
new function `h(x)` such that the data-structure that is passed from `g`
to `f` is never constructed. This is achieved by creating a new function

      h(x) = f(g(x))

and inlining the definitions of `f` and `g`. If everything works out the
data deconstructors of `f` can be fused with the data constructors of
`g` and no data are constructed. Recursive invocations `f(g(y))` of the
fused functions can be replaced with a call to the new function `h(y)`.

Algorithms for deforestation

-   [ShortCutFusion[^?^](http://www.program-transformation.org/edit/Transform/ShortCutFusion?topicparent=Transform.DeForestation)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [WarmFusion[^?^](http://www.program-transformation.org/edit/Transform/WarmFusion?topicparent=Transform.DeForestation)]{.twikiNewLink
    style="background : #FFFFCE;"}

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 02 Dec 2001

------------------------------------------------------------------------

[CategoryOptimization](CategoryOptimization){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.DeForestation moved from
Transform.DeforestationTransformation on 02 Dec 2001 - 09:08 by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/DeForestation?newweb=Transform&newtopic=DeforestationTransformation&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
