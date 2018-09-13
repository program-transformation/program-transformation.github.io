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
    Page](http://www.program-transformation.org/edit/Tiger/HpcAnnouncements?t=1536826687)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HpcAnnouncements)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HpcAnnouncements)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HpcAnnouncements?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HpcAnnouncements?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/HpcAnnouncements?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HpcAnnouncements)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HpcAnnouncements?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/HpcAnnouncements?template=oopsmore&param1=1.1&param2=1.1)
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
Hpc Announcements {#hpc-announcements .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

**2000/10/10**

Tiger-0.9 is available. You can find it at
[WebHome](WebHome){.twikiLink}.

New in this version:

-   asm/Allocate-Registers is a complete implementation of register
    allocation with coalescing, provided the liveness analysis in
    asm/Liveness.r is implemented correctly.

<!-- -->

-   The file asm/runtime.s is Appel\'s port of the Tiger runtime system
    to the
    [MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}.

<!-- -->

-   The file asm/runtime-debug.s is my edition of the file in which I
    have commented out some initialization code that doesn\'t (seem to)
    work. Appel mentions that not all the code has been tested!

<!-- -->

-   In xmpl/makerules a new target has been added: make file.s to create
    the
    [MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}
    code for file.tig. It includes the code from file.ra and the code
    for the runtime system.

The code in file.s can be run using SPIM. See the SPIM manual for
instructions. (Basically: xspim -file file.s)

Notes:

-   The runtime system provides allocRecord instead of malloc. I suppose
    that is a change since my edition of the book.

<!-- -->

-   Functions in the runtime system don\'t take a static link as first
    parameter.

<!-- -->

-   Note that .text and .data sections need to bee aligned on (double?)
    word boundaries. It is a good idea to emit align(2) directives
    before the code of each STRING and PROC fragment.

**2000/09/06**

-   [WebHome](WebHome){.twikiLink} version 0.7 is available. New in this
    version are control-flow graph computation and liveness analysis for
    [ASM](ASM){.twikiLink} programs. The implementation of the data flow
    equations is left out as an exercise.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
