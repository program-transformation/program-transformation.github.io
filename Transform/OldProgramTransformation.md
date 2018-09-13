::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/OldProgramTransformation?t=1536826524)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/OldProgramTransformation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/OldProgramTransformation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/OldProgramTransformation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/OldProgramTransformation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/OldProgramTransformation?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/OldProgramTransformation?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/OldProgramTransformation?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/OldProgramTransformation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/OldProgramTransformation?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/OldProgramTransformation?template=oopsmore&param1=1.2&param2=1.2)
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
Old Program Transformation {#old-program-transformation .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Definition**

*Program transformation* is the act of changing one program into
another. The term *program transformation* is also used for a program,
or any other description of an algorithm, that implements program
transformation.

The language in which the program being transformed and the resulting
program are written are called the *source* and *target* languages,
respectively. One can distinguish scenarios where the source and target
language are different (*translations*) from scenarios where they are
the same (*rephrasings*).

**Transformation Scenarios**

Program transformation is used in many areas of
[SoftwareEngineering](SoftwareEngineering){.twikiLink}, including
[CompilerConstruction[^?^](http://www.program-transformation.org/edit/Transform/CompilerConstruction?topicparent=Transform.OldProgramTransformation)]{.twikiNewLink
style="background : #FFFFCE;"},
[SoftwareVisualization](SoftwareVisualization){.twikiLink},
[DocumentationGeneration](DocumentationGeneration){.twikiLink}, and
automatic [SoftwareRenovation](SoftwareRenovation){.twikiLink}. At the
basis of all these different applications lie the main program
transformation *scenarios* of translation and rephrasing. These main
scenarios can be refined into a number of typical *sub-scenarios* that
are characterized by the *constraints* imposed on the main scenarios.

**Translation**

In a *translating* scenario a program is transformed from a source
language into a program in a *different* target language. Examples of
translating scenarios are synthesis, migration, compilation, analysis.
In [ProgramSynthesis](ProgramSynthesis){.twikiLink} an implementation is
derived from a high-level specification by semantics preserving
transformations. That is, it is guaranteed that the implementation
satisfies the specification. A prime example of program synthesis is
parser generation. In [ProgramMigration](ProgramMigration){.twikiLink} a
program is transformed to another language, while preserving all
meaning. For example, transforming a Fortran77 program to an equivalent
Fortran90 program. Compilation is a form of synthesis in which a program
in a high-level language is transformed to a program in a more low-level
language. In [ProgramAnalysis](ProgramAnalysis){.twikiLink} a program is
reduced to some property, or value. Type-checking is an example of
program analysis.

**Rephrasing**

In a *rephrasing* scenario a program is transformed into a different
program in the *same* language, i.e., source and target language are the
same. Examples of rephrasing scenarios are normalization, renovation,
refactoring and optimization In a
[ProgramNormalization](ProgramNormalization){.twikiLink} a program is
reduced to a program in a sub-language. In
[SoftwareRenovation](SoftwareRenovation){.twikiLink} some aspect of a
program is improved. For example, repairing a Y2K bug. A
[ProgramRefactoring](ProgramRefactoring){.twikiLink} is a meaning
preserving modification that improves the design. A
[ProgramOptimization](ProgramOptimization){.twikiLink} is a meaning
preserving modification that improves the run-time and/or space
performance of the program.
[CompilationByTransformation](CompilationByTransformation){.twikiLink}
is a paradigm in which many components of a compilers are defined as
rephrasing transformations.

**A Taxonomy of Transformation Scenarios**

The program transformation scenarios discussed above can be organized in
a taxonomy of sub-scenarios.

Translating scenarios

-   [ProgramMigration](ProgramMigration){.twikiLink}
-   [ProgramSynthesis](ProgramSynthesis){.twikiLink}
    -   Compilation
        -   [TranslationToIR[^?^](http://www.program-transformation.org/edit/Transform/TranslationToIR?topicparent=Transform.OldProgramTransformation)]{.twikiNewLink
            style="background : #FFFFCE;"}
        -   [InstructionSelection](InstructionSelection){.twikiLink}
    -   [ProgramRefinement](ProgramRefinement){.twikiLink}
-   [ReverseEngineering](ReverseEngineering){.twikiLink}
    -   [ArchitectureExtraction](ArchitectureExtraction){.twikiLink}
    -   [DocumentationGeneration](DocumentationGeneration){.twikiLink}
    -   [SoftwareVisualization](SoftwareVisualization){.twikiLink}
-   [ProgramAnalysis](ProgramAnalysis){.twikiLink}
    -   [ControlFlowAnalysis](ControlFlowAnalysis){.twikiLink}
    -   [DataFlowAnalysis](DataFlowAnalysis){.twikiLink}
    -   [TypeAnalysis[^?^](http://www.program-transformation.org/edit/Transform/TypeAnalysis?topicparent=Transform.OldProgramTransformation)]{.twikiNewLink
        style="background : #FFFFCE;"}

Rephrasing scenarios

-   [ProgramNormalization](ProgramNormalization){.twikiLink}
    -   [ProgramSimplification[^?^](http://www.program-transformation.org/edit/Transform/ProgramSimplification?topicparent=Transform.OldProgramTransformation)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [ProgramDesugaring[^?^](http://www.program-transformation.org/edit/Transform/ProgramDesugaring?topicparent=Transform.OldProgramTransformation)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [AspectWeaving[^?^](http://www.program-transformation.org/edit/Transform/AspectWeaving?topicparent=Transform.OldProgramTransformation)]{.twikiNewLink
        style="background : #FFFFCE;"}
-   [ProgramOptimization](ProgramOptimization){.twikiLink}
    -   [ProgramSpecialization](ProgramSpecialization){.twikiLink}
    -   [FunctionInlining[^?^](http://www.program-transformation.org/edit/Transform/FunctionInlining?topicparent=Transform.OldProgramTransformation)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [CommonSubexpressionElimination[^?^](http://www.program-transformation.org/edit/Transform/CommonSubexpressionElimination?topicparent=Transform.OldProgramTransformation)]{.twikiNewLink
        style="background : #FFFFCE;"}
-   [ProgramRestructuring[^?^](http://www.program-transformation.org/edit/Transform/ProgramRestructuring?topicparent=Transform.OldProgramTransformation)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   [ProgramRefactoring](ProgramRefactoring){.twikiLink}
    -   [SoftwareRenovation](SoftwareRenovation){.twikiLink}

**Other Definitions**

The
[FreeOnLineDictionaryOfComputing](FreeOnLineDictionaryOfComputing){.twikiLink}
describes program transformation as: *The systematic development of
efficient programs from high-level specifications by meaning-preserving
program manipulations. Also known as optimisation.*

[WolframKahl](WolframKahl){.twikiLink} (at
<http://ist.unibw-muenchen.de/kahl/progtrans.html>) defines program
transformation as: *Program transformation systematically changes a
program within one language into a different shape, usually preserving
its semantics. The aim usually is to improve efficiency.*

These definitions correspond to the notions
[ProgramSynthesis](ProgramSynthesis){.twikiLink} or
[ProgramOptimization](ProgramOptimization){.twikiLink} above. The reason
for choosing a wider scope of program transformation is that the other
scenarios discussed above have much in common with the narrower notion
of [ProgramOptimization](ProgramOptimization){.twikiLink}; improving the
efficiency is not the only application of program transformation
techniques.

**Tools**

Many program transformations can be implemented by means of
[ProgramTransformationTools](ProgramTransformationTools){.twikiLink}
that support the description of program transformations at a
(reasonably) high level of abstraction.

**See Also**

-   [TheOnlineSurveyOfProgramTransformation](TheOnlineSurveyOfProgramTransformation){.twikiLink}

------------------------------------------------------------------------

[CategoryTransformation](CategoryTransformation){.twikiLink} \|
Contributions by [EelcoVisser](../Main/EelcoVisser){.twikiLink},
[JoostVisser](../Main/JoostVisser){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
