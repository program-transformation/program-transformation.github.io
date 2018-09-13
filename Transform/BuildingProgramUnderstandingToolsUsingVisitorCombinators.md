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
    Page](http://www.program-transformation.org/edit/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators?t=1536826399)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators?template=oopsmore&param1=1.2&param2=1.2)
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
Building Program Understanding Tools Using Visitor Combinators {#building-program-understanding-tools-using-visitor-combinators .twikiTopicTitle}
==============================================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

*Building Program Understanding Tools Using Visitor Combinators*

by [ArieVanDeursen](ArieVanDeursen){.twikiLink} and
[JoostVisser](JoostVisser){.twikiLink}

This paper describes how
[VisitorCombinators](VisitorCombinators){.twikiLink}, as supported by
[JJForester](../Tools/JJForester){.twikiLink} and
[JJTraveler](../Tools/JJTraveler){.twikiLink}, have been used in the
implementation of the program comprehension tool
[ControlCruiser[^?^](http://www.program-transformation.org/edit/Tools/ControlCruiser?topicparent=Transform.BuildingProgramUnderstandingToolsUsingVisitorCombinators)]{.twikiNewLink
style="background : #FFFFCE;"}. This tool performs *procedure
reconstruction* to derive *conditional call graphs* for Cobol programs.

See:

-   <http://www.cwi.nl/~jvisser/papers/ControlCruiser.ps>
-   <http://www.cwi.nl/~jvisser/papers/ControlCruiser.pdf>

**Abstract**

Program understanding tools manipulate program representations, such as
abstract syntax trees, control-flow graphs, or data-flow graphs. This
paper deals with the use of *VisitorCombinators* to conduct such
manipulations. Visitor combinators are an extension of the well-known
visitor design pattern. They are small, reusable classes that carry out
specific visiting steps. They can be composed in different
constellations to build more complex visitors. We evaluate the
expressiveness, reusability, ease of development, and applicability of
visitor combinators to the construction of program understanding tools.
To that end, we conduct a case study in the use of visitor combinators
for control flow analysis and visualization as used in a commercial
Cobol program understanding tool.

**See also**

[VisitorCombinationAndTraversalControl](VisitorCombinationAndTraversalControl){.twikiLink}

[CategoryAnalysis](CategoryAnalysis){.twikiLink},
[CategoryPaper](CategoryPaper){.twikiLink},
[CategoryProgramUnderstanding](CategoryProgramUnderstanding){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.BuildingProgramUnderstandingToolsUsingVisitorCombinators
moved from
Tools.BuildingProgramUnderstandingToolsUsingVisitorCombinators on 21 Feb
2002 - 14:10 by [JoostVisser](../Main/JoostVisser){.twikiLink}* - [put
it
back](http://www.program-transformation.org/rename/Transform/BuildingProgramUnderstandingToolsUsingVisitorCombinators?newweb=Tools&newtopic=BuildingProgramUnderstandingToolsUsingVisitorCombinators&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
