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
    Page](http://www.program-transformation.org/edit/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?t=1536825458)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?template=oopsmore&param1=1.5&param2=1.5)
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
A new revision of this paper is available under the title [A Survey of
Strategies in Rule Based Program Transformation
Systems](http://www.program-transformation.org/Transform/ASurveyOfStrategiesInRuleBasedProgramTransformationSystems){.twikiLink}.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 12 Mar 2004

------------------------------------------------------------------------

[EelcoVisser](../Main/EelcoVisser){.twikiLink}. **A Survey of Rewriting
Strategies in Program Transformation Systems**. Draft. February 23, 2003
([pdf](http://www.cs.uu.nl/~visser/ftp/Vis03-survey.pdf))

**Abstract**

Program transformation is used in a wide range of applications including
compiler construction, optimization, program synthesis, refactoring,
software renovation, and reverse engineering. In the realization of a
program transformation system for a certain type of transformation,
design choices must be made regarding the representation of programs and
the paradigm for implementation of transformations. This paper gives a
taxonomy of the application areas of program transformation, discusses
considerations to be made in the implementation of program
transformation systems, especially focussing on the specification of
transformation *strategies*.

Complex program transformations are achieved through a number of
consecutive modifications of a program. Basic modifications can be
modeled by rewrite rules, i.e., rules that rewrite a program
representation. A transformation *strategy* is an algorithm for choosing
a path in the rewrite relation induced by a set of rules. The
development of strategies in program transformation systems is
illustrated by a discussion of the support for strategies in several
typical systems.

------------------------------------------------------------------------

An earlier version appeared as

E. Visser. A survey of rewriting strategies in program transformation
systems. In B. Gramlich and S. Lucas, editors, Workshop on Reduction
Strategies in Rewriting and Programming ([WRS](WRS){.twikiLink}\'01),
volume 57 of Electronic Notes in Theoretical Computer Science, Utrecht,
The Netherlands, May 2001. Elsevier Science Publishers.

**Abstract**

Program transformation is used in a wide range of applications including
compiler construction, optimization, program synthesis, refactoring,
software renovation, and reverse engineering. Complex program
transformations are achieved through a number of consecutive
modifications of a program. Transformation rules define basic
modifications. A transformation strategy is an algorithm for choosing a
path in the rewrite relation induced by a set of rules. This paper
surveys the support for the definition of strategies in program
transformation systems. After a discussion of kinds of program
transformation and choices in program representation, the basic elements
of a strategy system are discussed and the choices in the design of a
strategy language are considered. Several styles of strategy systems as
provided in existing languages are then analyzed.

**Download**

-   <http://www.cs.uu.nl/~visser/ftp/Vis01-WRS.pdf>

------------------------------------------------------------------------

[CategoryPaper](CategoryPaper){.twikiLink} \| \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 14 May 2001\

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.ASurveyOfRewritingStrategiesInProgramTransformationSystems
moved from Transform.ASurveyOfStrategiesInProgramTransformationSystems
on 06 Dec 2001 - 17:41 by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems?newweb=Transform&newtopic=ASurveyOfStrategiesInProgramTransformationSystems&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
