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
    Page](http://www.program-transformation.org/edit/Transform/MultiLevelSpecifications?t=1536826212)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/MultiLevelSpecifications)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/MultiLevelSpecifications)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/MultiLevelSpecifications?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/MultiLevelSpecifications?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/MultiLevelSpecifications?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/MultiLevelSpecifications?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/MultiLevelSpecifications?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/MultiLevelSpecifications)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/MultiLevelSpecifications?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/MultiLevelSpecifications?template=oopsmore&param1=1.2&param2=1.2)
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
Multi Level Specifications {#multi-level-specifications .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[EelcoVisser](EelcoVisser){.twikiLink}. Multi-level specifications. In
[ArieVanDeursen](ArieVanDeursen){.twikiLink},
[JanHeering](JanHeering){.twikiLink}, and
[PaulKlint](PaulKlint){.twikiLink}, editors,
*[LanguagePrototyping](LanguagePrototyping){.twikiLink}. An Algebraic
Specification Approach* , volume 5 of *AMAST Series in Computing*, pages
105\--196. World Scientific, Singapore, September 1996.

**Abstract**

This chapter introduces a modular, applicative, multi-level equational
specification formalism that supports algebraic specification with
user-definable type constructors, polymorphic functions and higher-order
functions. Specifications consist of one or more levels numbered 0 to n.
Level 0 defines the object level terms. Level 1 defines the types used
in the signature of level 0. In general, the terms used as types in
level n are defined in level n+1. This setup makes the algebra of types
and the algebra of types of types, etc., user-definable. The applicative
term structure makes functions first-class citizens and facilitates
higher-order functions. The use of variables in terms used as types
provides polymorphism (including higher-order polymorphism, i.e.,
abstraction over type constructors). Functions and variables can be
overloaded. Specifications can be divided into modules. Modules can be
imported at several levels by means of a specification lifting
operation. Equations define the semantics of terms over a signature. The
formalism also allows equations over types, by means of which many type
systems can be described. The typechecker presented in this chapter does
not take into account type equations.

The specification, in [ASFandSDF](ASFandSDF){.twikiLink}, of the syntax,
type system and semantics of the formalism is presented in three stages:
(1) untyped equational specifications (2) applicative one-level
specifications (3) modular multi-level specifications. The definition of
a typechecker for stages (2) and (3) is divided into four parts: (a)
well-formedness judgements verifying type correctness of fully annotated
terms and specifications, (b) non well-formedness rules giving
descriptive error messages for the cases not covered under (a), (c) a
type assignment function annotating the terms in a plain specification
with types, and (d) a typechecking function which checks well-formedness
after applying type assignment. These functions are defined uniformly
for all levels of a specification.

Aside of defining a new specification formalism, this chapter
illustrates the use of [ASFandSDF](ASFandSDF){.twikiLink} for the design
and prototyping of sophisticated specification formalisms.

**Available**

-   <http://www.cs.uu.nl/people/visser/ftp/P9604.ps.gz>

------------------------------------------------------------------------

[CategoryPaper](CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
