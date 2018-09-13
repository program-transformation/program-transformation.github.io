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
    Page](http://www.program-transformation.org/edit/Gpce05/TutorialGP4?t=1536827966)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gpce05/TutorialGP4)
-   [Attach
    File](http://www.program-transformation.org/attach/Gpce05/TutorialGP4)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gpce05/TutorialGP4?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gpce05/TutorialGP4?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Gpce05/TutorialGP4?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Gpce05/TutorialGP4?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Gpce05/TutorialGP4?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Gpce05/TutorialGP4?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Gpce05/TutorialGP4?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Gpce05/TutorialGP4?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gpce05/TutorialGP4)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gpce05/TutorialGP4?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Gpce05/TutorialGP4?template=oopsmore&param1=1.5&param2=1.5)
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
Tutorial GP4 {#tutorial-gp4 .twikiTopicTitle}
============

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

Program Transformation Systems: Theory and Practice for Software Generation, Maintenance and Reengineering
----------------------------------------------------------------------------------------------------------

### []{#Description} Description

As software demands grow, so does the need for tools to aid software
engineers in designing, building and maintaining software systems.
Software maintenance costs dominate software engineering costs, partly
because most such engineering is done manually. Program transformation
systems are semantically sound tools that modify programs (implement
specifications, reverse engineer, change/modify/maintain code). These
tools work by applying a knowledge base of software modification
components called transformations that capture software system
implementation knowledge. The transformations mechanically reuse domain
engineering products to provide domain-specific automated analysis,
modification, and generation of software, therefore enhancing
productivity and quality over conventional methods.

Program transformation systems can capture software system
implementation knowledge, as well as mechanically reuse
domain-engineering products to provide domain-specific program
generation. Because they provide automation, they can carry out massive
changes to large-scale legacy systems that would be impractical by hand,
such as Y2K remediation, system porting, refactoring, etc. The
implementation knowledge available to a transformation system is key to
carrying out reverse engineering, by explaining how code can implement
proposed abstractions. Lastly, from the proper perspective, these
systems can unify specification, design, and maintenance lifecycle
phases.

An understanding of transformation system theory and technology can
provide a deep understanding of how code generation, modification, and
reuse of code and other software engineering artifacts can work. This
tutorial provides a complete overview of transformation systems, from
theory to implementation to application. The tutorial progresses from
introductory to intermediate, all the necessary background will be
provided, so attendees need only have basic software engineering
knowledge and motivating experience modifying software.

Additional information about the topics covered in this tutorial can be
found at [Semantic Designs](http://www.semdesigns.com/).

### []{#Location} Location

Pan Pacific Boardroom

### []{#Date_and_Time} Date and Time

Monday 10-25-2004 8:30 - 5:00 pm (full-day)

### []{#Presenters} Presenters

Ira Baxter, Semantic Designs, Inc., idbaxter (at) semdesigns.com

Hongjun Zheng, Semantic Designs, Inc., hzheng (at) semdesigns.com

Ira Baxter has been building system software since 1969. He acquired his
Ph.D. with emphasis on software engineering and reuse from the
University of California at Irvine in 1990. He has worked with a number
transformation systems starting with Draco in 1975, and is presently the
architect of DMS, a commercial program transformation system, and
designer of the PARLANSE parallel programming language in which DMS is
implemented. Dr. Baxter has been invited speaker at SSR'99, co-Chair of
the 1997 International Conference on Software Reuse, Program co-Chair of
the Working Conference on Reverse Engineering, and Program co-Chair of
the 2002 International Conference on Software Maintenance, and has been
a PC member of the International Conference on Software Maintenance for
a number of years.

Hongjun Zheng, received Ph.D. on computer science at Peking University
in 1997, M.S. on computer science at Jilin University in 1994. He is an
active professional in R&D of software engineering. He played
inseparable roles in diverse projects. Dr. Zheng, at Semantic Designs,
is performing research on generalized compiler framework for programming
languages used in large-scale software evolution and maintenance
environment. He is member of ACM and senior member of IEEE. Dr. Zheng
has served as committee member for computer-science conferences,
especially those focused on software engineering and formal methods:
International Conference on Formal Engineering Methods (2003, 2004),
International Workshop on Source Code Analysis and Manipulation (2004),
International Colloquium on Theoretical Aspects of Computing (2004).\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
