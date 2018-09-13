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
    Page](http://www.program-transformation.org/edit/Gpce05/TutorialT1?t=1536826600)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gpce05/TutorialT1)
-   [Attach
    File](http://www.program-transformation.org/attach/Gpce05/TutorialT1)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gpce05/TutorialT1?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gpce05/TutorialT1?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    11](http://www.program-transformation.org/view/Gpce05/TutorialT1?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Gpce05/TutorialT1?rev1=1.11&rev2=1.10)
-   [Rev
    10](http://www.program-transformation.org/view/Gpce05/TutorialT1?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Gpce05/TutorialT1?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Gpce05/TutorialT1?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Gpce05/TutorialT1?rev1=1.9&rev2=1.8)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gpce05/TutorialT1)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gpce05/TutorialT1?template=oopsmore&param1=1.11&param2=1.11)
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
    \...](http://www.program-transformation.org/oops/Gpce05/TutorialT1?template=oopsmore&param1=1.11&param2=1.11)
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
Tutorial T1 {#tutorial-t1 .twikiTopicTitle}
===========

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

Multi-stage Programming in MetaOCaml
------------------------------------

This tutorial is **CONFIRMED**. Limited support is available for
students, please contact <taha@cs.rice.edu>.

### []{#Description} Description

Despite their potential for improving reuse, abstraction mechanisms such
as objects, abstract types, polymorphism, and higher-order types are all
too often considered to have a prohibitive runtime cost. As a result,
many real-world programs are littered with lost opportunities where
these abstraction mechanisms could have been used to improve the quality
of the code, but where they are considered prohibitively expensive. An
important approach to dealing with this problem is program generation,
which can be used to reduce or eliminate the runtime overhead of
abstraction mechanisms. But writing program generators itself can be
hard. [Multi-stage programming
(MSP)](http://www.cs.rice.edu/%7Etaha/MSP/) is a light-weight,
semantically-motivated approach to making program generators easier to
write. [MetaOCaml](http://www.metaocaml.org/) is a programming language
that provides special support for MSP by providing:

-   Hygienic quasi-quotation notation for distinguishing different
    computational stages (that is, the generating vs. the generated
    code) in a program, and
-   An evaluation construct that allows generated code to be generated
    and executed at runtime, and
-   A type system that statically ensures that this is done safely.

The full-day tutorial will cover

-   Small examples illustrating MSP
-   Cross-stage persistence
-   What the type system guarantees
-   MetaOCaml\'s libraries for collecting performance measurements
-   An application to language implementation (staged interpreters)
-   An introduction to binding-time improvements
-   An application to AOSD (aspect weavers)
-   An application to dynamic programming
-   An introduction to the MSP research literature

The tutorial will be presented by [Walid
Taha](http://www.cs.rice.edu/%7Etaha/) and [Cristiano
Calcagno](http://www.doc.ic.ac.uk/%7Eccris/). Active participation is
encouraged. Slides from earlier offerings
([2003](http://www.metaocaml.org/doc/Tutorial%202003.pdf)
[2004](http://www.metaocaml.org/doc/Tutorial%202004.pdf)) of this
tutorial give a good idea of its level. The new slides will be put
online once they are available.

### []{#Location} Location

Vennaste saal

### []{#Date_and_Time} Date and Time

Tuesday, Sep. 27, 2005: 9.00 - 18.00 (full-day)

### []{#Presenters} Presenters

Walid Taha, Rice University, taha (at) cs.rice.edu

Cristiano Calcagno, Imperial College, ccris (at) doc.ic.ac.uk

Walid Taha and Cristiano Calcagno have lead the development of MetaOCaml
since 1999. Walid and Cristiano have also been involved in the study of
type systems for multi-stage languages since 1997.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Gpce05.TutorialT1 moved from Gpce05.TutorialGP1 on 13 Apr 2005 - 16:16
by [AndrewMalton](../Main/AndrewMalton){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Gpce05/TutorialT1?newweb=Gpce05&newtopic=TutorialGP1&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
