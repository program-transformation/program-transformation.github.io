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
    Page](http://www.program-transformation.org/edit/Gpce05/GpceDemo3?t=1536827966)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gpce05/GpceDemo3)
-   [Attach
    File](http://www.program-transformation.org/attach/Gpce05/GpceDemo3)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gpce05/GpceDemo3?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gpce05/GpceDemo3?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Gpce05/GpceDemo3?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Gpce05/GpceDemo3?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Gpce05/GpceDemo3?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Gpce05/GpceDemo3?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Gpce05/GpceDemo3?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gpce05/GpceDemo3?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gpce05/GpceDemo3)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gpce05/GpceDemo3?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Gpce05/GpceDemo3?template=oopsmore&param1=1.4&param2=1.4)
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
[]{#GPCE_Demonstration_23_g1}[]{#GPCE_Demonstration_23_g1_} GPCE Demonstration 23
=================================================================================

[]{#Implementation_of_DSLs_using_sta} Implementation of DSLs using staged interpreters in MetaOCaml
---------------------------------------------------------------------------------------------------

**Kedar Swadi**, Rice University

### []{#Summary} Summary

Domain-specific languages (DSLs) allow programmers to write applications
faster than in general-purpose languages. Two approaches are commonly
taken to implement DSLs. The first is to compile the DSLs into
machine-level code, or low-level languages such as C. While this results
in fast implementations, writing compilers requires expertise in
compiler technology, and long implementation times. An alternative
approach uses interpreters to implement DSLs. Though easier to write,
extend and maintain than compilers, the overhead of interpretation is
unacceptably large for many applications. Relevance to GPCE and
uniqueness of approach: The shortcomings in either approaches
significantly impede the widespread use of DSL-based generative
programming in software development. The demonstration addresses this
problem using multistage programming. It shows how staged interpreters
for implementing DSLs avoid problems in both abovementioned approaches,
and allow efficient machine-level realizations of DSL programs. Unlike
other existing approaches, this approach guarantees that the generated
code is typesafe. Underlying implementation techniques and technologies
used: This demonstration uses multistage programming in the MetaOCaml
language to write two-stage interpreters which translate DSL programs
into OCaml programs, which are finally compiled into efficient machine
code and executed.

First a quick introduction to multistage programming is given using a
simple example of the power function that computes x\^n. The
demonstration shows how three staging constructs in MetaOCaml are used
to automatically generate typesafe specialised versions of this function
from the generic function.

Second, the demonstration shows how to implement a staged interpreter
for a small language and how to correctly measure performance of
implementations. Finally, the demonstration visually shows performance
gains from a staged interpreter for the LOGO graphics language. This is
done by concurrently running the graphical outputs for the simple and
staged interpreters on two windows placed side-by-side.

Research papers and information about downloading, installing, and using
MetaOCaml are found at <http://www.metaocaml.org>.

### []{#Times_and_Locations} Times and Locations

-   Tue, 26 Oct., 15.30 - 16.15, Exhibition Hall Demo Room 4
-   Thu, 28 Oct., 12.30 - 13.15, Exhibition Hall Demo Room 4

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
