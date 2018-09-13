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
    Page](http://www.program-transformation.org/edit/Book/ChapterFirstClassPatternMatching?t=1536827725)
-   [Rename
    Page](http://www.program-transformation.org/rename/Book/ChapterFirstClassPatternMatching)
-   [Attach
    File](http://www.program-transformation.org/attach/Book/ChapterFirstClassPatternMatching)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Book/ChapterFirstClassPatternMatching?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Book/ChapterFirstClassPatternMatching?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Book/ChapterFirstClassPatternMatching?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Book/ChapterFirstClassPatternMatching?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Book/ChapterFirstClassPatternMatching?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Book/ChapterFirstClassPatternMatching?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Book/ChapterFirstClassPatternMatching?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Book/ChapterFirstClassPatternMatching)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Book/ChapterFirstClassPatternMatching?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Book/ChapterFirstClassPatternMatching?template=oopsmore&param1=1.3&param2=1.3)
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
Chapter First Class Pattern Matching {#chapter-first-class-pattern-matching .twikiTopicTitle}
====================================

::: {.twikiWebTitle}
Strategies for Program Transformation
:::

\[ [Previous](ChapterComposingStrategies){.twikiLink} \|
[Up](PartIII){.twikiLink} \|
[Next](ChapterGenericTraversalStrategies){.twikiLink} \]

### []{#Introduction} Introduction

So far we have assumed the basic actions applied by strategies are
rewrite rules. However, taking a closer look at rules, we see that they
are actually composed from several ingredients, i.e., matching the
pattern in the left-hand side, verifying the side conditions, and
instantiating the pattern on the right-hand side. In addition, a rule
implicitly delimits the scope of the variables that it uses. If we take
rules apart and make their components available as first-class strategy
actions, many interesting idioms can be expressed directly.

This chapter introduces the strategy actions match (?p), build (p), and
scope ({x1,\...,xn:s}), and shows how unconditional and conditional
rewrite rules can be expressed in terms of these actions. Many other
language constructs that involve matching can also be expressed in terms
of these operations.

### []{#Preprint} Preprint

-   [Chapter-9.pdf](http://www.cs.uu.nl/~visser/book/Chapter-9.pdf)
-   [Chapter-9.ps](http://www.cs.uu.nl/~visser/book/Chapter-9.ps)

### []{#Remarks} Remarks

-   Rule for explicit pattern matching is missing
-   Rule for term project should use where

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
