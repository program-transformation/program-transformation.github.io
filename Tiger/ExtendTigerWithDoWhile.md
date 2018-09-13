::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![Stratego
logo](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)

------------------------------------------------------------------------

***Tiger in Stratego***

------------------------------------------------------------------------

**[WebHome](WebHome){.twikiLink}**\
[Tiger Compiler](TigerCompiler){.twikiLink}\
[Architecture](CompilerArchitecture){.twikiLink}\
[Packages](CompilerPackages){.twikiLink}\
[Components](CompilerComponent){.twikiLink}\
[Glossary](WebGlossary){.twikiLink}

[Download](DownloadAndInstallation){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tiger/ExtendTigerWithDoWhile?t=1536826691)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/ExtendTigerWithDoWhile)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/ExtendTigerWithDoWhile)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/ExtendTigerWithDoWhile?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/ExtendTigerWithDoWhile?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tiger/ExtendTigerWithDoWhile?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/ExtendTigerWithDoWhile?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tiger/ExtendTigerWithDoWhile?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/ExtendTigerWithDoWhile)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/ExtendTigerWithDoWhile?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tiger/ExtendTigerWithDoWhile?template=oopsmore&param1=1.2&param2=1.2)
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
Extend Tiger With Do While {#extend-tiger-with-do-while .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

Extend [TigerLanguage](TigerLanguage){.twikiLink} with a do-while
construct.

This requires updating the following components from the
[TigerFront](TigerFront){.twikiLink} package:

-   [TigerSyntax](http://www.program-transformation.org/Tiger/TigerSyntax){.twikiLink}
-   [TigerAbstractSyntax](http://www.program-transformation.org/Tiger/TigerAbstractSyntax){.twikiLink}
-   [TigerDesugar](http://www.program-transformation.org/Tiger/TigerDesugar){.twikiLink}
-   [TigerTypecheck](http://www.program-transformation.org/Tiger/TigerTypecheck){.twikiLink}
-   [TigerEval](http://www.program-transformation.org/Tiger/TigerEval){.twikiLink}

Note that the exercise is not difficult; the do-while construct is a
straightforward variation on the while-do construct. The point of this
assignment is to get an overview of the components of the
[TigerFront](TigerFront){.twikiLink} package and to refresh your
Stratego knowledge. See
[HowToInstallTheTigerCompiler](HowToInstallTheTigerCompiler){.twikiLink}
(note that you only need [TigerFront](TigerFront){.twikiLink} for now)
and [HowToTestTheTigerCompiler](HowToTestTheTigerCompiler){.twikiLink}.

The first step is to be able to parse do-while constructs. Take a look
at the `*.sdf` files in `syn/`. Decide on a concrete syntax (add a test
case to `xmpl/`!) and add it to the grammar.

There are two ways of implementing the new construct:

-   By eliminating it during desugaring (cf. `tas/Tiger-Desugar.r`)
-   By extending the typechecker (`tc/*.r`) and interpreter
    (`eval/Tiger-Eval.r`)

Implement both ways.

------------------------------------------------------------------------

[CategoryAssignment](CategoryAssignment){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
