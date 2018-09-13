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
    Page](http://www.program-transformation.org/edit/Gpce04/GpceDemo5?t=1536827625)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gpce04/GpceDemo5)
-   [Attach
    File](http://www.program-transformation.org/attach/Gpce04/GpceDemo5)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gpce04/GpceDemo5?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gpce04/GpceDemo5?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Gpce04/GpceDemo5?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo5?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Gpce04/GpceDemo5?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo5?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Gpce04/GpceDemo5?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo5?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo5)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gpce04/GpceDemo5?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Gpce04/GpceDemo5?template=oopsmore&param1=1.4&param2=1.4)
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
[]{#GPCE_OOPSLA_Demonstration_15_4}[]{#GPCE_OOPSLA_Demonstration_15_4_} GPCE/OOPSLA Demonstration 15
====================================================================================================

[]{#C_SAW_and_GenAWeave_A_Two_Level}[]{#C_SAW_and_GenAWeave_A_Two_Level_} C-SAW and GenAWeave: A Two-Level Aspect Weaving Toolsuite
-----------------------------------------------------------------------------------------------------------------------------------

**Jeff Gray**, University of Alabama at Birmingham\
**Ira Baxter**, Semantic Designs\
**Jing Zhang**, University of Alabama at Birmingham\
**Suman Roychoudhury**, University of Alabama at Birmingham

### []{#Summary} Summary

The C-SAW and GenAWeave tools support evolution of object-oriented
legacy software through a two-level approach using aspects. The
principle strategy of these tools is to generate low-level
transformation rules from higher-level domain languages. The generated
transformation rules, along with the initial version of the application
source code, serve as input to the Design Maintenance System (DMS) from
Semantic Designs. The generated rules drive the transformation process
in order to produce a modified version of the source containing new
concerns that have been woven across the application code base. The
demonstration will show the ability to make rapid adaptations to a large
cross-section of an application through simple specification changes at
a high-level of abstraction.

As case studies, the demonstration will highlight the transformation of
two legacy commercial applications: a large mission-computing avionics
framework written in C++, and a client-server enterprise management
system implemented in Object Pascal. In the avionics application,
transformation rules are generated from domain-specific models created
in the Generic Modeling Environment (from Vanderbilt University). Using
C-SAW, it will be shown that small changes in a representative model can
regulate concurrency and logging policies across many C++ classes. The
Object Pascal portion of the demonstration will illustrate the use of
DMS as the underlying engine for an aspect weaver. A unique feature of
the demonstration is the ability to weave aspects into various legacy
languages (not just Java) at the source level using GenAWeave.

### []{#Times_and_Locations} Times and Locations

-   Tue, 26 Oct., 11.30 - 12.15, Exhibition Hall Demo Room 2
-   Thu, 28 Oct., 12.30 - 13.15, Exhibition Hall Demo Room 3

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
