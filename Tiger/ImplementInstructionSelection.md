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
    Page](http://www.program-transformation.org/edit/Tiger/ImplementInstructionSelection?t=1536826695)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/ImplementInstructionSelection)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/ImplementInstructionSelection)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/ImplementInstructionSelection?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/ImplementInstructionSelection?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Tiger/ImplementInstructionSelection?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tiger/ImplementInstructionSelection?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tiger/ImplementInstructionSelection?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/ImplementInstructionSelection?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tiger/ImplementInstructionSelection?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/ImplementInstructionSelection)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/ImplementInstructionSelection?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Tiger/ImplementInstructionSelection?template=oopsmore&param1=1.3&param2=1.3)
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
Implement Instruction Selection {#implement-instruction-selection .twikiTopicTitle}
===============================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

### []{#Instruction_Selection_for_the_MI}[]{#_Instruction_Selection_for_the_M} [Instruction Selection](InstructionSelection){.twikiLink} for the [MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}

Build an instruction selector
[IR2ASM](http://www.program-transformation.org/Tiger/IR2ASM){.twikiLink}
for programs in [intermediate
representation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
that produces
[MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}
code. This essentially consists of defining rules that cover all
combinations of IR expressions and map them to
[MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}
instructions.

The instruction selection component should be implemented in
[IR2ASM](http://www.program-transformation.org/Tiger/IR2ASM){.twikiLink}.r
in the [TigerTrans](TigerTrans){.twikiLink} package. In order to build
the component you\'ll also need to install the [ASM](ASM){.twikiLink}
package, which implements the back-end and provides the signature and
[OverlayDefinitions](../Stratego/OverlayDefinition){.twikiLink} for
[MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}
code.

### []{#Notes} Notes

-   Use the
    [OverlayDefinitions](../Stratego/OverlayDefinition){.twikiLink} in
    [MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}.r
    (from the [ASM](ASM){.twikiLink} package) as compact representations
    of abstract assembly code instructions.

<!-- -->

-   First define a basic instruction selection scheme that covers all
    [IntermediateRepresentation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
    constructs. Then try to find more complex patterns that produce more
    efficient code.

<!-- -->

-   Expressions produce results. In assembly code intermediate results
    should be stored in registers. If the IR expression does not
    explicitly move the result into a register, you\'ll have to invent a
    new temporary to put the result in and to retrieve it from in the
    next expression.

<!-- -->

-   In order to construct a correct control-flow graph, all branching
    instructions need to have all possible labels they can branch to in
    their labels argument. This includes the label of the next
    instruction in case the instruction can fall through. Also be aware
    of the fact that jal returns to the next instruction.

<!-- -->

-   Make small test programs to test your instruction selection scheme.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 13 Nov 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
