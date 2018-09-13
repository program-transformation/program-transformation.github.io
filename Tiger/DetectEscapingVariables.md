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
    Page](http://www.program-transformation.org/edit/Tiger/DetectEscapingVariables?t=1536826693)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/DetectEscapingVariables)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/DetectEscapingVariables)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/DetectEscapingVariables?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/DetectEscapingVariables?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/DetectEscapingVariables?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/DetectEscapingVariables)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/DetectEscapingVariables?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/DetectEscapingVariables?template=oopsmore&param1=1.1&param2=1.1)
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
Detect Escaping Variables {#detect-escaping-variables .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

The default escaping variables analysis is very conservative and makes
all variables escaping by annotating their declaration with `Stack(x)`.

In order for your compiler to produce good code is necessary to put as
many variables as possible into registers.

Extend module `Tiger-VarEscape.r` in directory `tas2ir/` in the
[TigerTrans](TigerTrans){.twikiLink} package to detect only really
escaping variables.

Sketch of the algorithm

-   In principle every variable is non-escaping, i.e., its name `x` in
    its declaration should be transformed into `Reg(x)`.

<!-- -->

-   If a variable is used inside a function that is different than the
    function it is declared in, the variable is escaping and its name
    `x` in its *declaration* should be transformed into `Stack(x)`.

The analysis can be very nicely expressed in a single traversal over the
program tree using dynamic rules.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 16 Nov 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
