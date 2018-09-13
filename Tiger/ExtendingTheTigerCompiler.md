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
    Page](http://www.program-transformation.org/edit/Tiger/ExtendingTheTigerCompiler?t=1536825756)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/ExtendingTheTigerCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/ExtendingTheTigerCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/ExtendingTheTigerCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/ExtendingTheTigerCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tiger/ExtendingTheTigerCompiler?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/ExtendingTheTigerCompiler?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tiger/ExtendingTheTigerCompiler?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/ExtendingTheTigerCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/ExtendingTheTigerCompiler?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tiger/ExtendingTheTigerCompiler?template=oopsmore&param1=1.2&param2=1.2)
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
Extending The Tiger Compiler {#extending-the-tiger-compiler .twikiTopicTitle}
============================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

The [Tiger compiler](TigerCompiler){.twikiLink} can easily be extended
since it is component-based. Adding a new optimization phase, extending
the syntax of the language, or replacing the back-end, is a matter of
creating a new component and constructing a new compilation pipeline.
This page lists some ideas for extensions.

Language extensions

-   Add a module system and separate compilation
-   Function arguments (escaping functions)
-   Objects
-   Add support for XML \-- the [TigerXML](TigerXML){.twikiLink} package
    is a first stab

Compiler improvements

-   Garbage collection
-   Target different platforms (e.g. Intel)
-   Improve spilling heuristics in the register allocator
-   Improve stack allocation of escaping variables (overlap variables
    that are not live at the same time)
-   Allocate non-escaping records and arrays on the stack
-   Optimization \-- first experiments in the
    [TigerOpt](TigerOpt){.twikiLink} package
    -   Add data-flow optimizations
    -   Add loop optimizations
    -   Inline functions
    -   Partial evaluation / specialization
-   Parallel execution

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 15 Sep 2002\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tiger.ExtendingTheTigerCompiler moved from
Tiger.HowToExtendTheTigerCompiler on 15 Sep 2002 - 18:55 by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tiger/ExtendingTheTigerCompiler?newweb=Tiger&newtopic=HowToExtendTheTigerCompiler&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
