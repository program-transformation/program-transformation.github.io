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
    Page](http://www.program-transformation.org/edit/Book/ChapterGenericTraversalStrategies?t=1536826213)
-   [Rename
    Page](http://www.program-transformation.org/rename/Book/ChapterGenericTraversalStrategies)
-   [Attach
    File](http://www.program-transformation.org/attach/Book/ChapterGenericTraversalStrategies)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Book/ChapterGenericTraversalStrategies?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Book/ChapterGenericTraversalStrategies?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Book/ChapterGenericTraversalStrategies?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Book/ChapterGenericTraversalStrategies?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Book/ChapterGenericTraversalStrategies?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Book/ChapterGenericTraversalStrategies)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Book/ChapterGenericTraversalStrategies?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Book/ChapterGenericTraversalStrategies?template=oopsmore&param1=1.2&param2=1.2)
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
Chapter Generic Traversal Strategies {#chapter-generic-traversal-strategies .twikiTopicTitle}
====================================

::: {.twikiWebTitle}
Strategies for Program Transformation
:::

\[ [Previous](ChapterFirstClassPatternMatching){.twikiLink} \|
[Up](PartIII){.twikiLink} \|
[Next](ChapterScopedDynamicRewriteRules){.twikiLink} \]

### []{#Introduction} Introduction

In the previous chapters we saw how strategies can be used to control
transformations and how rules can be broken down into the primitive
actions match, build and scope. Together, these combinators allow us to
define any transformation. However, the definition of traversals using
congruence operators is specific for a data-type. Although a one step
traversal can be factored out of the definition of full tree traversals,
there are no generic definitions of traversals. This entails, that
traversals should be defined for each data type.

In this chapter we introduce combinators for *generic term traversal*,
that support data type independent definition of traversals, which can
be reused for any data type. Furthermore, the strategies that we have
inspected so far are geared to transform terms while preserving types,
i.e., *rephrasings* according to the taxonomy in [Chapter Program
Transformation](ChapterProgramTransformation){.twikiLink}. There is also
a class of transformations, in which terms are *translated* to a
different type. In this chapter we introduce a *generic term
construction and decomposition* operator, which allows us to define
generic translation or *type unifying* strategies.

### []{#Preprint} Preprint

-   [Chapter-10.pdf](http://www.cs.uu.nl/~visser/book/Chapter-10.pdf)
-   [Chapter-10.ps](http://www.cs.uu.nl/~visser/book/Chapter-10.ps)

### []{#Remarks} Remarks

Very draft\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
