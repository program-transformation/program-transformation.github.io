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
    Page](http://www.program-transformation.org/edit/Transform/GraphModelingLanguage?t=1536826493)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/GraphModelingLanguage)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/GraphModelingLanguage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/GraphModelingLanguage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/GraphModelingLanguage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/GraphModelingLanguage?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/GraphModelingLanguage?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/GraphModelingLanguage?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/GraphModelingLanguage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/GraphModelingLanguage?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/GraphModelingLanguage?template=oopsmore&param1=1.2&param2=1.2)
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
Graph Modeling Language {#graph-modeling-language .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The Graph Modeling Language ([GML](GML){.twikiLink}) (which is used by
Graphlet) has a simple and orthogonal syntax. A [GML](GML){.twikiLink}
file consists of key-value pairs. Values can be integers, floats,
strings, and lists. Integers are restricted to 32 bit and floats are
double precision. A list consists of key-value pairs. Duplicate keys
within the same list are legal and it is guaranteed that the order of
these duplicates is preserved during reading and writing. This makes it
possible to represent array and list data structures.
[GML](GML){.twikiLink} has predefined keys like \'graph\', \'node\', and
\'edge\'. A graph is represented with the top-level key \'graph\', whose
value is a list that contains \'node\' and \'edge\' keys. Every node
must be given a unique integer id. The id is then used to represent
edges between two nodes. [GML](GML){.twikiLink} defines default values
for every data type. These defaults are then used for missing key-value
pairs. Keys unknown to [GML](GML){.twikiLink} are handled differently,
depending if the key is considered safe or unsafe. Unknown keys that are
safe are considered invariant to graph modification and hence are
ignored (i.e., written back unmodified). In contrast, unsafe keys are
deleted (i.e., not written back) if the tools cannot update them
properly. Safe and unsafe attributes are distinguished with the
following convention: Safe (unsafe) attributes start with a lower (an
upper) case letter.

The following gives a code example that contains two nodes (called
\'one\' and \'two\') that are connected with an edge. The edge is
colored red.

      graph [
       node [ id 1
          label "one" ]
       node [ id 2
          label "two" ]
       edge [ source 1
          target 2
          graphics [ fill "red" ]
        ]
      ]

(Quoted from
[ExchangeFormatBibliography](ExchangeFormatBibliography){.twikiLink})

The Graphlet home page is located at:

-   <http://www.infosun.fmi.uni-passau.de/Graphlet/>

The following page describes the [GML](GML){.twikiLink} format:

-   <http://www.infosun.fmi.uni-passau.de/Graphlet/GML/>
-   <http://infosun.fmi.uni-passau.de/Graphlet/GML/gml-tr.html>

\-- [HolgerKienle](HolgerKienle){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
