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
    Page](http://www.program-transformation.org/edit/Transform/OPTIMIX?t=1536826331)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/OPTIMIX)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/OPTIMIX)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/OPTIMIX?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/OPTIMIX?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/OPTIMIX?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/OPTIMIX)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/OPTIMIX?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/OPTIMIX?template=oopsmore&param1=1.1&param2=1.1)
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
OPTIMIX {#optimix .twikiTopicTitle}
=======

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Description**

[OPTIMIX](OPTIMIX){.twikiLink} is a specification language for the
specification of optimizers based on graph rewriting developed by
[UweAssman](UweAssman){.twikiLink} at the University of Karlsruhe \[3\].
A specification consists of a set of modules that each define a set of
rewrite systems that consist of a list of graph rewrite rules. A rule
matches a subgraph of the graph and adds or deletes edges and nodes. In
order to avoid non-termination and non-confluence a transformation is
defined in several separate rewrite systems that are then consecutively
applied.

Only a restricted set of rewrite systems is supported that can be
divided in two flavours. (1) Edge Addition Rewrite Systems (EARS)
consist only of rules that add edges. These are used for program
analysis; extra edges express relations between program nodes, e.g., is
a subexpression of. (2) General Graph Rewrite Systems are used to
express transformations. However, only those systems are supported that
can be proven to be terminating according to a termination check. This
boils down to systems that do not create new redexes after
transformation steps.

In effect, an [OPTIMIX](OPTIMIX){.twikiLink} rewrite system
specification appears to be an abstraction of a certain class of
while-programs that perform a loop over the program tree/graph finding
all applications of the rules and then applying the transformations
once.

A specification is translated to a C program in which each rewrite
system corresponds to a C function that performs a transformation. These
C functions have to be invoked from a C program that implements the rest
of the compiler. Data types are declared with a data definition language
([CoSy](CoSy){.twikiLink}-fSDL or AST from the Cocktail package).

The specification method is related to Datalog.

[OPTIMIX](OPTIMIX){.twikiLink} is an imperative specification language
in the sense that there is one tree/graph that is manipulated. Other
paradigms are usually functional, i.e., compute a new tree from an old
one.

**References**

-   Online articles on [OPTIMIX](OPTIMIX){.twikiLink} \[1\]
-   The [OPTIMIX](OPTIMIX){.twikiLink} homepage \[2\]

**See Also**

Other [TransformationSystems](TransformationSystems){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
