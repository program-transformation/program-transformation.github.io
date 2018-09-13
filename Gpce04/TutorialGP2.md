::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/Gpce04/WebLeftBar/gpce-logo.jpg){width="100" height="120"}\
**[GPCE Home](http://www.gpce.org)**\
**[Home](WebHome){.twikiLink}**\
[Organization](ConferenceOrganization){.twikiLink}\
[Venue](ConferenceVenue){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Program](ConferenceProgram){.twikiLink}\
[Registration](ConferenceRegistration){.twikiLink}

**[Tutorials](GpceTutorials){.twikiLink}**\
[GP1](TutorialGP1){.twikiLink} \| [GP2](TutorialGP2){.twikiLink}\
[GP3](TutorialGP3){.twikiLink} \| [GP4](TutorialGP4){.twikiLink}\

**[Workshops](GpceWorkshops){.twikiLink}**\
[STS](STS){.twikiLink}\
[MetaOCaml](http://www.program-transformation.org/Gpce04/MetaOCaml){.twikiLink}\
[Young
Researchers](http://www.program-transformation.org/Gpce04/YoungResearchers){.twikiLink}

**[Demonstrations](GpceDemonstrations){.twikiLink}**\

**Calls for**\
[Technical Papers](CallForPapers){.twikiLink}\
[Workshops](CallForWorkshops){.twikiLink}\
[Tutorials](CallForTutorials){.twikiLink}\
[Demonstrations](CallForDemonstrations){.twikiLink}

**[Print call](PrintCall){.twikiLink}**\
[Flyer](http://www.cs.uu.nl/~visser/GPCE04-CfC.pdf)

**[Submission](ElectronicSubmission){.twikiLink}**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Gpce04/TutorialGP2?t=1536827566)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gpce04/TutorialGP2)
-   [Attach
    File](http://www.program-transformation.org/attach/Gpce04/TutorialGP2)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gpce04/TutorialGP2?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gpce04/TutorialGP2?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Gpce04/TutorialGP2?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Gpce04/TutorialGP2?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Gpce04/TutorialGP2?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Gpce04/TutorialGP2?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Gpce04/TutorialGP2?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Gpce04/TutorialGP2?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gpce04/TutorialGP2)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gpce04/TutorialGP2?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Gpce04/TutorialGP2?template=oopsmore&param1=1.7&param2=1.7)
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
Generative Programming and Component Engineering {#generative-programming-and-component-engineering .twikiTopicTitle}
================================================

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

Multi-stage Programming in MetaOCaml
------------------------------------

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
hard. [Multi-stage programming (MSP)](http://www.cs.rice.edu/~taha/MSP/)
is a light-weight, semantically-motivated approach to making program
generators easier to write. [MetaOCaml](http://www.metaocaml.org/) is a
programming language that provides special support for MSP by providing:

-   Heigenic quasi-quotation notation for distinguishing different
    computational stages (that is, the generating vs the generated code)
    in a program, and
-   An evaluation construct that allows generated code to be generated
    and executed at runtime, and
-   A type system that statically ensures that this is done safely.

The half-day tutorial will cover

-   Small examples illustrating MSP
-   Cross-stage persistence,
-   What the type system guarantees,
-   MetaOCaml\'s libraries for collecting performance measurements,
-   An application to language implementation (staged interpreters),
-   An introduction to binding-time improvements,
-   An applicaiton to dynamic programming,
-   An introduction to the MSP research literature.

Slides and other updated information regarding this tutorial can be
found at the official [MetaOCaml tutorial web
page](http://www.metaocaml.org/tutorial04/).

### []{#Student_Stipend} Student Stipend

The National Science Foundation (NSF) has kindly provided a number of
stipends to support student travel and participation to attend the
MetaOCaml Tutorial and/or the MetaOCaml Workshop:

<http://metaocaml.org/tutorial4/>

<http://metaocaml.org/workshop04/>

Awards will be made on the basis of relevance to the students education
and research activities. To apply, please send an email to
<taha@rice.edu> by September 5th. The email should include:

1.  1.  1.  ) Primary interest (Tutorial or Workshop)
        2.  ) Explanation of relevance to your current educational
            and/or research goals (200-500 words)
        3.  ) Secondary interest
        4.  ) Explanation of relevance
        5.  ) Estimated travel expense

Reimbursements will be made based on submitted expense receipts.
Students submitting papers to the MetaOCaml Workshop are eligible for
stipends. Amount of stipend will be indicated when you are notified of
the result of your application.

Applications should be sent to <taha@rice.edu> by September 5th, 2004.

### []{#Location} Location

Conf. Ctr. Meeting Room 17

### []{#Date_and_Time} Date and Time

Sunday 1:30 - 5:00 (half-day)

### []{#Presenters} Presenters

Walid Taha, Rice University, taha (at) rice.edu

Cristiano Calcagno, Imperial College, ccris (at) dcs.qmul.ac.uk

Walid Taha and Cristiano Calcagno have been involved in the development
of MetaOCaml since 1999. Walid and Cristiano have also been involved in
the study of type systems for multi-stage languages since 1997. Walid
has a record of organizing a number of successful workshops and
conferences, including SAIG\'00 (organizer and PC Chair), SAIG\'01
(organizer and PC Chair), and GPCE\'02 (General Chair).

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
