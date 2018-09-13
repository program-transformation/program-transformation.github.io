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
    Page](http://www.program-transformation.org/edit/Transform/ProgramAnalysis?t=1536825741)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ProgramAnalysis)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ProgramAnalysis)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ProgramAnalysis?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ProgramAnalysis?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/ProgramAnalysis?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/ProgramAnalysis?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/ProgramAnalysis?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ProgramAnalysis)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ProgramAnalysis?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/ProgramAnalysis?template=oopsmore&param1=1.2&param2=1.2)
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
Program Analysis {#program-analysis .twikiTopicTitle}
================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[ProgramAnalysis](ProgramAnalysis){.twikiLink} is the (automated)
inspection of a program to infer some property. Program analysis is
needed for most kinds of
[ProgramTransformation](ProgramTransformation){.twikiLink} and can range
from simple local properties in
[PatternMatching](PatternMatching){.twikiLink} to more complicated
global properties in
[DeadCodeElimination[^?^](http://www.program-transformation.org/edit/Transform/DeadCodeElimination?topicparent=Transform.ProgramAnalysis)]{.twikiNewLink
style="background : #FFFFCE;"}.

Tools for program analysis

-   [BANE](BANE){.twikiLink}

Analysis paradigms

-   [TypeBasedAnalysis](TypeBasedAnalysis){.twikiLink}

------------------------------------------------------------------------

I came acrosss an article by Tom Reps called \"Program Analysis via
Graph Reachability\", *Information and Software Technology*
40(1998):701-726, available from <http://www.cs.wisc.edu/~reps/>

Its first paragraph nicely summarizes program analysis:

-   The purpose of program analysis is to ascertain information about a
    program without actually running the program. For example, in
    classical dataflow analysis of imperative programs, the goal is to
    associate an appropriate set of \"dataflow facts\" with each program
    point (i.e., with each assignment statement, call statement, I/O
    statement, predicate of a loop or conditional statement, etc.).
    Typically, the dataflow facts associated with a program point *p*
    describe some aspect of the execution state that holds when control
    reaches *p*, such as available expressions, live variables, reaching
    definitions, etc. Information obtained from program analysis is used
    in [ProgramOptimization](ProgramOptimization){.twikiLink}, as well
    as in tools for software engineering and
    [ReEngineering](ReEngineering){.twikiLink}.

\--ArieVanDeursen

------------------------------------------------------------------------

[CategoryAnalysis](CategoryAnalysis){.twikiLink} \| Contributions by
[EelcoVisser](../Main/EelcoVisser){.twikiLink},
[ArieVanDeursen](ArieVanDeursen){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
