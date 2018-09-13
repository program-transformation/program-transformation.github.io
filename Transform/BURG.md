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
    Page](http://www.program-transformation.org/edit/Transform/BURG?t=1536826316)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/BURG)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/BURG)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/BURG?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/BURG?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/BURG?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/BURG?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/BURG?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/BURG)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/BURG?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/BURG?template=oopsmore&param1=1.2&param2=1.2)
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
BURG {#burg .twikiTopicTitle}
====

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[BURG](BURG){.twikiLink} is a system for
[CodeGeneration](CodeGeneration){.twikiLink} from
[IntermediateRepresentation[^?^](http://www.program-transformation.org/edit/Transform/IntermediateRepresentation?topicparent=Transform.BURG)]{.twikiNewLink
style="background : #FFFFCE;"} expression trees developed by
[ChristopherFraser](ChristopherFraser){.twikiLink},
[ToddProebsting](ToddProebsting){.twikiLink} and others in the early
90\'s.

Papers

-   C. W. Fraser, D. R. Hanson, and T. A. Proebsting. Engineering a
    simple, efficient code-generator generator. *ACM Letters on
    Programming Languages and Systems*, 1(3):213\--226, September 1992.

<!-- -->

-   C. W. Fraser, R. R. Henry, and T. A. Proebsting.
    [BURG](BURG){.twikiLink}\-\--fast optimal instruction selection and
    tree parsing. *ACM [SIGPLAN](SIGPLAN){.twikiLink} Notices*,
    27(4):68\--76, April 1992.

<!-- -->

-   T. A. Proebsting. BURS automata generation. *ACM Transactions on
    Programming Languages and Systems*, 17(3):461\--486, May 1995.

------------------------------------------------------------------------

**Description**

[BURG](BURG){.twikiLink} is a system for code generation from
intermediate expression trees. A mapping from intermediate
representation trees to machine instruction is defined by means of a
tree grammar. A production of the form `n -> t (c)` defines a mapping of
tree pattern `t` to non-terminal `n` at cost `c`. Associated with each
production is an action to take when the production is selected. For
example, [ToddProebsting](ToddProebsting){.twikiLink} gives the
following example grammar:

      [1] goal -> reg            (0)  [5] reg  -> Plus(reg, reg) (2)
      [2] reg  -> Reg            (0)  [6] addr -> reg            (0)
      [3] reg  -> Int            (1)  [7] addr -> Int            (0)
      [4] reg  -> Fetch(addr)    (2)  [8] addr -> Plus(reg, Int) (0)

According to this grammar, the term `Fetch(Fetch(Plus(Reg,Int)))` has
two coverings corresponding to the derivations `4(4(6(5(2,3))))` and
`4(4(8(2)))`.

As illustrated by this example, more than one covering of a tree is
possible, corresponding to different ways to generate code. Each node
can have several different parses because of overlapping patterns and
chain rules. The costs associated with the productions express the cost
of executing the associated machine instruction. The goal of a code
generator is to find the lowest cost covering (i.e., lowest execution
time) of an intermediate representation expression tree.

According to bottom-up rewriting theory (BURS) an intermediate
representation tree can be translated to a sequence of instructions
using the following strategy. In a bottom-up traversal all lowest-cost
patterns that match each node are computed and associated with the node.
This involves matching the righ-hand sides of the productions to the
tree, taking into account earlier matches for sub-trees. Instructions
are then selected in a top-down traversal that is driven by the goal
non-terminal for the root of the tree.

This restricted form of rewriting can also be applied for simple type
inference problems, for checking tree formats, and for tree
simplifications.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 30 Apr 2001\

------------------------------------------------------------------------

[CategorySystem](CategorySystem){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
