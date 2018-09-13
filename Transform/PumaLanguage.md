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
    Page](http://www.program-transformation.org/edit/Transform/PumaLanguage?t=1536826333)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/PumaLanguage)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/PumaLanguage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/PumaLanguage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/PumaLanguage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/PumaLanguage?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/PumaLanguage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/PumaLanguage?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/PumaLanguage?template=oopsmore&param1=1.1&param2=1.1)
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
Puma Language {#puma-language .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Description**

Puma \[Grosch91\] is the program transformation generator of the Coctail
compiler toolkit. A Puma specification specifies a transformation of an
abstract syntax tree that has been produced and attributed by some other
tool. The generator translates such a specification to a C or Modula-2
program that implements the transformation tool.

A specification defines a series of procedures (or functions or
predicates) that operate on one or more tree arguments. A procedure is
defined by one or more rules. A rule matches the arguments against
patterns, tests further properties of the arguments, computes some side
effects and computes the values of output arguments and the result. Each
of these computations can cause the failure of the rule upon which the
next rule is tried or the procedure fails if no more rules are
available.

Tree traversal is achieved by means of procedural recursion. All
traversals have to be defined explicitly. This means that there is no
higher-level support for finding application instances of transformation
rules nor are procedures higher-order, hence no generic traversals can
be described.

Puma is a typical example of a domain-specific language that provides
domain abstractions on top of an existing paradigm. The language
provides syntactic support for talking about trees, e.g., pattern
matching and attribute reference, and for dealing with computations that
can fail. These are features not usually provided in imperative
languages and that can be quite awkard to program. The result is a kind
of functional language for abstract syntax trees with some imperative
features.

**References**

-   Articles in [ResearchIndex](ResearchIndex){.twikiLink} \[1\]

**See Also**

Other [TransformationSystems](TransformationSystems){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
