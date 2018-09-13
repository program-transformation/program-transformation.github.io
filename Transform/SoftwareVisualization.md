::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/SoftwareVisualization?t=1536825741)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/SoftwareVisualization)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/SoftwareVisualization)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/SoftwareVisualization?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/SoftwareVisualization?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/SoftwareVisualization?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/SoftwareVisualization?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/SoftwareVisualization?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/SoftwareVisualization?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/SoftwareVisualization?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/SoftwareVisualization?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/SoftwareVisualization)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/SoftwareVisualization?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/SoftwareVisualization?template=oopsmore&param1=1.7&param2=1.7)
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
Software Visualization {#software-visualization .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The software visualization \[1\] group at
[GeorgiaTech](GeorgiaTech){.twikiLink} describes **software
visualization** as:

-   *the use of computer graphics and animation to help illustrate and
    present computer programs, processes, and algorithms. Software
    visualization systems can be used in teaching to help students
    understand how algorithms work, and they can be used in program
    development as a way to help programmers understand their code
    better.*

The MIT Press has published a book on the subject edited by Stasko *et
al.* called *Software visualization: programming as a multimedia
experience*, 1998.

------------------------------------------------------------------------

Claire Knight and Malcolm Munro from the
[ResearchInstituteInSoftwareEvolution](ResearchInstituteInSoftwareEvolution){.twikiLink}
provide a definition which emphasizes that visualization provides a view
that eliminates some of the overwhelming complexity of software systems:

-   *Software visualization is a discipline that makes use of various
    forms of imagery to provide insight and understanding and to
    **reduce complexity** of the existing system under consideration*
    (Proc. [IWPC](IWPC){.twikiLink}, 1999).

They also work on finding real life metaphors to use when visualizing
software. Their current metaphor is that of a *city*: districts are
classes, methods are buildings, dark buildings are private methods, etc.

------------------------------------------------------------------------

Steve Eick has done quite some work on visualizing large software
systems. He uses several clever tricks, one of which is to use
individual pixels (!) to represent a line of code, keeping the
indentation as it was in the original source text. Applied to several
millions of lines of C-code from Lucent\'s 5ESS phone switch. See:

-   Thomas A. Ball and Stephen G. Eick. *Software Visualization in the
    Large*. [IEEE](IEEE){.twikiLink} Computer, 29(4):33-43, 1996.
    <http://citeseer.nj.nec.com/ball96software.html>

------------------------------------------------------------------------

Lot\'s of software visualization is done through
[GraphVisualization[^?^](http://www.program-transformation.org/edit/Transform/GraphVisualization?topicparent=Transform.SoftwareVisualization)]{.twikiNewLink
style="background : #FFFFCE;"}, for example to represent call graphs,
control flow, data flow, and so on. A topic on its own \-- see
[GraphXML](GraphXML){.twikiLink},
[ExternalGraphTools](ExternalGraphTools){.twikiLink},
[DaVinciSystem](DaVinciSystem){.twikiLink}, \...

------------------------------------------------------------------------

A visualization technique developed for the purpose of
[ReverseEngineering](ReverseEngineering){.twikiLink} is
[SHriMP](SHriMP){.twikiLink} \-- Simple Hierarchical Multi-Perspective
views. The [SHriMP](SHriMP){.twikiLink} visualization technique uses a
nested-graph formalism, and a fisheye-view for manipulating large graphs
while providing context and preserving constraints such as orthogonality
and proximity. [SHriMP](SHriMP){.twikiLink} has been incorporated in the
[RigiSystem](RigiSystem){.twikiLink}. More info:

-   [PeggyStorey](PeggyStorey){.twikiLink},
    [HausiMueller](HausiMueller){.twikiLink} and
    [KennyWong](KennyWong){.twikiLink}. Manipulating and Documenting
    Software Structures. In P. Eades and K. Zhang, editors, Software
    Engineering and Knowledge Engineering, pp. 244-264. World
    Scientific, 1996. <http://www.csr.uvic.ca/~mstorey/papers/sprocl.ps>

------------------------------------------------------------------------

Visualization for object oriented systems is provided by
[CodeCrawler](CodeCrawler){.twikiLink}.

------------------------------------------------------------------------

Resources include

-   [VisSoft](VisSoft){.twikiLink} specifically on visualization of
    sfotware;
-   the [IEEE](IEEE){.twikiLink} conferences on information
    visualization, [IV](IV){.twikiLink} and
    [InfoVis](InfoVis){.twikiLink};
-   <http://www.softvis.org/>
-   Program understanding conferences such as [IWPC](IWPC){.twikiLink},
    [WCRE](WCRE){.twikiLink}, and [ICSM](ICSM){.twikiLink}.

------------------------------------------------------------------------

[CategoryProgramUnderstanding](CategoryProgramUnderstanding){.twikiLink}
\| Contributions by [ArieVanDeursen](ArieVanDeursen){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
