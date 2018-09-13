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
    Page](http://www.program-transformation.org/edit/Transform/JustInTime?t=1536826509)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/JustInTime)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/JustInTime)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/JustInTime?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/JustInTime?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/JustInTime?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/JustInTime?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/JustInTime?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/JustInTime)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/JustInTime?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/JustInTime?template=oopsmore&param1=1.2&param2=1.2)
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
Just In Time {#just-in-time .twikiTopicTitle}
============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Just In Time dynamic compilers, also called JITs, are programs that
postpone compilation (translation from some input language such as Java
[ByteCodes](ByteCodes){.twikiLink}) until the code is actually needed to
be run. At that point, the input code is translated into native machine
instructions to form a code fragment, which is also stored in the
fragment cache. If the code is needed again later, it is run from the
cache at full native speed, so the cost of translation is amortized over
many runs of the code.

Actually, many JITs do not translate all input code. Only code that is
known to be executed several times (a so called \"hot trace\") is
translated; other code may be interpreted. This would be a two stage
[DynamicTranslator](DynamicTranslator){.twikiLink}. A multistage JIT
such as Sun\'s
[HotSpot](http://java.sun.com/products/hotspot/index.html) (server
version) also performs expensive optimizations usually reserved for
[StaticTranslators](StaticTranslator){.twikiLink}.

To find out what code is hot and what is not, the input code must be
instrumented. For example, counters may be placed at the start of
methods, and at all backwards conditional branches (which may form the
end of loops).

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 01 Dec 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
