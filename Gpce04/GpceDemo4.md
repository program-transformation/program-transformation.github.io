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
    Page](http://www.program-transformation.org/edit/Gpce04/GpceDemo4?t=1536827625)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gpce04/GpceDemo4)
-   [Attach
    File](http://www.program-transformation.org/attach/Gpce04/GpceDemo4)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gpce04/GpceDemo4?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gpce04/GpceDemo4?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Gpce04/GpceDemo4?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo4?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Gpce04/GpceDemo4?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo4?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Gpce04/GpceDemo4?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo4?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gpce04/GpceDemo4)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gpce04/GpceDemo4?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Gpce04/GpceDemo4?template=oopsmore&param1=1.5&param2=1.5)
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
[]{#GPCE_Demonstration_21_g4}[]{#GPCE_Demonstration_21_g4_} GPCE Demonstration 21
=================================================================================

[]{#Xirc_Cross_Artifact_Information}[]{#Xirc_Cross_Artifact_Information_} Xirc: Cross-Artifact Information Retrieval
--------------------------------------------------------------------------------------------------------------------

**Michael Eichberg**, Darmstadt University of Technology\
**Thorsten Schaefer**, Darmstadt University of Technology

### []{#Summary} Summary

In large scale software development projects, in particular in the field
of Component-Based Software Development(CBSD), the kinds of a project\'s
sources are diverse and related information is spread over the different
artifacts. E.g., the transaction attributes (\"Required\",
\"Requires-New\",etc.) of methods of an Enterprise Java Bean are defined
in the deployment descriptor while the method bodies are defined in a
Java class.

If we want to put these information into relation, e.g., to find all
methods with a specific transaction attribute, we have to use multiple
search engines and have to map the information manually. It is not
possible to execute one query that returns the desired result.

To solve these problems we have developed XIRC, a tool and architecture
that enables to define queries over a uniform representation of all
artifacts of a software project. XIRC maps all artifacts of a project to
XML representations and stores the documents in a database. Then,
XQuery, a functional query language for XML documents (databases), can
be used to query the database. Hence, XIRC can be used as a
sophisticated search engine, as a tool to check implementation
restrictions, to find errors or as a basis for further tools for code
generation and visualization.

The first part of the demo will be a short PowerPoint presentation
introducing the XIRC architecture and its features. The second part will
be a live demo of the XIRC Eclipse Plug-in. This part will show how to
put information spread over (EJB-) deployment descriptors and code into
relation to ease the development of a component, to check implementation
restrictions or to find errors.

### []{#Times_and_Locations} Times and Locations

-   Wed, 27 Oct., 10.30 - 11.15, Exhibition Hall Demo Room 4
-   Thu, 28 Oct., 10.30 - 11.15, Exhibition Hall Demo Room 4

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
