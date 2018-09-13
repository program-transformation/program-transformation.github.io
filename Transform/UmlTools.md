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
    Page](http://www.program-transformation.org/edit/Transform/UmlTools?t=1536826587)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/UmlTools)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/UmlTools)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/UmlTools?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/UmlTools?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/UmlTools?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/UmlTools?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/UmlTools?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/UmlTools?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/UmlTools?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/UmlTools)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/UmlTools?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/UmlTools?template=oopsmore&param1=1.3&param2=1.3)
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
Uml Tools {#uml-tools .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

There are many tools for editing [UML](UML){.twikiLink} diagrams. I
conducted a little comparison to find a good tool to use in a software
engineering course in the Spring of 2000. This page lists requirements
for good [UML](UML){.twikiLink} tools and reviews a number of existing
tools. Since I put the page up I have had some requests from tool
vendors to add a link to their tool. I have moved the page to the
program-transformation.org wiki such that anyone can add to this page.
Feel free to add more links and reviews by selecting the Edit link in
the sidebar. \-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 19 Nov
2001\

[]{#Requirements_for_UML_Tools} Requirements for [UML](UML){.twikiLink} Tools
-----------------------------------------------------------------------------

### []{#Functionality} Functionality

-   Diagram composition
    -   Completeness: How much of [UML](UML){.twikiLink} is supported?
    -   Can diagrams be layed out automatically? What is the quality of
        the automatic layout?
-   Code generation
    -   Is it possible to generate code from diagrams?
    -   Which languages are covered?
-   Reverse engineering
    -   Is it possible to generate diagrams from existing code?
    -   Which languages are covered? To what extent?
-   Round-trip engineering
    -   Is it possible to keep diagrams and code in sync?

### []{#Constraints} Constraints

-   Availability
    -   Price
    -   Student/academic edition
-   Performance
    -   Is drawing and manipulating diagrams realtime?
-   Open
    -   Can the tool be combined with other tools?
-   Open source
    -   Is it possible to improve and extend the tool?

[]{#Existing_Tools} Existing Tools
----------------------------------

There are numerous tools for creating and manipulating
[UML](UML){.twikiLink} diagrams. I have looked at a few of them

-   Rational Rose
    -   <http://www.rational.com>
    -   developed by the designers of [UML](UML){.twikiLink}
    -   not on Linux
    -   expensive license
-   Object Domain
    -   <http://www.objectdomain.com>
    -   implemented in Java (portable)
    -   supports round-trip engineering
    -   supports [HTML](HTML){.twikiLink} documentation generation
    -   affordable academic license (\$95)
-   [ArgoUML[^?^](http://www.program-transformation.org/edit/Transform/ArgoUML?topicparent=Transform.UmlTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   <http://argouml.tigris.org>
    -   open source (free)
    -   implemented in Java
    -   fast
    -   supports Java generation, but not reverse engineering
-   [TogetherSoft[^?^](http://www.program-transformation.org/edit/Transform/TogetherSoft?topicparent=Transform.UmlTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   <http://www.togethersoft.com>
    -   expensive full edition, free whiteboard edition (only supports
        class diagrams)
    -   implemented in Java
    -   supports instaneous synchronisation between model and code
-   Visual Paradigm for [UML](UML){.twikiLink}
    -   <http://www.visual-paradigm.com/vpuml.php>
    -   free community edition for non-commercial
    -   well-tested on Windows, Mac OS X, Linux, UNIX

The reviews above were conducted in the Spring of 2000 and might be out
of date.

There are a number of other tools that I haven\'t had time for to look
at:

-   Artisan
    -   <http://www.artisansw.com>
-   GDPro from Advanced Software Technologies Inc.
    -   <http://www.embarcadero.com>
-   Object Techology Workbench
    -   <http://www.otwsoftware.com>
-   [MinUML](MinUML){.twikiLink}
    -   <http://www.minuml.com>

------------------------------------------------------------------------

[CategorySystem](CategorySystem){.twikiLink} \| Contributions by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
