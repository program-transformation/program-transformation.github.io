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
    Page](http://www.program-transformation.org/edit/Transform/GraphDescriptionLanguage?t=1536826492)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/GraphDescriptionLanguage)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/GraphDescriptionLanguage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/GraphDescriptionLanguage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/GraphDescriptionLanguage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/GraphDescriptionLanguage?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/GraphDescriptionLanguage?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/GraphDescriptionLanguage?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/GraphDescriptionLanguage?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/GraphDescriptionLanguage?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/GraphDescriptionLanguage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/GraphDescriptionLanguage?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/GraphDescriptionLanguage?template=oopsmore&param1=1.3&param2=1.3)
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
Graph Description Language {#graph-description-language .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The Graph Description Language ([GDL](GDL){.twikiLink}) of the VCG tool
and its successor aiSee describes graphs in terms of nodes, edges,
subgraphs and their attributes. The [GDL](GDL){.twikiLink} syntax
supports special kinds of edges (e.g., nearedge) that control the graph
layout. Attributes are key-value pairs. Default attributes and
redefinition of default attributes for edges, nodes, and subgraphs are
supported as well. Nodes are identified with an obligatory title
attribute. Edges must have source and target attributes that refer to
the nodes\' titles. [GDL](GDL){.twikiLink} has a very rich set of
predefined attributes. The core of [GDL](GDL){.twikiLink} is compatible
to GRL, the specification language of the Edge graph editor.

The following gives a code example that contains two nodes (called \'a\'
and \'b\') that are connected with an edge. The edge is colored red.

     graph: {
      node: { title:  "a" }
      node: { title:  "b" }
      edge: { source: "a" target: "b" color: red }
            }

Resources:

-   [GDL](GDL){.twikiLink} in a Nutshell:
    <http://www.absint.com/aisee/gdl/guide/index.htm>
-   VCG Graph Layout Tool:
    <http://rw4.cs.uni-sb.de/users/sander/html/gsvcg1.html>
-   aiSee Graph Visualization Software: <http://www.aisee.com>
-   Citations: <http://citeseer.nj.nec.com/context/316931/0>

\-- [TWikiGuest](../Main/TWikiGuest){.twikiLink} - 10 Oct 2001\

------------------------------------------------------------------------

What is the relationship
[GDLVersusGXL[^?^](http://www.program-transformation.org/edit/Transform/GDLVersusGXL?topicparent=Transform.GraphDescriptionLanguage)]{.twikiNewLink
style="background : #FFFFCE;"}?\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
