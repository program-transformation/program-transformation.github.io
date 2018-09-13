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
    Page](http://www.program-transformation.org/edit/Transform/SORCERER?t=1536826336)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/SORCERER)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/SORCERER)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/SORCERER?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/SORCERER?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/SORCERER?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/SORCERER)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/SORCERER?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/SORCERER?template=oopsmore&param1=1.1&param2=1.1)
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
SORCERER {#sorcerer .twikiTopicTitle}
========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[SORCERER](SORCERER){.twikiLink} is the tree parser generator of
[ANTLR](ANTLR){.twikiLink}.

Papers

-   [TerenceParr](TerenceParr){.twikiLink}. *Language Translation Using
    [PCCTS](PCCTS){.twikiLink} and [CPP](CPP){.twikiLink}. A Reference
    Guide.* Automata Publishing Company, San Jose, Ca. 1993. Availble
    from <http://www.antlr.org/buybook.html>

<!-- -->

-   [TerenceParr](TerenceParr){.twikiLink}. *An Overview of
    [SORCERER](SORCERER){.twikiLink}: A Simple Tree-Parser Generator.*
    April, 1994. <http://www.antlr.org/papers/sorcerer.ps>

------------------------------------------------------------------------

**Review**

[SORCERER](SORCERER){.twikiLink} is the tree parser generator for the
[ANTLR](ANTLR){.twikiLink} language processing system.
[SORCERER](SORCERER){.twikiLink} generates tree walkers from tree
grammars. A tree grammar is a BNF like notation for the definition of
tree structures. For example, the grammar

    exp : #(PLUS exp exp)
        | INT

describes expression trees composed from integers and addition.

Tree translations and transformations are achieved by associating
actions with the grammar productions. Translations to textual output are
achieved by printing actions. For example, the following grammar prints
expressions using infix notation.

    exp : #(PLUS exp <<printf("+");>> exp)
        | i:INT <<printf("%d", i);>>

Tree transformations are achieved by reconstructing trees and returning
them as results. For example the following grammar transforms
expressions by swapping the arguments of the \\texttt{PLUS} operator.

    exp :! #(PLUS l:exp r:exp) <<#exp = #(PLUS r l);>>
        | INT

Grammar non-terminals can have arguments that can be used in the actions
in productions. Non-terminals can also return results. A tree grammar
gives rise to a set of mutually recursive functions, one for each
non-terminal, that together define a one-pass traversal over a tree.
Patterns can be nested and can use regular tree expressions with
optionals, alternatives and lists.

Transformation rules in tree grammars are embedded in grammar
productions. Separation of rules and strategies and generic tree
traversals are not supported in [SORCERER](SORCERER){.twikiLink}.

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
