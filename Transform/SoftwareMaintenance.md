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
    Page](http://www.program-transformation.org/edit/Transform/SoftwareMaintenance?t=1536826278)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/SoftwareMaintenance)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/SoftwareMaintenance)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/SoftwareMaintenance?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/SoftwareMaintenance?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    16](http://www.program-transformation.org/view/Transform/SoftwareMaintenance?rev=1.16)
    [(diff 15)](http://www.program-transformation.org/rdiff/Transform/SoftwareMaintenance?rev1=1.16&rev2=1.15)
-   [Rev
    15](http://www.program-transformation.org/view/Transform/SoftwareMaintenance?rev=1.15)
    [(diff 14)](http://www.program-transformation.org/rdiff/Transform/SoftwareMaintenance?rev1=1.15&rev2=1.14)
-   [Rev
    14](http://www.program-transformation.org/view/Transform/SoftwareMaintenance?rev=1.14)
    [(diff 13)](http://www.program-transformation.org/rdiff/Transform/SoftwareMaintenance?rev1=1.14&rev2=1.13)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/SoftwareMaintenance)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/SoftwareMaintenance?template=oopsmore&param1=1.16&param2=1.16)
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
    \...](http://www.program-transformation.org/oops/Transform/SoftwareMaintenance?template=oopsmore&param1=1.16&param2=1.16)
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
Software Maintenance {#software-maintenance .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

------------------------------------------------------------------------

**Definitions**

Software maintenance is defined by the ANSI/IEEE Std. 729-1983 and
[IEEE](IEEE){.twikiLink} Std. 1219-1998 as:

-   *modification of a software product after delivery to correct
    faults, to improve performance or other attributes, or to adapt the
    product to a changed environment.*

The ISO Std. 12207-1995 defines software maintenance as follows:

-   The software product undergoes modification to code and associated
    documentation due to a problem or the need for improvement. The
    objective is to modify the existing software while preserving its
    integrity.

The textbook
[PracticalSoftwareMaintenance](PracticalSoftwareMaintenance){.twikiLink}
(p, 356) provides a more elaborate definition:

-   *the totality of activities required to provide cost-effective
    suport to a software system. Activites are performed during the
    predelivery stage as well as the postdelivery stage. Predelivery
    activities include planning for postdelivery operations,
    supportability, and logistics determination. Postdelivery activities
    include software modification, training, and operating a help desk.*

------------------------------------------------------------------------

**Resources**

[A detailed list of resources on software maintenance and
evolution](EvolutionResources){.twikiLink}

Other resources on software maintenance include:

-   [JournalOfSystemsAndSoftware](JournalOfSystemsAndSoftware){.twikiLink}
-   Chapter 6 of the [SWEBOK](SWEBOK){.twikiLink} guide gives an
    overview of the field.

------------------------------------------------------------------------

**Phases of software evolution**

[KeithBennett](KeithBennett){.twikiLink} and
[VaclavRajlich](VaclavRajlich){.twikiLink} ( *A Staged Model for the
Software Lifecycle* , [IEEE](IEEE){.twikiLink} Computer, July 2000, pp
66-71) argue that software maintenance is not a single phase, but should
be thought of as consisting of several *stages*:

-   Initial development (before maintenance)
-   [SoftwareEvolution](SoftwareEvolution){.twikiLink}: the engineers
    extend the capabilities and functionality of the system to meet
    needs of its users, possibly in major ways
-   Servicing: minor defect repairs
-   Phase out: no more servicing, but still generating revenues
-   Close down: death.

*Evolution could well be a phase in which
[ExtremeProgramming](ExtremeProgramming){.twikiLink} would be adopted
(and XP would make initial development as short as possible, at most a
couple of weeks).* \--ArieVanDeursen

------------------------------------------------------------------------

**Research areas**

Software maintenance research areas from the
[SoftwareMaintenanceAndEvolutionARoadmap](SoftwareMaintenanceAndEvolutionARoadmap){.twikiLink}
include:

-   System dynamics, modeling changes over time
-   [SoftwareProcess](SoftwareProcess){.twikiLink}
-   Impact analysis
-   [ProgramUnderstanding](ProgramUnderstanding){.twikiLink}
-   Management and people issues
-   [ReverseEngineering](ReverseEngineering){.twikiLink}
-   Validation and [SoftwareTesting](SoftwareTesting){.twikiLink}.

------------------------------------------------------------------------

[CategorySoftwareEvolution](CategorySoftwareEvolution){.twikiLink} \|
Contributions by [ArieVanDeursen](ArieVanDeursen){.twikiLink} and
[TomMens](TomMens){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
