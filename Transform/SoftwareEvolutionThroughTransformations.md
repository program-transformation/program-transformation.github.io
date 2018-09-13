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
    Page](http://www.program-transformation.org/edit/Transform/SoftwareEvolutionThroughTransformations?t=1536826352)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/SoftwareEvolutionThroughTransformations)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/SoftwareEvolutionThroughTransformations)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/SoftwareEvolutionThroughTransformations?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/SoftwareEvolutionThroughTransformations?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/SoftwareEvolutionThroughTransformations?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/SoftwareEvolutionThroughTransformations?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/SoftwareEvolutionThroughTransformations?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/SoftwareEvolutionThroughTransformations?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/SoftwareEvolutionThroughTransformations?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/SoftwareEvolutionThroughTransformations?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/SoftwareEvolutionThroughTransformations)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/SoftwareEvolutionThroughTransformations?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/SoftwareEvolutionThroughTransformations?template=oopsmore&param1=1.4&param2=1.4)
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
Software Evolution Through Transformations {#software-evolution-through-transformations .twikiTopicTitle}
==========================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**ICGT 2002 Workshop on Software Evolution Through Transformations (SET
2002)**

*Towards uniform support throughout the software life-cycle*

Transformations of artefacts like models, schemata, programs, or
[SoftwareArchitectures](SoftwareArchitecture){.twikiLink} provide a
uniform and systematic way to express and reason about
[SoftwareEvolution](SoftwareEvolution){.twikiLink}. For example, in the
context of [ForwardEngineering](ForwardEngineering){.twikiLink}, the
transition between different abstraction levels (like analysis, design,
and implementation) can be described in terms of transformations, like
refinement relations or automatic generation of models or code. In
[ReverseEngineering](ReverseEngineering){.twikiLink}, transformations
are used to build abstractions from implementations, e.g., by detecting
design patterns or clichés.

[Official SET 2002
website](http://www.uni-paderborn.de/cs/ag-engels/Conferences/ICGT02/FSWE/)

------------------------------------------------------------------------

**ICGT 2004 Workshop on Software Evolution Through Transformations
(SETra 2004)**

*Model-based versus implementation-level solutions*

Software evolution can been studied and supported at the level of both
models and programs. Model-based software development as proposed, for
example, by the OMG\'s [MDA](MDA){.twikiLink} initiative, addresses
evolution by automating (via several intermediate levels) the
transformation of models into code. In this way, software can be evolved
at the model level, relying on automated transformations to keep the
implementation in sync. Classical re-engineering technology, instead,
starts at level of programs which, due to the poor quality of models
found in industrial contexts, provide the only definite representation
of the system.

Which approach is better in which situation and how they can be combined
is still an open question. At the conceptual level, the laws of software
evolution and the theory behind them may provide us with answers about
the respective tradeoffs and likely combinations. At the technology
level, graphs defined by meta models, and their transformations, have
been recognized as a uniform way to support evolution, both at the
programming and the model level.

[Official SETra 2004
website](http://wwwcs.upb.de/cs/ag-engels/ag_engl/Segravis/Events/SETra04/)

------------------------------------------------------------------------

**ICGT 2006 Workshop on Software Evolution Through Transformations
(SETra 2006)**

*Embracing The Change*

Transformation-based techniques such as refactoring, model
transformation, architectural reconfiguration, etc. are at the heart of
many software engineering activities, making it possible to cope with an
ever changing environment. This workshop provides a forum for discussing
these techniques, their formal foundations and applications.

[Official SETra 2006
website](http://www.cs.le.ac.uk/people/rh122/setra.html)

------------------------------------------------------------------------

[CategoryConference](CategoryConference){.twikiLink} \|
[CategorySoftwareEvolution](CategorySoftwareEvolution){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.SoftwareEvolutionThroughTransformations moved from
Transform.SET on 09 Jul 2004 - 10:02 by
[TomMens](../Main/TomMens){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/SoftwareEvolutionThroughTransformations?newweb=Transform&newtopic=SET&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
