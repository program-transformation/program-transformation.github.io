::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE06/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://www.gpce.org/)**\
**[GPCE\'06 Home](WebHome){.twikiLink}**\
**[Final Program](ConferenceProgram){.twikiLink}**\
**[Final
Program[^?^](http://www.program-transformation.org/edit/GPCE06/PubGPCE06WebHomeGpceProgrampdf?topicparent=GPCE06.TutorialGPCE3)]{.twikiNewLink
style="background : #FFFFCE;"}(pdf)**\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Venue](ConferenceVenue){.twikiLink}\
[Registration](ConferenceRegistration){.twikiLink}

**[Tutorials](GpceTutorials){.twikiLink}**\
[GPCE1](TutorialGPCE1){.twikiLink} \|
[GPCE2](TutorialGPCE2){.twikiLink}\
[GPCE3](TutorialGPCE3){.twikiLink} \|
[GPCE4](TutorialGPCE4){.twikiLink}\
[GPCE5](TutorialGPCE5){.twikiLink} \|
[GPCE6](TutorialGPCE6){.twikiLink}\
[GPCE7](TutorialGPCE7){.twikiLink}\

**[Workshops](GpceWorkshops){.twikiLink}**\
[AOPLE](http://www.softeng.ox.ac.uk/aople/)\
[DSAL](http://dsal06.dcc.uchile.cl/)\
[STS](http://www.program-transformation.org/Sts/STS06)\
[GPCE4QoS](http://www.cis.uab.edu/gpce-qos/)

**Calls for**\
[Demos](CallForDemonstrations){.twikiLink}\
[Papers](CallForPapers){.twikiLink}\
[Tutorials](CallForTutorials){.twikiLink}\
[Workshops](CallForWorkshops){.twikiLink}

**[Electronic\
Submission](ElectronicSubmission){.twikiLink}**

**[Tutorials and\
Workshops](TutorialsAndWorkshops){.twikiLink}**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE06/TutorialGPCE3?t=1536827512)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE06/TutorialGPCE3)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE06/TutorialGPCE3)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE06/TutorialGPCE3?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE06/TutorialGPCE3?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/GPCE06/TutorialGPCE3?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/GPCE06/TutorialGPCE3?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/GPCE06/TutorialGPCE3?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE06/TutorialGPCE3)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE06/TutorialGPCE3?template=oopsmore&param1=1.2&param2=1.2)
:::
:::

::: {.flexMenu onmouseover="return showMenu(event, 102);" onmouseout="return hideMenu(event, 102);"}
Web

::: {#flexMenuContent102 .flexMenuContent}
-   [Recent
    Changes](http://www.program-transformation.org/GPCE06/WebChanges){.twikiLink}
-   [Notify Service](WebNotify){.twikiLink}
-   [News](WebNews){.twikiLink}

<!-- -->

-   [Page
    Index](http://www.program-transformation.org/GPCE06/WebIndex){.twikiLink}
-   [Search](WebSearch){.twikiLink}

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE06/TutorialGPCE3?template=oopsmore&param1=1.2&param2=1.2)
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
TutorialGPCE3 {#tutorialgpce3 .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

### []{#Using_Feature_Models_for_Product} Using Feature Models for Product Derivation

Danilo Beuche, pure-systems GmbH

Olaf Spinczyk, University Erlangen-Nuremberg

**Monday, Oct 23, from 08:30 to 12:00**

### []{#Abstract} Abstract

In general the implementation of a software product line leads to a high
degree of variability within the software architecture. For an effective
development and deployment it is necessary to resolve variation points
in architecture and source code automatically during product/variant
derivation. Given the complexity of most software systems tool support
is necessary for these tasks. This tutorial shows how feature models
combined with appropriate tools can provide this support. At first the
importance of the separation of problem space modeling and solution
space modelling is discussed. Concepts how to connect both spaces using
constraints and/or generative approaches are shown. Furthermore some
typical patterns of variability in the solution space are shown and
their automatic resolution in common languages like C/C++ and Java is
demonstrated. Integration of code generators, aspect-oriented
programming and software configuration management systems into the
derivation process is also discussed. The tutorial is accompanied by
short demonstrations of the presented concepts with freely available
tools (XVCL, pure::variants, OAW) and thereby gives attendees an idea
where to look when concepts are put into practice.

### []{#Level_Introductory_Intermediate} Level: Introductory/Intermediate

### []{#Required_Knowledge} Required Knowledge

Practitioners from Industry (SPL Novice to Intermediate) - attendees
should have a basic understanding software design, some knowledge about
software product lines in general is helpful.

### []{#Speaker_profiles} Speaker profiles

Olaf is Assistant Professor of Computer Science at Friedrich-Alexander
University Erlangen-Nuremberg, Germany. He is an experienced researcher
and tutorial presenter who works in the area of aspect-oriented software
product lines. His current research projects
[CiAO[^?^](http://www.program-transformation.org/edit/GPCE06/CiAO?topicparent=GPCE06.TutorialGPCE3)]{.twikiNewLink
style="background : #FFFFCE;"} and Fame-DBMS are targeting the domain of
embedded systems and exploit aspect-oriented and feature-oriented
programming languages.

Danilo is managing director of the pure-systems GmbH. He works as
consultant in the area of product line development mainly for client
from the automotive industry. He has been tutorial presenter, speaker,
workshop organizer and panellist at conferences such as AOSD, ISORC,
SPLC and OOPSLA.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
