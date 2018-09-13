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
    Page](http://www.program-transformation.org/edit/Tiger/AddAnOptimizer?t=1536826689)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/AddAnOptimizer)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/AddAnOptimizer)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/AddAnOptimizer?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/AddAnOptimizer?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tiger/AddAnOptimizer?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tiger/AddAnOptimizer?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tiger/AddAnOptimizer?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tiger/AddAnOptimizer?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tiger/AddAnOptimizer?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/AddAnOptimizer?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/AddAnOptimizer)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/AddAnOptimizer?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tiger/AddAnOptimizer?template=oopsmore&param1=1.4&param2=1.4)
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
Add An Optimizer {#add-an-optimizer .twikiTopicTitle}
================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

After finishing the basic [TigerCompiler](TigerCompiler){.twikiLink},
extend it with at least one optimization component. Which optimization
in which stage of compilation you implement is up to you. Here are some
ideas, but other optimizations are also possible

### []{#Transformations_on_Tiger_Abstrac} Transformations on [Tiger Abstract Syntax](http://www.program-transformation.org/Tiger/TigerAbstractSyntax){.twikiLink}

The [TigerOptimize](TigerOptimize){.twikiLink} component can be filled
with many kinds of optimizations.

-   Constant and copy propagation (requires
    [canonicalization](http://www.program-transformation.org/Tiger/IRCanonicalize){.twikiLink})
-   Dead code elimination
-   Allocate non-escaping records and arrays on the stack
-   Make [static links](StaticLink){.twikiLink} explicit
    ([LambdaLifting[^?^](http://www.program-transformation.org/edit/Transform/LambdaLifting?topicparent=Tiger.AddAnOptimizer)]{.twikiNewLink
    style="background : #FFFFCE;"})
-   [Partial evaluation](../Transform/PartialEvaluation){.twikiLink} /
    specialization
-   Make memory explicit (introduce `MEM` operator in Tiger)

### []{#Improvements_of_TAS2IR}[]{#Improvements_of_TAS2IR_} Improvements of [TAS2IR](TAS2IR){.twikiLink}

-   Improve stack allocation of escaping variables and spilled local
    variables (overlap variables that are not live at the same time)
-   [TailCallElimination](../Transform/TailCallElimination){.twikiLink}

### []{#Transformations_on_Intermediate}[]{#Transformations_on_Intermediate_} Transformations on [Intermediate Representation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}

-   Target different platforms (e.g. Intel)
-   Constant and copy propagation
-   Dead code elimination

### []{#Transformations_on_ASM_Code} Transformations on [ASM](ASM){.twikiLink} Code

-   Improve spilling heuristics in the register allocator

### []{#Extensions_of_the_Run_Time_Syste} Extensions of the [Run Time System](http://www.program-transformation.org/Tiger/RunTimeSystem){.twikiLink}

-   Garbage collection

### []{#Other} Other

-   Parallel execution

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 04 Dec 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
