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
    Page](http://www.program-transformation.org/edit/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages?t=1536826402)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/MontagesSpecificationsOfRealisticProgrammingLanguages?template=oopsmore&param1=1.2&param2=1.2)
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
Montages Specifications Of Realistic Programming Languages {#montages-specifications-of-realistic-programming-languages .twikiTopicTitle}
==========================================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

by [PhilippKutter](PhilippKutter){.twikiLink} and
[AlfonsoPierantonio](AlfonsoPierantonio){.twikiLink}. In Journal of
Universal Computer Science, vol. 3, no. 5 (1997), 416\--442

**Abstract**

Montages are a new way of describing all aspects of programming
languages formally. Such specifications are intelligible for a broad
range of people involved in programming language design and use. In
order to enhance readability we combine visual and textual elements to
yield specifications similar in structure, length, and complexity to
those in common language manuals, but with a formal semantics. The
formal semantics is based on Gurevich\'s Abstract State Machines
(formerly called Evolving Algebras).

**Resources**

-   JUCS: <http://www.jucs.org/jucs_3_5/montages_specifications>
-   [ResearchIndex](ResearchIndex){.twikiLink}:
    <http://citeseer.nj.nec.com/kutter97montage.html>
-   [MontagesFramework](MontagesFramework){.twikiLink}
-   [GemMex](GemMex){.twikiLink}

------------------------------------------------------------------------

### []{#Review} Review

Summary

A Montage is a, partially visual, specification of a programming
language construct. The specification consists of a BNF style syntax
definition of the construct, a specification of the control and data
flow through the construct, and a specification of the computation on
the data induced by the construct. Control and data flow are defined by
means of additional edges in the abstract syntax tree. The control flow
edges indicates in which order program points should be visited during
execution. Data flow edges indicate the data dependencies between nodes.
The flow information can be specified using a visual language. The
following picture shows the control and data flow of the while
construct:

![](http://www.tik.ee.ethz.ch/~montages/WhileStmentGraph.xbm)

Computations are defined by functions applied to the values of
previously computed nodes. Control flow is determined by actions which
manipulate the abstract program counter `CurrentTask`. Control flow can
be conditional on data values.

A Montage is translated to rules for an
[AbstractStateMachine[^?^](http://www.program-transformation.org/edit/Transform/AbstractStateMachine?topicparent=Transform.MontagesSpecificationsOfRealisticProgrammingLanguages)]{.twikiNewLink
style="background : #FFFFCE;"}. These rules define how the abstract
program counter and the contents of the store are changed by the
computations of the tokens. The implicit parallelism of the rules is
tamed by annotating program points with flags that indicate whether it
has been executed already.

Questions/Remarks

-   Could control flow not be deduced from the data dependencies? First
    perform the computations corresponding to those nodes from which
    data is needed.

<!-- -->

-   The
    [EvaluationStrategy[^?^](http://www.program-transformation.org/edit/Transform/EvaluationStrategy?topicparent=Transform.MontagesSpecificationsOfRealisticProgrammingLanguages)]{.twikiNewLink
    style="background : #FFFFCE;"} is determined by the specification of
    control flow. How could one model different evaluation strategies
    for the same language? In other words, tying together all semantic
    aspects of a language constructs prevents reuse of some aspect.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 23 Dec 2001\

------------------------------------------------------------------------

[CategoryPaper](CategoryPaper){.twikiLink} \|
[CategoryReview](CategoryReview){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
