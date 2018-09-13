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
    Page](http://www.program-transformation.org/edit/Tiger/HowToTestTheTigerCompiler?t=1536825756)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HowToTestTheTigerCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HowToTestTheTigerCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HowToTestTheTigerCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HowToTestTheTigerCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tiger/HowToTestTheTigerCompiler?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/HowToTestTheTigerCompiler?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tiger/HowToTestTheTigerCompiler?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HowToTestTheTigerCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HowToTestTheTigerCompiler?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tiger/HowToTestTheTigerCompiler?template=oopsmore&param1=1.2&param2=1.2)
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
How To Test The Tiger Compiler {#how-to-test-the-tiger-compiler .twikiTopicTitle}
==============================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

There are a bunch of test cases in the `xmpl` subdirectory of the
[TigerXmpl](TigerXmpl){.twikiLink} package. After you have built the
[TigerCompiler](TigerCompiler){.twikiLink} or just some of its
[CompilerPackages](CompilerPackages){.twikiLink}, you can automatically
test them using various `make` targets.

For example, there is a test case called `queens.tig` that computes the
solutions to the Eight Queens Problem. Running `make queens.tas` will
parse and desugar it into `queens.tas`, `make queens.tc.tas` will
typecheck it, etc.

The targets include:

-   `filename.tasfix` (from `filename.tig`) - the full parse tree
    (concrete syntax)
-   `filename.sweettas` (from `filename.tasfix`) - the imploded parse
    tree (abstract syntax)
-   `filename.tas` (from `filename.sweettas`) - the desugared abstract
    syntax
-   `filename.tas.check` (from `filename.tas`) - checks the validity of
    abstract syntax trees
-   `filename.tc.tas` (from `filename.tas`) - the abstract syntax
    annotated with type information; fails in case of a type error
-   `filename.tc.tas.tccheck` (from `filename.tas`) - checks the
    validity of type annotated abstract syntax trees
-   `filename.val.tas` (from `filename.tas` and `filename.input`) -
    interprets a desugared Tiger program, with `filename.input` as input
-   `filename.flattas` (from `filename.tas`) - resugared abstract syntax
-   `filename.abox` (from `filename.flattas`) - intermediate step for
    pretty-printing
-   `filename.txt` (from `filename.abox`) - pretty-printed Tiger code
    (i.e., translates abstract syntax back to concrete syntax)

Also see the [CompilerArchitecture](CompilerArchitecture){.twikiLink}
for a picture of how these file types relate to each other and what
programs are involved in producing them.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
