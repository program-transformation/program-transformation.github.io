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
Program[^?^](http://www.program-transformation.org/edit/GPCE06/PubGPCE06WebHomeGpceProgrampdf?topicparent=GPCE06.TutorialGPCE6)]{.twikiNewLink
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
    Page](http://www.program-transformation.org/edit/GPCE06/TutorialGPCE6?t=1536827513)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE06/TutorialGPCE6)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE06/TutorialGPCE6)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE06/TutorialGPCE6?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE06/TutorialGPCE6?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/GPCE06/TutorialGPCE6?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/GPCE06/TutorialGPCE6?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/GPCE06/TutorialGPCE6?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE06/TutorialGPCE6)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE06/TutorialGPCE6?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/GPCE06/TutorialGPCE6?template=oopsmore&param1=1.2&param2=1.2)
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
TutorialGPCE6 {#tutorialgpce6 .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

### []{#Feature_Modularity_in_Software_P} Feature Modularity in Software Product Lines

Don Batory, University of Texas at Austin

### []{#Date} Date

**Tuesday, Oct 24, from 13:30 to 17:00**

### []{#Abstract} Abstract

Feature Oriented Programming (FOP) is a design methodology and tools for
program synthesis in software product lines. Programs are specified
declaratively in terms of features. FOP has been used to develop
product-lines in widely varying domains, including compilers for
extensible Java dialects, fire support simulators for the U.S. Army,
network protocols, and program verification tools. The fundamental units
of modularization in FOP are program extensions (aspects, mixins, or
traits) that encapsulate the implementation of an individual feature. An
FOP model of a product-line is an algebra: base programs are constants
and program extensions are functions (that add a specified feature to an
input program). Program designs are expressions - compositions of
functions and constants - that are amenable to optimization and
analysis. This tutorial reviews core results on FOP: models and tools
for synthesizing code and non-code artefacts by feature module
composition, automatic algorithms for validating compositions, and the
relationship between product-lines, metaprogramming, and model driven
engineering (MDE).

### []{#Level_Introductory} Level: Introductory

### []{#Required_Knowledge} Required Knowledge

Basic concepts of object-orientation are assumed; no special background
is necessary.

### []{#Speaker_profile} Speaker profile

Don Batory holds the David Bruton Centennial Professorship at The
University of Texas at Austin. He is an Associate Editor of the Journal
of Aspect-Oriented Software Development and was an Associate Editor of
IEEE Transactions on Software Engineering (1999-2002).\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
