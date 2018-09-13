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
    Page](http://www.program-transformation.org/edit/Tiger/InstructionSelection?t=1536826656)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/InstructionSelection)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/InstructionSelection)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/InstructionSelection?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/InstructionSelection?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/InstructionSelection?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/InstructionSelection)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/InstructionSelection?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/InstructionSelection?template=oopsmore&param1=1.1&param2=1.1)
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
Instruction Selection {#instruction-selection .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

Instruction selection is the phase in compilation in which
[IntermediateRepresentation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
trees are mapped to sequences of target machine instructions.

Algorithms

-   [MaximalMunch[^?^](http://www.program-transformation.org/edit/Tiger/MaximalMunch?topicparent=Tiger.InstructionSelection)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [DynamicProgramming[^?^](http://www.program-transformation.org/edit/Tiger/DynamicProgramming?topicparent=Tiger.InstructionSelection)]{.twikiNewLink
    style="background : #FFFFCE;"}

The [TigerCompiler](TigerCompiler){.twikiLink} implements instruction
selection in the
[IR2ASM](http://www.program-transformation.org/Tiger/IR2ASM){.twikiLink}
component in the [TigerTrans](TigerTrans){.twikiLink} package. The
translation uses an encoding of the
[MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}
instruction set.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 04 Dec 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
