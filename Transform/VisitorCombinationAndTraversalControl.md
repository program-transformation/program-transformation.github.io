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
    Page](http://www.program-transformation.org/edit/Transform/VisitorCombinationAndTraversalControl?t=1536826591)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/VisitorCombinationAndTraversalControl)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/VisitorCombinationAndTraversalControl)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/VisitorCombinationAndTraversalControl?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/VisitorCombinationAndTraversalControl?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/VisitorCombinationAndTraversalControl?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/VisitorCombinationAndTraversalControl?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/VisitorCombinationAndTraversalControl?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/VisitorCombinationAndTraversalControl?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/VisitorCombinationAndTraversalControl?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/VisitorCombinationAndTraversalControl)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/VisitorCombinationAndTraversalControl?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/VisitorCombinationAndTraversalControl?template=oopsmore&param1=1.3&param2=1.3)
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
Visitor Combination And Traversal Control {#visitor-combination-and-traversal-control .twikiTopicTitle}
=========================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

*Visitor Combination and Traversal Control*

by [JoostVisser](JoostVisser){.twikiLink}

This paper describes
[VisitorCombinators](VisitorCombinators){.twikiLink}. These are
implementations of the Visitor interface that can be used to *compose*
new visitors from given ones. The paper also describes the generic
visitor combinator framework Tools.JJTraveler, and the visitor generator
Tools.JJForester, which supports instantation of this framework for a
given grammar.

See:

-   <http://www.cwi.nl/~jvisser/papers/VisitorCombinationAndTraversalControl.pdf>
-   <http://www.cwi.nl/~jvisser/papers/VisitorCombinationAndTraversalControl.ps>

**Abstract**

The Visitor design pattern allows the encapsulation of polymorphic
behavior outside the class hierarchy on which it operates. A common
application of Visitor is the encapsulation of tree traversals.
Unfortunately, visitors resist composition and allow little traversal
control.

To remove these limitations, we introduce visitor combinators. These are
implementations of the visitor interface that can be used to compose new
visitors from given ones. The set of combinators we propose includes
traversal combinators that can be used to obtain full traversal control.

A clean separation can be made between the generic parts of the
combinator set and the parts that are speci c to a particular class
hierarchy. The generic parts form a reusable framework. The specific
parts can be generated from a (tree) grammar. Due to this separation,
programming with visitor combinators becomes a form of generic
programming with significant reuse of (visitor) code.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
