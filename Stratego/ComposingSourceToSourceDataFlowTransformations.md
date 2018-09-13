::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/ComposingSourceToSourceDataFlowTransformations?t=1536825426)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ComposingSourceToSourceDataFlowTransformations)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ComposingSourceToSourceDataFlowTransformations)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ComposingSourceToSourceDataFlowTransformations?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ComposingSourceToSourceDataFlowTransformations?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ComposingSourceToSourceDataFlowTransformations?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ComposingSourceToSourceDataFlowTransformations?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ComposingSourceToSourceDataFlowTransformations?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ComposingSourceToSourceDataFlowTransformations?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ComposingSourceToSourceDataFlowTransformations?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ComposingSourceToSourceDataFlowTransformations)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ComposingSourceToSourceDataFlowTransformations?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/ComposingSourceToSourceDataFlowTransformations?template=oopsmore&param1=1.3&param2=1.3)
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
K. Olmos and E. Visser. **Composing Source-to-Source Data-Flow
Transformations with Rewriting Strategies and Dependent Dynamic Rewrite
Rules.** In R. Bodik, editor, 14th International Conference on Compiler
Construction (CC\'05), volume 3443 of Lecture Notes in Computer Science,
pages 204\--220. Springer-Verlag, April 2005.
([techrep](http://www.cs.uu.nl/research/techreps/UU-CS-2005-006.html))

### []{#Abstract} Abstract

Data-flow transformations used in optimizing compilers are also useful
in other programming tools such as code generators, aspect weavers,
domain- and application-specific optimizers, and refactoring tools.
These applications require source-to-source transformations rather than
transformations on a low-level intermediate representation.

In this paper we describe the composition of source-to-source data-flow
transformations in the program transformation language Stratego. The
language supports the high-level specification of transformations by
means of rewriting strategy combinators that allow a natural modeling of
data- and control-flow without committing to a specific source language.
Data-flow facts are propagated using dynamic rewriting rules. In
particular, we introduce the concept of dependent dynamic rewrite rules,
for modeling the dependencies of data-flow facts on program entitities
such as variables. The approach supports the combination of analysis and
transformation, the combination of multiple transformations, the
combination with other types of transformations, and the correct
treatment of variable binding constructs and lexical scope to avoid
variable capture.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
