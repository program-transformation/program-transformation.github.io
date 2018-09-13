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
    Page](http://www.program-transformation.org/edit/Tiger/HpcSchedule?t=1536826698)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HpcSchedule)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HpcSchedule)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HpcSchedule?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HpcSchedule?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/Tiger/HpcSchedule?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Tiger/HpcSchedule?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Tiger/HpcSchedule?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Tiger/HpcSchedule?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Tiger/HpcSchedule?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Tiger/HpcSchedule?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HpcSchedule)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HpcSchedule?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/Tiger/HpcSchedule?template=oopsmore&param1=1.10&param2=1.10)
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
Hpc Schedule {#hpc-schedule .twikiTopicTitle}
============

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

In the course we discuss the following topics (Chapters refer to
[ModernCompilerImplementationInML](../Transform/ModernCompilerImplementationInML){.twikiLink}).
The project entries in the schedule are steps in building the
[TigerCompiler](TigerCompiler){.twikiLink}.

Week 1

-   Meeting 1 (29/10)
    -   Introduction,
        [CompilerArchitecture](CompilerArchitecture){.twikiLink},
        [TigerLanguage](TigerLanguage){.twikiLink},
        [StrategoLanguage](../Stratego/StrategoLanguage){.twikiLink}
        (Chapter 1, Appendix A)
-   Meeting 2 (2/11):
    -   Translating Tiger to MIPS
    -   Tiger Abstract Syntax, Assembly Code (Chapter 4)
    -   Tiger Eval

<!-- -->

-   Project
    -   [ExtendTigerWithDoWhile](ExtendTigerWithDoWhile){.twikiLink}

Week 2

-   Meeting 3 (5/11)
    -   Translation To
        [IntermediateRepresentation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
        (Chapter 7)
-   Meeting 4 (9/11)
    -   no meeting scheduled (voorlichting)

<!-- -->

-   Project
    -   [TranslateExpressionsByHand](TranslateExpressionsByHand){.twikiLink}
    -   [TranslateExpressionsToIntermediateRepresentation](TranslateExpressionsToIntermediateRepresentation){.twikiLink}

Week 3

-   Meeting 5 (12/11)
    -   Instruction Selection (Chapter 9)
    -   [NielsJanssen](../Main/NielsJanssen){.twikiLink}
-   Meeting 6 (16/11)
    -   Canonical Form for
        [IntermediateRepresentation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
        (Chapter 8)
    -   [MarcelBroeken[^?^](http://www.program-transformation.org/edit/Main/MarcelBroeken?topicparent=Tiger.HpcSchedule)]{.twikiNewLink
        style="background : #FFFFCE;"}

<!-- -->

-   Project
    -   IR2ASM: Instruction Selection for MIPS
    -   CanonicalizeIR: canonicalize Intermediate Representation

Week 4

-   Meeting 7 (19/11)
    -   Translating Declarations (Chapters 5, 6, 7, 12)
    -   [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}
-   Meeting 8 (23/11)
    -   Loose ends in the basic compiler

<!-- -->

-   Project
    -   Finish basic compiler
    -   week 5-6: Polish and extend with optimizers

Week 5

-   Meeting 9 (26/11)
    -   Dataflow Analysis (Chapter 17)
    -   [PaulHagg](../Main/PaulHagg){.twikiLink}
-   Meeting 10 (30/11)
    -   Register Allocation (Chapter 10, 11)
    -   Jory van Zessen

Week 6

-   Meeting 10 (3/12)
    -   The Memory Hierarchy (Chapter 21)
    -   [WesselDankers](../Main/WesselDankers){.twikiLink}
-   Meeting 11 (7/12)
    -   Loop Optimizations (Chapter 18)
    -   [RobVermaas](../Main/RobVermaas){.twikiLink}

Week 7

-   Meeting 11 (10/12)
    -   Pipelining and Scheduling (Chapter 20)
    -   [AlanVanDam](../Main/AlanVanDam){.twikiLink}
-   Meeting 11 (14/12)
    -   Compiling Functional Programming Languages (Chapter 15)
    -   Jory van Zessen,
        [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}

Week 8

-   Finish the [TigerCompiler](TigerCompiler){.twikiLink} (See
    [HpcProject](HpcProject){.twikiLink})

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
