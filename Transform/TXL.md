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
    Page](http://www.program-transformation.org/edit/Transform/TXL?t=1536826338)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/TXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/TXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/TXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/TXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/TXL?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/TXL?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/TXL?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/TXL?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/TXL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/TXL?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/TXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/TXL?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/TXL?template=oopsmore&param1=1.4&param2=1.4)
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
TXL {#txl .twikiTopicTitle}
===

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#TXL_Tree_Transformation_Language} [TXL](TXL){.twikiLink}: Tree Transformation Language
------------------------------------------------------------------------------------------

**Homepage:** <http://www.txl.ca/>

The [TreeRewriting](TreeRewriting){.twikiLink} language
[TXL](TXL){.twikiLink} (developed by
[JamesCordy](JamesCordy){.twikiLink} at Queen\'s University in Kingston,
Canada) supports the definition of transformation rules on first-order
terms of a given context-free grammar. Rules not only specify a rewrite,
but also the strategy for applying it. Strategies are chosen from a
small set of implicit top-down search strategies augmented with explicit
scoped application of parameterized subrules in the style of a
first-order functional language.

[TXL](TXL){.twikiLink} is programming language and rapid prototyping
system specifically designed to support the specification and rapid
implementation of source analysis and transformation tasks of all kinds.
[TXL](TXL){.twikiLink} has been used to process over four and a half
billion lines of source code in commercial Year 2000 automated
maintenance systems, and provides the reverse engineering capabilities
of commercial software engineering systems such as Embarcadero
Describe(tm).

The [TXL](TXL){.twikiLink} language is a hybrid functional / rule-based
programming language with unification, implied iteration and deep
pattern match. Each [TXL](TXL){.twikiLink} program has two components:

-   A description of the structures to be transformed, specified as an
    EBNF grammar in ambiguous context-free form

<!-- -->

-   A rooted set of structural rewriting rules, specified by example
    using pattern/replacement pairs.

As a programming language [TXL](TXL){.twikiLink} is unique in that it is
has a pure functional superstructure that provides scoping, abstraction,
parameterization and recursion, over Prolog-like structural rewriting
rules providing pattern search, unification and implicit iteration. The
formal semantics and implementation of [TXL](TXL){.twikiLink} are based
on formal tree rewriting, but the trees are largely hidden from the user
due to the by-example style of rule specification.

------------------------------------------------------------------------

[CategorySystem](CategorySystem){.twikiLink} \|
[TransformationSystems](TransformationSystems){.twikiLink} \|
Contributions by [EelcoVisser](../Main/EelcoVisser){.twikiLink}
[JamesCordy](JamesCordy){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
