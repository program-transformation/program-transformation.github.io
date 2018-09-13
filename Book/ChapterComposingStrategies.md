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
    Page](http://www.program-transformation.org/edit/Book/ChapterComposingStrategies?t=1536829080)
-   [Rename
    Page](http://www.program-transformation.org/rename/Book/ChapterComposingStrategies)
-   [Attach
    File](http://www.program-transformation.org/attach/Book/ChapterComposingStrategies)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Book/ChapterComposingStrategies?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Book/ChapterComposingStrategies?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Book/ChapterComposingStrategies?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Book/ChapterComposingStrategies?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Book/ChapterComposingStrategies?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Book/ChapterComposingStrategies)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Book/ChapterComposingStrategies?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Book/ChapterComposingStrategies?template=oopsmore&param1=1.2&param2=1.2)
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
Chapter Composing Strategies {#chapter-composing-strategies .twikiTopicTitle}
============================

::: {.twikiWebTitle}
Strategies for Program Transformation
:::

\[ [Previous](ChapterInControlOfRewriting){.twikiLink} \|
[Up](PartIII){.twikiLink} \|
[Next](ChapterFirstClassPatternMatching){.twikiLink} \]

### []{#Introduction} Introduction

In the [previous chapter](ChapterInControlOfRewriting){.twikiLink} we
saw that pure term rewriting is not adequate for term rewriting because
of the lack of control over the application of rules. Approaches for
encoding such control within the pure rewriting paradigm lead to
functionalized control by means of extra rules and constructors at the
expense of traversal overhead and at the loss of the separation of rules
and strategies. We need a mechanism that provides such control, but
maintains the separation of rules and strategies and keeps traversal
overhead to a minimum. Such a mechanism should allow strategies
parameterized with selections from the available rules.

Also we saw that many transformation problems can be solved by
alternative strategies such as a one-pass bottom-up or top-down
traversal. Others can be solved by selecting the rules that are applied
in an innermost normalization, rather than all the rules in a
specification. However, no fixed set of such alternative strategies will
be sufficient for dealing with all transformation problems. Rather than
providing one or a few fixed rewriting strategies, we need to be able to
*compose* strategies from basic building blocks with a few fundamental
operators.

In program transformation, the basic building blocks are single rewrite
steps, for example defined by a rewrite rule. This chapter introduces a
set of operators for composing such single step transformations into
complex transformations. By allowing abstraction over the basic
transformation, *generic* transformation *strategies* can be defined.
The combinators discussed in this chapter cover sequential programming
and type-specific traversal. Extensions of this basic framework will be
considered in later chapters.

### []{#Preprint} Preprint

-   [Chapter-8.pdf](http://www.cs.uu.nl/~visser/book/Chapter-8.pdf)
-   [Chapter-8.ps](http://www.cs.uu.nl/~visser/book/Chapter-8.ps)

### []{#Remarks} Remarks

Lacks discussion of literature.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
