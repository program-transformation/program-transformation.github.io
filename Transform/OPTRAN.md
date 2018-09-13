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
    Page](http://www.program-transformation.org/edit/Transform/OPTRAN?t=1536826331)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/OPTRAN)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/OPTRAN)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/OPTRAN?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/OPTRAN?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/OPTRAN?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/OPTRAN)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/OPTRAN?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/OPTRAN?template=oopsmore&param1=1.1&param2=1.1)
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
OPTRAN {#optran .twikiTopicTitle}
======

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Description**

[OPTRAN](OPTRAN){.twikiLink} \[LMW88\] is a specification language for
attributed tree transformation written by Reinhard Wilhelm at the
University of Saarlandes in the early 1980\'s.

A *transformation unit* consists of a tree grammar specifying the
abstract syntax of the language, semantic rules that specify attribute
dependencies and transformation rules. Transformation rules correspond
to simple rewrite rules that are extended such that application can
depend on attribute values and such that attribute values can be changed
as part of a transformation. A few simple strategies (bottom-up,
top-down, left-to-right, right-to-left) are available to control
application of rules. Furthermore, some heuristics are used to resolve
remaining ambiguities (e.g., use most specific rule or use textual order
of rules). Patterns in transformation rules are static (no contexts) and
linear. Attributes are reevaluated after a transformation rule is
applied.

The language is implemented in Pascal and specifications are also
specified using Pascal. The paper \[LMW88\] discusses the disadvantages
of such an embedding of a [DSL](DSL){.twikiLink} in a general-purpose
language and remarks that a functional language would solve several of
the problems of this embedding.

**References**

**See Also**

Other [TransformationSystems](TransformationSystems){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
