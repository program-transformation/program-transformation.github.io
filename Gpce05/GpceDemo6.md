::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/Gpce05/WebLeftBar/gpce-logo.jpg){width="100" height="120"}

**[GPCE Home](../Gpce/WebHome){.twikiLink}**\
**[GPCE\'05 Home](WebHome){.twikiLink}**\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Venue](http://www.cs.ioc.ee/tfp-icfp-gpce05/venue.html)

**[Program](ConferenceProgram){.twikiLink}**\
**[Registration](ConferenceRegistration){.twikiLink}**\
[GPCE conference](ProgramMainEvent){.twikiLink}\
[Affiliated events](ProgramsAffiliatedEvents){.twikiLink}

**[Tutorials and Workshops](GpceTutorialsAndWorkshops){.twikiLink}**\
[W1](YoungResearchers){.twikiLink}\| [W2](MetaOCaml){.twikiLink}\|
[W3](GraphModelTransformations){.twikiLink}\
[T1](TutorialT1){.twikiLink} \| [T2](TutorialT2){.twikiLink}

**[Travel, Hotels, etc.](http://www.cs.ioc.ee/tfp-icfp-gpce05/)**\
[Tallinn](http://www.brics.dk/~danvy/icfp05/Tallinn/)

**[Flyer](http://www.disi.unige.it/person/MoggiE/GPCE05.pdf)** (pdf)

**Calls for**\
[Demos](CallForDemonstrations){.twikiLink}\
[Papers](CallForPapers){.twikiLink}\
[Tutorials](CallForTutorials){.twikiLink}\
[Workshops](CallForWorkshops){.twikiLink}

**[Camera-ready\
Submission](AuthorInstructions){.twikiLink}**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Gpce05/GpceDemo6?t=1536827963)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gpce05/GpceDemo6)
-   [Attach
    File](http://www.program-transformation.org/attach/Gpce05/GpceDemo6)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gpce05/GpceDemo6?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gpce05/GpceDemo6?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Gpce05/GpceDemo6?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Gpce05/GpceDemo6?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Gpce05/GpceDemo6?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Gpce05/GpceDemo6?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Gpce05/GpceDemo6?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gpce05/GpceDemo6?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gpce05/GpceDemo6)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gpce05/GpceDemo6?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Gpce05/GpceDemo6?template=oopsmore&param1=1.4&param2=1.4)
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
[]{#GPCE_OOPSLA_Demonstration_14_18}[]{#GPCE_OOPSLA_Demonstration_14_18_} GPCE/OOPSLA Demonstration 14
======================================================================================================

[]{#Program_Transformations_for_Re_E} Program Transformations for Re-Engineering C++ Components
-----------------------------------------------------------------------------------------------

**Ira Baxter**, Semantic Designs\
**Larry Akers**, Semantic Designs\
**Michael Mehlich**, Semantic Designs

### []{#Summary} Summary

Component-based software engineering enables applications to be
assembled from component parts, provided they adhere to a
component-style specific interface specification and protocol.
Obviously, components available for one style are not available for
another. Component styles evolve, too, which can obsolete components
using a legacy style. This creates a demand for migrating components
from one style to another, which can require complex changes to the
component source code. For a large component library, doing this
manually is likely prohibitive. An alternative is to apply automated
program transformations to carry out the changes.

Using source-to-source transformations on real code requires a scalable,
robust program transformation technology. Such technologies are
difficult to justify for single applications. DMS is a commercial
program transformation system which has been used to transform many
programming languages, including C++, C\#, Java and ObjectPascal. It is
parameterized by language and desired task, enabling its infrastructure
costs to be amortized across many different software analysis or change
applications.

This demonstration shows a concrete example of DMS program
transformations being used to migrate legacy C++ components from a
Boeing distributed avionics software system, using a Boeing proprietary
component format, to a CORBA component style. The conversion requires
nontrivial understanding and manipulation of the C++ source code. It
will explain the component migration problem to be solved, show some of
the transformations, and actually convert a component.

### []{#Times_and_Locations} Times and Locations

-   Wed, 27 Oct., 15.30 - 16.15, Exhibition Hall Demo Room 3
-   Thu, 28 Oct., 11.30 - 12.15, Exhibition Hall Demo Room 2

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
