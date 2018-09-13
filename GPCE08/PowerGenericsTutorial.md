::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE08/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://www.gpce.org/)**\
**[GPCE\'08 Home](WebHome){.twikiLink}**\
[Program](ConferenceProgram){.twikiLink}\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Venue](ConferenceVenue){.twikiLink}\
[Registration](ConferenceRegistration){.twikiLink}

**[Tutorials](GpceTutorials){.twikiLink}**\
[GP1: MDE Systems](MdeTutorial){.twikiLink}\
[GP2: S. Jarzabek](PowerGenericsTutorial){.twikiLink}\
[GP3: W. Taha](MultiStageProgrammingTutorial){.twikiLink}

**[Workshops](GpceWorkshops){.twikiLink}**\
[DSPD 2008](http://www.labri.fr/perso/reveille/DSPD/2008/)\
[McGPLE
2008](http://www.infosun.fim.uni-passau.de/cl/staff/apel/McGPLE2008/index.html)\
[STS 2008](../Sts/STS08)

**Calls for**\
[Papers](CallForPapers){.twikiLink}\
[Tutorials](CallForTutorials){.twikiLink}\
[Workshops](CallForWorkshops){.twikiLink}

**[Electronic\
Submission](http://www.easychair.org/conferences/?conf=gpce2008)**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE08/PowerGenericsTutorial?t=1536827522)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE08/PowerGenericsTutorial)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE08/PowerGenericsTutorial)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE08/PowerGenericsTutorial?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE08/PowerGenericsTutorial?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/GPCE08/PowerGenericsTutorial?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/GPCE08/PowerGenericsTutorial?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/GPCE08/PowerGenericsTutorial?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/GPCE08/PowerGenericsTutorial?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/GPCE08/PowerGenericsTutorial?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/GPCE08/PowerGenericsTutorial?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE08/PowerGenericsTutorial)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE08/PowerGenericsTutorial?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/GPCE08/PowerGenericsTutorial?template=oopsmore&param1=1.6&param2=1.6)
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
PowerGenericsTutorial {#powergenericstutorial .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

[]{#GPCE_Tutorial_2_GP2}[]{#GPCE_Tutorial_2_GP2_} GPCE Tutorial \#2 (GP2)
=========================================================================

[]{#Problems_We_Can_Solve_with_Power}[]{#_Problems_We_Can_Solve_with_Powe} \"Problems We Can Solve with Power-Generics\" by Stan Jarzabek, National University of Singapore
===========================================================================================================================================================================

### []{#Date_Oct_22_afternoon} Date: Oct 22, afternoon

### []{#Description} Description

Repetitions are common in software. Genericity is a prime strategy to
avoid repetitions. STL is a hallmark example of benefits that can be
gained by exploiting software similarities and representing them in
generic form. Can we replicate STL success in other application domains,
e.g., business systems, in which we also observe much similarity?

The concept of power-generics addresses this question, trying to reach
beyond what we can achieve with conventional generic design mechanisms,
such as type-parameterization. The goal of power-generics is to let a
programmer avoid redundancies whenever a programmer wishes to do so. The
basic requirement for power-generics is to represent in a generic form
any group of similar program structures of any kind and granularity,
from similar classes, to recurring similar patterns of collaborating
classes/components, to modules and subsystems.

Why are such power-generics useful and interesting? Power-generics let
us exploit the benefits of non-redundancy and simplification in any
domain where we observe substantial repetitions. They also open a sea of
new possibilities for software engineering methods, in particular for
software reuse via Product Line approach. Reuse goal is to exploit
similarities in a family of software systems to boost productivity.
Power-generics can help us build generic representation for a family of
similar systems, extending the reuse capabilities of current Product
Line Architectures based on components and architectures, whereby
genericity is applied only in ad hoc way. In this context,
power-generics have a role to play in defining effective strategies for
variability management in Product Lines, and extending reuse benefits
from product development to its evolution (maintenance).

The concept of power-generics creates a much missed bridge between
programming language mechanisms and software engineering goals, such as
reusability or maintainability.

In this tutorial, we bring power-generics from the concept to
realization. Our solution is based on meta-level program decomposition,
unrestrictive parameterization, and generation. It is realized by simple
transformations at a meta-level program representation, with XVCL
technique (XML-based Variant Configuration Language,
xvcl.comp.nus.edu.sg).

XVCL program transformations are text-based, and have no regard to the
rules of the underlying programming language. This makes validation of
transformations in conventional sense difficult, if not impossible. A
programmer has to understand a meta-program, as well as a concrete
program, and properly relate one to another. He/she has to debug the
program derivation process, as well as a concrete program.

On the other hand, power-generics with XCL bring attractive and unique
engineering benefits, in terms of improved maintainability, reusability
and software complexity management, in general. These benefits have been
confirmed in industrial applications and lab studies. Empirical and
analytical studies shed light on the sources of the observed benefits,
as well as trade-offs and limitations involved in our realization of the
power-generics concept. The also explain the difficulties of realizing
power-generics with programming language mechanisms, as well as with
component-based and architectural approaches.

In the tutorial, we discuss advantages and compromises involved in
realizing power-generics with techniques such as XVCL. We revisit the
issue of programming language support for software engineering goals. We
compare XVCL with related approaches such as AOP, FOP and Java
annotations. We also discuss automated detection in software systems of
large-granularity similar program structures, as candidates for
power-generics solutions, so-called structural clones.

### []{#Duration} Duration

Half day tutorial.

### []{#Required_experience_target_audie} Required experience / target audience

The audience should have basic understanding of software design and
development. No prior knowledge of a specific programming technologies
is required. The target audience includes academic faculty, students and
researchers, software practitioners, project leaders, analysts and
designers.

### []{#Bio_speaker} Bio speaker

Stan Jarzabek is an Associate Professor at the Department of Computer
Science, School of Computing, National University of Singapore. He spent
12 years of his professional career in industry and 20 years in
academia. Stan is interested in all aspects of software design, in
particular techniques for design of adaptable, easy to change
(high-variability) software. He is an author of a book Effective
Software Maintenance and Evolution: Reuse-based Approach, Taylor &
Francis CRC Press, 2007, and published over 90 papers in international
journals and conference proceedings (his recent paper received the ACM
Distinguished Paper Award). Stan was a Principal Investigator in a
multi-national collaborative project involving universities (NUS and the
University of Waterloo) and companies in Singapore and Toronto.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
