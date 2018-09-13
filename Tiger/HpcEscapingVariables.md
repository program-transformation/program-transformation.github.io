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
    Page](http://www.program-transformation.org/edit/Tiger/HpcEscapingVariables?t=1536826688)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HpcEscapingVariables)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HpcEscapingVariables)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HpcEscapingVariables?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HpcEscapingVariables?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/HpcEscapingVariables?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HpcEscapingVariables)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HpcEscapingVariables?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/HpcEscapingVariables?template=oopsmore&param1=1.1&param2=1.1)
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
Hpc Escaping Variables {#hpc-escaping-variables .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

**Escaping Variables**

This is the seventh set of [HpcExercises](HpcExercises){.twikiLink}.

The current implementation of [WebHome](WebHome){.twikiLink} stores all
formal and local variables in the stack frame, even if they might be
kept in registers.

Extend the compiler with escaping variables analysis such that variables
that are not needed by nested functions are stored in registers.

1.  Which components are affected by this extension?

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
