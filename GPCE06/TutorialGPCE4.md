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
Program[^?^](http://www.program-transformation.org/edit/GPCE06/PubGPCE06WebHomeGpceProgrampdf?topicparent=GPCE06.TutorialGPCE4)]{.twikiNewLink
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
    Page](http://www.program-transformation.org/edit/GPCE06/TutorialGPCE4?t=1536827513)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE06/TutorialGPCE4)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE06/TutorialGPCE4)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE06/TutorialGPCE4?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE06/TutorialGPCE4?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/GPCE06/TutorialGPCE4?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/GPCE06/TutorialGPCE4?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/GPCE06/TutorialGPCE4?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/GPCE06/TutorialGPCE4?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/GPCE06/TutorialGPCE4?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE06/TutorialGPCE4)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE06/TutorialGPCE4?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/GPCE06/TutorialGPCE4?template=oopsmore&param1=1.3&param2=1.3)
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
TutorialGPCE4 {#tutorialgpce4 .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

### []{#Building_Java_Transformations_wi} Building Java Transformations with Stratego/XT

Martin Bravenboer, Utrecht University

Karl Trygve Kalleberg, University of Bergen

Eelco Visser, Utrecht University

**Monday, October 23rd, from 13:30 to 17:00**

### []{#Abstract} Abstract

This tutorial gives an overview of techniques for program
transformation, illustrated through the
[Stratego/XT](http://www.stratego-language.org) program transformation
system. We explain the general architecture of transformation systems,
and how Stratego/XT is used to assemble such systems from components. We
introduce a set of ready made components for Java transformation, and
show how to program custom transformation components using Stratego. In
particular, we show how to express local transformations using rewrite
rules and strategies and how context-sensitive transformations can be
expressed easily using dynamic rewrite rules. All techniques and
language features are illustrated with implementations of
transformations on Java programs, that show how to apply all introduced
techniques in practice.

### []{#Level_Introductory} Level: Introductory

### []{#Required_Knowledge} Required Knowledge

Basic understanding of compilers, parsing and program representation
using abstract syntax trees is an advantage, but we briefly summarize
the basics and ignore the technical details of parsing, since we focus
on application of program transformation to a particular programming
language, i.e. Java, for which all required parsing and pretty-print
support is already available.

### []{#Speaker_profiles} Speaker profiles

[Martin Bravenboer](http://www.cs.uu.nl/~martin) is a PhD student at
Utrecht University, researching language extensions and program
transformation.

[Karl Trygve Kalleberg](http://www.ii.uib.no/~karltk/) is a PhD student
at the University of Bergen, researching program transformation systems
and language extensions for program transformation.

[Eelco Visser](http://www.cs.uu.nl/~visser) is assistant professor at
Utrecht University, researching program transformation and software
configuration. He is the principal designer and developer of the
Stratego/XT program transformation system.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
