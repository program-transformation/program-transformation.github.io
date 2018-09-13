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
Program[^?^](http://www.program-transformation.org/edit/GPCE06/PubGPCE06WebHomeGpceProgrampdf?topicparent=GPCE06.TutorialGPCE2)]{.twikiNewLink
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
    Page](http://www.program-transformation.org/edit/GPCE06/TutorialGPCE2?t=1536827512)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE06/TutorialGPCE2)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE06/TutorialGPCE2)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE06/TutorialGPCE2?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE06/TutorialGPCE2?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/GPCE06/TutorialGPCE2?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/GPCE06/TutorialGPCE2?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/GPCE06/TutorialGPCE2?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE06/TutorialGPCE2)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE06/TutorialGPCE2?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/GPCE06/TutorialGPCE2?template=oopsmore&param1=1.2&param2=1.2)
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
TutorialGPCE2 {#tutorialgpce2 .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

### []{#Building_Domain_Specific_Languag} Building Domain Specific Languages with Eclipse and openArchitectureWare

Markus Völter, Independent Consultant

Arno Haase, Independent Software Architect

**Sunday, October 22nd, from 13:30 to 17:00**

### []{#Abstract} Abstract

DSLs are an important aspect of Model-Driven Software Development. Since
DSLs are specific to a certain domain, it is the domain architect\'s
task to define and implement DSLs so that application developers can use
the DSLs to configure or otherwise describe systems. In this tutorial,
participants will learn how to:

\* Define metamodels that form the basis for a DSL \* Define a graphical
syntax for the DSL \* Verify the correctness of models wrt. to the
metamodel that underlies them \* Write transformations that transform
models into executable code

To do all this, we will use tools and technologies from the Eclipse
platform. These include EMF for metamodelling, GMF for building
graphical editors as well as openArchitectureWare for verifying and
transforming models, and to generate code. The focus will be on the
graphical editor and code generation. The tutorial will be highly
interactive with only a minimum of slides, many live presentations show
the tools at work.

### []{#Level_Intermediate} Level: Intermediate

### []{#Required_Knowledge} Required Knowledge

Attendees must have a solid understanding of object-orientation and
architectural concepts as well as working knowledge of Java. A basic
understanding of Model-Driven Software Development is helpful. Working
knowledge in the use of Eclipse is very useful (since all our tooling
will be based on Eclipse).

### []{#Speaker_profiles} Speaker profiles

Markus works as a consultant for software technology and engineering. He
focuses on software architecture, middleware and model-driven
development. Markus is the co-author of several books on these topics.
He is a regular speaker at conferences.

Arno works as an independent software architect. He has been working in
the industry for fifteen years. During the last years, he has
specialized in introducing model-driven approaches both at the project
and the organization level.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
