::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/StrategoHistory?t=1536825372)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoHistory)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoHistory)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoHistory?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoHistory?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    11](http://www.program-transformation.org/view/Stratego/StrategoHistory?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Stratego/StrategoHistory?rev1=1.11&rev2=1.10)
-   [Rev
    10](http://www.program-transformation.org/view/Stratego/StrategoHistory?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Stratego/StrategoHistory?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Stratego/StrategoHistory?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/StrategoHistory?rev1=1.9&rev2=1.8)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoHistory)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoHistory?template=oopsmore&param1=1.11&param2=1.11)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoHistory?template=oopsmore&param1=1.11&param2=1.11)
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
Stratego History {#stratego-history .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Since its always interesting to see how ideas develop, this page
contains a reconstruction of the development of
[StrategoLanguage](StrategoLanguage){.twikiLink} and its implementation.

**March 1997**

At a visit to INRIA in Nancy the ideas of
[RewritingStrategies](RewritingStrategy){.twikiLink} in
[ELAN](../Transform/ELAN){.twikiLink} are explained. This looks like an
interesting mechanism for dealing with some of the problems encountered
in [ASFandSDF](../Transform/ASFandSDF){.twikiLink} specification.

**Summer 1997**

Development of strategy combinators with
[BasLuttik](../Transform/BasLuttik){.twikiLink}. The combinators are a
mixture of process algebra (sequential programming) and modal logic (for
term traversal). In contrast to [ELAN](../Transform/ELAN){.twikiLink} no
full backtracking operators are provided. New are combinators for
[GenericTermTraversal](GenericTermTraversal){.twikiLink}. The
combinators are implemented in
[ASFandSDF](../Transform/ASFandSDF){.twikiLink}.

-   [SpecificationOfRewritingStrategies](SpecificationOfRewritingStrategies){.twikiLink}

**Fall 1997**

At the
[OregonGraduateInstitute[^?^](http://www.program-transformation.org/edit/Transform/OregonGraduateInstitute?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
style="background : #FFFFCE;"}
[AndrewTolmach](../Transform/AndrewTolmach){.twikiLink} is interested in
a high-level language for specifying optimizations. An interpreter for
the strategy combinators is implemented in
[MetaML](../Transform/MetaML){.twikiLink}.

**Winter 1998**

Since the implementation of [MetaML](../Transform/MetaML){.twikiLink} is
not up to speed the implementation of the interpreter is continued in
Transform.SML. The interpreter parses modules written in a dedicated
language for specifying [RewriteRules](RewriteRule){.twikiLink} and
[RewritingStrategies](RewritingStrategy){.twikiLink}.

While attending POPL\'98 in San Diego it becomes clear that
[ContextualRules](ContextualRule){.twikiLink} (inspired by the paper
[ShrinkingLambdaExpressionsInLinearTime[^?^](http://www.program-transformation.org/edit/Transform/ShrinkingLambdaExpressionsInLinearTime?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
style="background : #FFFFCE;"} by
[AndrewAppel](../Transform/AndrewAppel){.twikiLink} and
[TrevorJim[^?^](http://www.program-transformation.org/edit/Transform/TrevorJim?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
style="background : #FFFFCE;"}) can be implemented elegantly when match
can share its variable scope with the context. A contextual rule can be
implemented by means of a local traversal that performs a transformation
that shares bindings from the context.

**Spring 1998**

Since interpretation is very slow implementation of compiler is begun
with [ZinoBenaissa](../Transform/ZinoBenaissa){.twikiLink}.

![portland-board-22-04-1998.jpg](http://www.cs.uu.nl/~visser/pictures/portland-board-22-04-1998.jpg)

(See also this
[CompilerWritingPicture](CompilerWritingPicture){.twikiLink})

The compiler is written in SML based on the front-end for the
intepreter. The compiler implements full backtracking. Strategy
definitions are interpreted as macros and are completely expanded at
compile time. The compiler reduces a specification to one huge strategy
expression which is compiled to a single C function.

-   Visit to
    [MaudeLanguage[^?^](http://www.program-transformation.org/edit/Transform/MaudeLanguage?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"} group at SRI

<!-- -->

-   [BuildingOptimizersWithRewritingStrategies[^?^](http://www.program-transformation.org/edit/Stratego/BuildingOptimizersWithRewritingStrategies?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}

At a talk at FMCS
[EugenioMoggi[^?^](http://www.program-transformation.org/edit/Transform/EugenioMoggi?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
style="background : #FFFFCE;"} observes that the operational semantics
does not require full backtracking. It turns out that an implementation
without full backtracking is desirable, i.e., much more efficient.

-   [ACoreLanguageForRewriting](ACoreLanguageForRewriting){.twikiLink}:
    implement traditional rewriting with strategies, allows easy
    extension with features such conditional and default rules

**Summer 1998**

As a test case for the language, i.e., to get material to compile and to
get a feeling for programming in the language, a compiler for the
strategies language is written in itself.

**September 1998**

The first bootstrap is completed just before attending
[ICFP](../Transform/ICFP){.twikiLink}\'98.

As [JanHeering](../Transform/JanHeering){.twikiLink} had already
suggested it suddenly becomes clear that the language should be called
Stratego.

**Fall 1998**

-   [StrategicPatternMatching](StrategicPatternMatching){.twikiLink}:
    overlays, [ContextualRules](ContextualRule){.twikiLink},
    [RecursivePattern](RecursivePattern){.twikiLink}

**Winter 1999**

The first application other than the toy RML compiler and the
[StrategoCompiler](StrategoCompiler){.twikiLink} itself is the
implementation of the [WarmFusion](WarmFusion){.twikiLink} algorithm
with [PatriciaJohann](../Transform/PatriciaJohann){.twikiLink}. This
later turns into the [HSX](HSX){.twikiLink} package.

-   [WarmFusionInStratego](WarmFusionInStratego){.twikiLink}

<!-- -->

-   [OttoSkroveBagge](OttoSkroveBagge){.twikiLink} from Bergen visits
    Utrecht to learn Stratego and to work on the implementation of
    [CodeBoost](CodeBoost){.twikiLink}, a transformation engine for C++
    programs.

**Summer 1999**

-   First public release (0.4.1) in August

**Fall 1999**

-   Architecture of the XT bundle of transformation tools
    -   [ImplodeAsFix[^?^](http://www.program-transformation.org/edit/Tools/ImplodeAsFix?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}: using Tools.SDF parsers
    -   pretty-printing: connecting the
        [GenericPrettyPrinting[^?^](http://www.program-transformation.org/edit/Tools/GenericPrettyPrinting?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"} package

**Winter 2000**

-   [OttoSkroveBagge](OttoSkroveBagge){.twikiLink} from Bergen visits
    for 3 months to work on the implementation of
    [CodeBoost](CodeBoost){.twikiLink}.

<!-- -->

-   [KarinaOlmos[^?^](http://www.program-transformation.org/edit/Stratego/KarinaOlmos?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"} starts DSP transformation project at
    Philips Research Laboratories

<!-- -->

-   [FirstStrategoUsersDay](FirstStrategoUsersDay){.twikiLink}

<!-- -->

-   Program Optimization Seminar
    -   simple optimizations

**Spring 2000**

-   [LanguageIndependentTraverals[^?^](http://www.program-transformation.org/edit/Stratego/LanguageIndependentTraverals?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   [GenericTermDeConstruction[^?^](http://www.program-transformation.org/edit/Stratego/GenericTermDeConstruction?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}

<!-- -->

-   First course on
    [SoftwareGeneration[^?^](http://www.program-transformation.org/edit/Stratego/SoftwareGeneration?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   [MondrianOptimizer[^?^](http://www.program-transformation.org/edit/Stratego/MondrianOptimizer?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}

**Summer 2000**

Implementation of compiler for
[TigerLanguage[^?^](http://www.program-transformation.org/edit/Hpc/TigerLanguage?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
style="background : #FFFFCE;"}

**Fall 2000**

-   First
    [HighPerformanceCompilersCourse[^?^](http://www.program-transformation.org/edit/Hpc/HighPerformanceCompilersCourse?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   [TigerInStratego[^?^](http://www.program-transformation.org/edit/Hpc/TigerInStratego?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}

<!-- -->

-   [XTaBundleOfTransformationTools[^?^](http://www.program-transformation.org/edit/Stratego/XTaBundleOfTransformationTools?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}

**Winter 2001**

-   Visit [PatriciaJohann](PatriciaJohann){.twikiLink}
    -   [FusingLogicAndControlWithLocalTransformations[^?^](http://www.program-transformation.org/edit/Stratego/FusingLogicAndControlWithLocalTransformations?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}

<!-- -->

-   Visit to Nancy: interpreter for
    [RhoCalculus[^?^](http://www.program-transformation.org/edit/Transform/RhoCalculus?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [StrategoScript[^?^](http://www.program-transformation.org/edit/Stratego/StrategoScript?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}: an interpreter for Stratego

<!-- -->

-   [SecondStrategoUsersDay](SecondStrategoUsersDay){.twikiLink}

<!-- -->

-   [ASurveyOfStrategiesInProgramTransformation[^?^](http://www.program-transformation.org/edit/Stratego/ASurveyOfStrategiesInProgramTransformation?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   Master\'s Projects
    -   [RhoStratego](RhoStratego){.twikiLink}: generalizing the case
        construct
    -   [CobolX](CobolX){.twikiLink}:
        [PreserveLayout[^?^](http://www.program-transformation.org/edit/Stratego/PreserveLayout?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [PanOptimizer](PanOptimizer){.twikiLink}:
        [InliningStrategies[^?^](http://www.program-transformation.org/edit/Stratego/InliningStrategies?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}

**Spring 2001**

Teaching

-   Second course on
    [SoftwareGeneration[^?^](http://www.program-transformation.org/edit/Stratego/SoftwareGeneration?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   new slides on Stratego

Language extension

-   [ScopedDynamicRewriteRules](ScopedDynamicRewriteRules){.twikiLink}:
    generation of context-sensive rules
    -   [TigerInterpreter[^?^](http://www.program-transformation.org/edit/Stratego/TigerInterpreter?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [TigerTypeChecker[^?^](http://www.program-transformation.org/edit/Stratego/TigerTypeChecker?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [TigerInliner[^?^](http://www.program-transformation.org/edit/Stratego/TigerInliner?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}

**Summer 2001**

-   [StrategoRelease06](StrategoRelease06){.twikiLink}

<!-- -->

-   New compilation scheme using setjmp/longjmp to implement failure and
    nested functions (a gcc extension) to implement higher-order
    strategy arguments.

**Fall 2001**

-   Third course on
    [SoftwareGeneration[^?^](http://www.program-transformation.org/edit/Stratego/SoftwareGeneration?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   more [slides](StrategoDocumentation){.twikiLink} on Stratego
    -   assignments on:
        [ProgramSimplification[^?^](http://www.program-transformation.org/edit/Transform/ProgramSimplification?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"},
        [SoftwareVisualization](../Transform/SoftwareVisualization){.twikiLink},
        [ProgramInstrumentation[^?^](http://www.program-transformation.org/edit/Transform/ProgramInstrumentation?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}

<!-- -->

-   Implementation of optimizations with
    [DynamicRules](DynamicRule){.twikiLink} by
    [KarinaOlmos](../Transform/KarinaOlmos){.twikiLink}

<!-- -->

-   Third course on [High-Performance
    Compilers[^?^](http://www.program-transformation.org/edit/Hpc/WebHome?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   Improved implementation of the
        [TigerCompiler[^?^](http://www.program-transformation.org/edit/Hpc/TigerCompiler?topicparent=Stratego.StrategoHistory)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   Bottomup-rewriting for code generation using dynamic rules by
        [MartinBravenboer](../Transform/MartinBravenboer){.twikiLink}

<!-- -->

-   [Stratego 0.6.3](StrategoRelease063){.twikiLink} introduces
    [TermWrap](TermWrap){.twikiLink} and
    [TermProject](TermProject){.twikiLink}

**Fall 2002**

-   [Stratego 0.8](StrategoDownload08){.twikiLink} introduces support
    for program transformation with concrete object syntax

**Winter 2003**

-   [StrategoXT
    0.9](http://www.stratego-language.org/Stratego/StrategoRelease09)
    merges Stratego and the XT toolset.

<!-- -->

-   [XTC](XTC){.twikiLink} tool composition for creating complete
    transformation systems in Stratego.

**Spring 2004**

-   [StrategoXT
    0.10](http://www.stratego-language.org/Stratego/StrategoRelease010):
    major redesign of dynamic rules.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
