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
    Page](http://www.program-transformation.org/edit/Transform/DotLanguage?t=1536825771)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DotLanguage)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DotLanguage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DotLanguage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DotLanguage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/DotLanguage?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DotLanguage?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DotLanguage?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DotLanguage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DotLanguage?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/DotLanguage?template=oopsmore&param1=1.2&param2=1.2)
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
Dot Language {#dot-language .twikiTopicTitle}
============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Dot and neato are two graph layout tools that share an almost identical
graph format. Dot makes layouts of directed graphs whereas neato is for
undirected graphs. The format has three kinds of items: graphs, nodes,
and edges. The top-level graph can be structured by introducing
subgraphs, which define a subset of nodes and edges. Nodes are
identified by their name. Edges are created when nodes are joined with
an edge operator. Graphs, nodes, and edges can be attributed. Attributes
are name-value pairs of character strings. It is also possible to define
new default values for edge and node attributes (this can be seen as a
primitive form of attribute inheritance). The format has a large number
of predefined attributes (e.g., node shape, line style, color, and
layout parameters such as weights). Application specific attributes,
which are ignored by dot, can be attached as well.

The following gives a code example that contains two nodes (called
\'one\' and \'two\') that are connected with an edge. The edge is
colored red.

      digraph G {
        one -> two [ color= red ]
      }

(Quoted from
[ExchangeFormatBibliography](ExchangeFormatBibliography){.twikiLink})

Resources:

-   <http://www.research.att.com/sw/tools/graphviz/>

------------------------------------------------------------------------

[CategoryDataFormat](CategoryDataFormat){.twikiLink} \| Contributions by
[HolgerKienle](HolgerKienle){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
