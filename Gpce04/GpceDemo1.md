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
    Page](http://www.program-transformation.org/edit/Gpce04/GpceDemo1?t=1536827625)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gpce04/GpceDemo1)
-   [Attach
    File](http://www.program-transformation.org/attach/Gpce04/GpceDemo1)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gpce04/GpceDemo1?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gpce04/GpceDemo1?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Gpce04/GpceDemo1?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo1?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Gpce04/GpceDemo1?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo1?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Gpce04/GpceDemo1?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo1?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo1)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gpce04/GpceDemo1?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Gpce04/GpceDemo1?template=oopsmore&param1=1.4&param2=1.4)
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
[]{#GPCE_Demonstration_22_g3}[]{#GPCE_Demonstration_22_g3_} GPCE Demonstration 22
=================================================================================

[]{#Towards_Domain_Driven_Developmen} Towards Domain-Driven Development: the SmartTools Software Factory
--------------------------------------------------------------------------------------------------------

**Didier Parigot**, INRIA Sophia-Antipolis

### []{#Summary} Summary

Nowadays, software needs to be more open, flexible, and capable of
evolving quickly to meet new user or technology requirements. It should
be easy to adapt, even by none computer-specialists. To tackle these
challenges for DSL (Domain-Specific language) tools, we have developed a
software factory, named SmartTools.

One of the main ideas behind the design of SmartTools (and consequently
behind the design of the generated DSL tools) is to model the business
logic of each concern in a technology-free manner which can then be used
to generate platform-specific code. The following four concerns have
been taken into consideration:

-   The language data definition;
-   The semantics analysis frameworks that describe method signatures
    and traversal;
-   The graphical representation of the data;
-   And the component that links together all the tools of a DSL.

To offer open and adaptable tools, its design benefits from the
following paradigms:

-   Generative programming;
-   Aspect-Oriented Software Development (AOSD);
-   Component programming;
-   Model-Driven Architecture (MDA);
-   Standard technologies (XML) and patterns (such as the visitor design

SmartTools is heavily bootstrapped; that is, it internally uses its
technology to develop its own models. Through the development of these
models, our approach in integrating the mentioned paradigms and
technologies has been intensively tested and refined. Since then,
SmartTools has been used to produce tools for many diverse languages
such as SVG, DTD, XML scheme, CSS, WSDL, and BPEL.

The SmartTools framework represents approximately 100 000 lines of Java
source code before the generation stage and 1 000 000 lines after. This
ratio shows the efficiency of this approach and validates this new
development approach based on generative programming.

Before the demonstration, we will present the key features of
SmartTools. Then during the demonstration, we will focus on how to
define different tools for a DSL and show, for each concern, the
benefits gained from using the mentioned paradigms and technologies.
This demonstration is not only targeted at DSL tool developers, but also
at people who want to understand how these new paradigms can be
practically integrated into software.

### []{#Times_and_Locations} Times and Locations

-   Tue, 26 Oct., 10.30 - 11.15, Exhibition Hall Demo Room 4
-   Thu, 28 Oct., 11.30 - 12.15, Exhibition Hall Demo Room 4

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
