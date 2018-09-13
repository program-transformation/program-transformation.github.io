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
    Page](http://www.program-transformation.org/edit/Transform/ProgramTransformation?t=1536825364)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ProgramTransformation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ProgramTransformation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ProgramTransformation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ProgramTransformation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    23](http://www.program-transformation.org/view/Transform/ProgramTransformation?rev=1.23)
    [(diff 22)](http://www.program-transformation.org/rdiff/Transform/ProgramTransformation?rev1=1.23&rev2=1.22)
-   [Rev
    22](http://www.program-transformation.org/view/Transform/ProgramTransformation?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Transform/ProgramTransformation?rev1=1.22&rev2=1.21)
-   [Rev
    21](http://www.program-transformation.org/view/Transform/ProgramTransformation?rev=1.21)
    [(diff 20)](http://www.program-transformation.org/rdiff/Transform/ProgramTransformation?rev1=1.21&rev2=1.20)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ProgramTransformation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ProgramTransformation?template=oopsmore&param1=1.23&param2=1.23)
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
    \...](http://www.program-transformation.org/oops/Transform/ProgramTransformation?template=oopsmore&param1=1.23&param2=1.23)
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
Program Transformation {#program-transformation .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

(See also [ModelTransformation](ModelTransformation){.twikiLink})

[]{#A_Definition} A Definition
------------------------------

A program is a structured object with semantics. The structure allows us
to transform a program. The semantics gives us the means to compare
programs and to reason about the validity of transformations. Semantics
includes the extensional and intensional behaviour of a program. A
programming language is a collection of programs. This is a rather broad
definition that is designed to cover proper programming languages (with
an operational interpretation), but also data formats and
domain-specific languages.

Programming languages can be clustered into classes with structural
and/or semantic similarities. One of the aims of a general framework for
program transformation is to define transformations that are reusable
accross as wide a range of languages as possible. For example, the
notion of variable and variable binding is shared by all programming
languages. Transformations dealing with variables such as bound variable
renaming, substitution, and unification can be defined in a very generic
manner for all languages at once.

Program transformation is the act of changing one program into another.
The term *program transformation* is also used for a formal description
of an algorithm that implements program transformation. The language in
which the program being transformed and the resulting program are
written are called the *source* and *target* languages, respectively.

Program transformation is known under many different names

-   [Meta Programming](MetaProgramming){.twikiLink}
-   [Software generation](SoftwareGeneration){.twikiLink}
-   [Generative programming](GenerativeProgramming){.twikiLink}
-   [Program synthesis](ProgramSynthesis){.twikiLink}
-   [Program refinement](ProgramRefinement){.twikiLink}
-   [Program calculation](ProgramCalculation){.twikiLink}

[]{#A_Taxonomy_of_Program_Transforma} A Taxonomy of Program Transformation
--------------------------------------------------------------------------

Program transformation is used in many areas of software engineering,
including compiler construction, software visualization, documentation
generation, and automatic software renovation. In all these applications
we can distinguish two main scenarios, i.e., ones where the source and
target language are different (*translations*) from scenarios where they
are the same (*rephrasings*). These main scenarios can be refined into a
number of typical sub-scenarios based on their effect on the level of
abstraction of a program and to what extent they preserve the semantics
of a program. This refinement results in the following
[TransformationTaxonomy](TransformationTaxonomy){.twikiLink}.

-   Translation
    -   [ProgramMigration](ProgramMigration){.twikiLink}
    -   [ProgramSynthesis](ProgramSynthesis){.twikiLink}
        -   [ProgramRefinement](ProgramRefinement){.twikiLink}
        -   [ProgramCompilation](ProgramCompilation){.twikiLink}
        -   [CodeGeneration](CodeGeneration){.twikiLink}
    -   [ReverseEngineering](ReverseEngineering){.twikiLink}
        -   [DeCompilation](DeCompilation){.twikiLink}
        -   [ArchitectureExtraction](ArchitectureExtraction){.twikiLink}
        -   [DocumentationGeneration](DocumentationGeneration){.twikiLink}
        -   [SoftwareVisualization](SoftwareVisualization){.twikiLink}
    -   [ProgramAnalysis](ProgramAnalysis){.twikiLink}
-   Rephrasing
    -   [ProgramNormalization](ProgramNormalization){.twikiLink}
    -   [ProgramOptimization](ProgramOptimization){.twikiLink}
        -   [ProgramSpecialization](ProgramSpecialization){.twikiLink}
        -   [DeForestation](DeForestation){.twikiLink}
        -   [SuperCompilation](SuperCompilation){.twikiLink}
    -   [ProgramRefactoring](ProgramRefactoring){.twikiLink}
        -   [ProgramObfuscation](ProgramObfuscation){.twikiLink}
    -   [ProgramReflection[^?^](http://www.program-transformation.org/edit/Transform/ProgramReflection?topicparent=Transform.ProgramTransformation)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [SoftwareRenovation](SoftwareRenovation){.twikiLink} /
        [ReEngineering](ReEngineering){.twikiLink}

[]{#Translation} Translation
----------------------------

In a *translation* scenario a program is transformed from a source
language into a program in a *different* target language. Translation
scenarios can be distinguished by their effect on the level of
abstraction of a program. Although translations aim at preserving the
extensional semantics of a program, it is usually not possible to retain
all information across a translation. Examples of translation scenarios
are synthesis, migration, reverse engineering, and analysis. Their
relations are illustrated by the diagram in the following figure:

![Relationships](../pub/Transform/ProgramTransformation/taxonomy5.png)

### []{#Program_Synthesis}[]{#_Program_Synthesis_} [Program Synthesis](ProgramSynthesis){.twikiLink}

[ProgramSynthesis](ProgramSynthesis){.twikiLink} is a class of
transformations that lower the level of abstraction of a program. In
[ProgramRefinement](ProgramRefinement){.twikiLink} an implementation is
derived from a high-level specification such that the implementation
satisfies the specification. Compilation is a form of synthesis in which
a program in a high-level language is transformed to machine code. This
translation is usually achieved in several phases in which a high-level
language is first translted into an intermediate representation.
Instruction selection then translates the intermediate representation
into machine instructions. Other examples of synthesis are parser and
pretty-printer generation from context-free grammars.

### []{#Program_Migration}[]{#_Program_Migration_} [Program Migration](ProgramMigration){.twikiLink}

In [ProgramMigration](ProgramMigration){.twikiLink} a program is
transformed to another language at the same level of abstraction. This
can be a translation between dialects, for example, transforming a
Fortran77 program to an equivalent Fortran90 program or a translation
from one language to another, e.g., porting a Pascal program to C.

In some cases you may want to keep programming with the source language
(Fortran77 in the example), and migrate your program (to Fortran90) each
time you compile. It can be useful when you program in some kind of
\"old but very powerful source language\" that you don\'t want to throw
away, but you don\'t want to maintain the compiler.

### []{#Reverse_Engineering}[]{#_Reverse_Engineering_} [Reverse Engineering](ReverseEngineering){.twikiLink}

The purpose of [ReverseEngineering](ReverseEngineering){.twikiLink} is
to extract from a low-level program a high-level program or
specification, or at least some higher-level aspects. Reverse
engineering raises the level of abstraction and is the dual of
synthesis. Examples of reverse engineering are
[decompilation](DeCompilation){.twikiLink} in which an object program is
translated into a high-level program, architecture extraction in which
the design of a program is derived, documentation generation, and
software visualization in which some aspect of a program is depicted in
an abstract way.

### []{#Program_Analysis}[]{#_Program_Analysis_} [Program Analysis](ProgramAnalysis){.twikiLink}

[ProgramAnalysis](ProgramAnalysis){.twikiLink} reduces a program to one
aspect such as its control-flow. Analysis can thus be considered a
transformation to a sub-language or an aspect language.

[]{#Rephrasing} Rephrasing
--------------------------

Rephrasings are transformations that transform a program into a
different program in the *same* language, i.e., source and target
language are the same. In general, rephrasings try to say the same thing
in different words thereby aiming at *improving* some aspect of the
program, which entails that they *change the semantics* of the program.
The main sub-scenarios of rephrasing are normalization, optimization,
refactoring, and renovation.

### []{#Program_Normalization}[]{#_Program_Normalization_} [Program Normalization](ProgramNormalization){.twikiLink}

A normalization reduces a program to a program in a sub-language, with
the purpose of decreasing its syntactic complexity. *Desugaring* is a
kind of normalization in which some of the constructs (syntactic sugar)
of a language are eliminated by translating them into more fundamental
contructs. For example, the Haskell language definition describes for
many constructs how they can be desugared to a kernel language. Other
examples are module flattening and the definition of EBNF constructs in
pure BNF as is done for example in the
[SDF2](../Sdf/WebHome){.twikiLink} normalizer . *Simplification* is a
more general kind of normalization in which a program is reduced to a
normal (standard) form, without necessarily removing simplified
constructs. For example, consider canonicalization of intermediate
representation and algebraic simplification of expressions. Note that
normal form does not necessarily correspond to being a normal form with
respect to a set of rewrite rules.

### []{#Program_Optimization}[]{#_Program_Optimization_} [Program Optimization](ProgramOptimization){.twikiLink}

An *optimization* is a transformation that improves the run-time and/or
space performance of a program. Examples of optimization are fusion,
inlining, constant propagation, constant folding, common-subexpression
elimination, and dead code elimination.

### []{#Program_Refactoring}[]{#_Program_Refactoring_} [Program Refactoring](ProgramRefactoring){.twikiLink}

[ProgramRefactoring](ProgramRefactoring){.twikiLink} is a transformation
that improves the design of a program by restructuring it such that it
becomes easier to understand while preserving its functionality.
[ProgramObfuscation](ProgramObfuscation){.twikiLink} is a transformation
that makes a program *harder* to understand by renaming variables,
inserting dead code, etc. Obfuscation is done to hide the business rules
embedded in software by making it harder to reverse engineer the
program.

### []{#Program_Reflection}[]{#_Program_Reflection_} [Program Reflection[^?^](http://www.program-transformation.org/edit/Transform/ProgramReflection?topicparent=Transform.ProgramTransformation)]{.twikiNewLink style="background : #FFFFCE;"}

[ProgramReflection[^?^](http://www.program-transformation.org/edit/Transform/ProgramReflection?topicparent=Transform.ProgramTransformation)]{.twikiNewLink
style="background : #FFFFCE;"} is a transformation that changes a
program to compute some aspect of the program itself. For instance, one
can transform a program such that, in addition to its usual behaviour,
the program also calculates a trace of its own execution. Other uses
might include the generation of self-profiling programs.

### []{#Software_Renovation}[]{#_Software_Renovation_} [Software Renovation](SoftwareRenovation){.twikiLink}

In *software renovation* the extensional behaviour of a program is
changed in order to repair an error or to bring it up to date with
respect to changed requirements. Examples are repairing a Y2K bug, or
converting a program to deal with the Euro.

------------------------------------------------------------------------

[CategoryTaxonomy](CategoryTaxonomy){.twikiLink} \|
[CategoryEntryPoint](CategoryEntryPoint){.twikiLink} \|
[CategoryTransformation](CategoryTransformation){.twikiLink} \|
[CategoryReengineeringPages](CategoryReengineeringPages){.twikiLink} \|
\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 03 May 2001, 01 Apr
2002 \-- [TomMens](../Main/TomMens){.twikiLink} - 9 Apr 2004 \--
[MalcolmWallace](../Main/MalcolmWallace){.twikiLink} - 07 May 2004\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
