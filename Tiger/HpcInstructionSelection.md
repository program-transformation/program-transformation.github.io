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
    Page](http://www.program-transformation.org/edit/Tiger/HpcInstructionSelection?t=1536826697)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HpcInstructionSelection)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HpcInstructionSelection)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HpcInstructionSelection?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HpcInstructionSelection?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/HpcInstructionSelection?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HpcInstructionSelection)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HpcInstructionSelection?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/HpcInstructionSelection?template=oopsmore&param1=1.1&param2=1.1)
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
Hpc Instruction Selection {#hpc-instruction-selection .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

**Instruction Selection for the
[MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}**

This is the fourth set of [HpcExercises](HpcExercises){.twikiLink}. In
these exercises you build an instruction selector for IR programs that
produces
[MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}
code.

1.  Extend the set of overlays for
    [MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}
    with instructions needed to implement IR.

<!-- -->

1.  Define rules that cover all combinations of IR expressions

<!-- -->

1.  Define the instructions for implementing the view shift for changing
    control from caller to callee.

------------------------------------------------------------------------

**Notes**

1.  In order to construct a correct control-flow graph, all branching
    instructions need to have all possible labels they can branch to in
    their labels argument. This includes the label of the *next
    instruction* in case the instruction can fall through. Also be aware
    of the fact that jal returns to the next instruction.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
