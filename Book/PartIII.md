::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
::: {style="overflow:auto; height:1px; width:1px;"}
[incest porn](http://sexpace.net/)\
:::

------------------------------------------------------------------------

  -----------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextless-100px.png)](WebHome)
  -----------------------------------------------------------------------------

------------------------------------------------------------------------

**[Cover](WebHome){.twikiLink}**\
[Title page](TitlePage){.twikiLink}\
[About](AboutThisBook){.twikiLink}\
[Contents](TableOfContents){.twikiLink}\
[News](WebNews){.twikiLink}

**[Part I](PartI){.twikiLink}**

**[Part II](PartII){.twikiLink}**

**[Part III](PartIII){.twikiLink}**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Book/PartIII?t=1536827723)
-   [Rename
    Page](http://www.program-transformation.org/rename/Book/PartIII)
-   [Attach
    File](http://www.program-transformation.org/attach/Book/PartIII)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Book/PartIII?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Book/PartIII?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Book/PartIII?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Book/PartIII?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Book/PartIII?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Book/PartIII)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Book/PartIII?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Book/PartIII?template=oopsmore&param1=1.2&param2=1.2)
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
Part III {#part-iii .twikiTopicTitle}
========

::: {.twikiWebTitle}
Strategies for Program Transformation
:::

[]{#Programmable_Rewriting_Strategie} Programmable Rewriting Strategies
-----------------------------------------------------------------------

### []{#Contents} Contents

-   [Chapter In Control of
    Rewriting](ChapterInControlOfRewriting){.twikiLink}
-   [Chapter Composing
    Strategies](ChapterComposingStrategies){.twikiLink}
-   [Chapter First Class Pattern
    Matching](ChapterFirstClassPatternMatching){.twikiLink}
-   [Chapter Generic Traversal
    Strategies](ChapterGenericTraversalStrategies){.twikiLink}
-   [Chapter Scoped Dynamic Rewrite
    Rules](ChapterScopedDynamicRewriteRules){.twikiLink}

### []{#Introduction} Introduction

Rewrite rules provide a good formalism for expressing basic program
transformation steps. However, rewriting has a number of limitations.
First, since most sets of rules are not confluent and/or terminating,
exhaustive application of rules is not adequate; more careful control
over the application of rewrite rules is needed.

[Chapter In Control of
Rewriting](ChapterInControlOfRewriting){.twikiLink} surveys several
solutions to controlling rewriting. Most solutions for the encoding of
control suffer from a substantial overhead in the definition of
*traversals* and/or *intertwine transformation rules and strategy*. The
paradigm of *programmable rewriting strategies* provides a solution with
minimal overhead for traversal, while maintaining the separation of
rules and strategies.

[Chapter Composing Strategies](ChapterComposingStrategies){.twikiLink}
to [Chapter Generic Traversal
Strategies](ChapterGenericTraversalStrategies){.twikiLink} introduce
combinators for the composition of programmable strategies. [Chapter
Composing Strategies](ChapterComposingStrategies){.twikiLink} introduces
combinators for sequential non-deterministic programming and for data
type specific traversal using congruence operators. [Chapter First Class
Pattern Matching](ChapterFirstClassPatternMatching){.twikiLink} reduces
rewrite rules to the more primitive strategy actions *match*, *build*,
and *scope*. The availability of *first class patterns* allows many
other operations involving pattern matching. Data type specific
traversal with congruence operators does solve the separation between
rules and strategies, but not the overhead caused by the specification
of traversals. [Chapter Generic Traversal
Strategies](ChapterGenericTraversalStrategies){.twikiLink} shows how
combinators for *generic traversal* can concisely capture traversal
schemata independent of any object language.

Another limitation of rewriting is that rewrite rules are context-free.
That is, only local information available during the pattern match can
be used in a transformation step. In [Chapter Scoped Dynamic Rewrite
Rules](ChapterScopedDynamicRewriteRules){.twikiLink} the paradigm of
rewriting strategies is extended with *scoped dynamic rewrite rules*,
rules which are generated at run-time to inherit context information.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
