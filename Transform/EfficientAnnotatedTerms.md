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
    Page](http://www.program-transformation.org/edit/Transform/EfficientAnnotatedTerms?t=1536826400)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/EfficientAnnotatedTerms)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/EfficientAnnotatedTerms)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/EfficientAnnotatedTerms?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/EfficientAnnotatedTerms?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/EfficientAnnotatedTerms?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/EfficientAnnotatedTerms?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/EfficientAnnotatedTerms?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/EfficientAnnotatedTerms?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/EfficientAnnotatedTerms?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/EfficientAnnotatedTerms)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/EfficientAnnotatedTerms?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/EfficientAnnotatedTerms?template=oopsmore&param1=1.3&param2=1.3)
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
Efficient Annotated Terms {#efficient-annotated-terms .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

M. G. J. van den Brand, H. A. de Jong, P. Klint, and P. A. Olivier.
Efficient Annotated Terms. *Software - Practice & Experience*,
30:259-291, 2000.

**Abstract**

How do distributed applications exchange tree-like data structures? We
introduce the abstract data type of *Annotated Terms* (*ATerms*) and
discuss their design, implementation and application. A comprehensive
procedural interface enables creation and manipulation of ATerms in C or
Java. The ATerm implementation is based on maximal subterm sharing and
automatic garbage collection. A binary exchange format for the concise
representation of ATerms (sharing preserved) allows the fast exchange of
ATerms between applications. In a typical application\--parse trees
which contain considerable redundant information\--less than 2 *bytes*
are needed to represent a node in memory, and less than 2 *bits* are
needed to represent it in binary format. The implementation of ATerms
scales up to the manipulation of ATerms in the giga-byte range.

Available:

-   Technical report:
    <http://www.cwi.nl/static/publications/reports/abs/SEN-R0003.html>
-   ATerm Library: <http://www.cwi.nl/projects/MetaEnv/aterm/>

See also

-   [ATerms[^?^](http://www.program-transformation.org/edit/Stratego/ATerms?topicparent=Transform.EfficientAnnotatedTerms)]{.twikiNewLink
    style="background : #FFFFCE;"} in Stratego
-   [ATermLibrary](../Tools/ATermLibrary){.twikiLink}

------------------------------------------------------------------------

[CategoryPaper](CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
