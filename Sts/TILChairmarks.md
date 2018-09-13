::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[Home](WebHome){.twikiLink}**\
[STS\'08](STS08){.twikiLink}\
[STS\'06](http://www.program-transformation.org/Sts/STS06){.twikiLink}\
[STS\'04](STS04){.twikiLink}\
[StsBench](StsBench){.twikiLink}\
\
**[News](WebNews){.twikiLink}**\
[Recent Changes](WebChanges){.twikiLink}\
[Mailinglist](MailingList){.twikiLink}\
\
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
    Page](http://www.program-transformation.org/edit/Sts/TILChairmarks?t=1536827751)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/TILChairmarks)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/TILChairmarks)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/TILChairmarks?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/TILChairmarks?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    26](http://www.program-transformation.org/view/Sts/TILChairmarks?rev=1.26)
    [(diff 25)](http://www.program-transformation.org/rdiff/Sts/TILChairmarks?rev1=1.26&rev2=1.25)
-   [Rev
    25](http://www.program-transformation.org/view/Sts/TILChairmarks?rev=1.25)
    [(diff 24)](http://www.program-transformation.org/rdiff/Sts/TILChairmarks?rev1=1.25&rev2=1.24)
-   [Rev
    24](http://www.program-transformation.org/view/Sts/TILChairmarks?rev=1.24)
    [(diff 23)](http://www.program-transformation.org/rdiff/Sts/TILChairmarks?rev1=1.24&rev2=1.23)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/TILChairmarks)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/TILChairmarks?template=oopsmore&param1=1.26&param2=1.26)
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
    \...](http://www.program-transformation.org/oops/Sts/TILChairmarks?template=oopsmore&param1=1.26&param2=1.26)
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
TILChairmarks {#tilchairmarks .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Software Transformation Systems
:::

The [TIL Chairmarks](TILChairmarks){.twikiLink} are a small set of
little benchmark transformation tasks, all based on the [Tiny Imperative
Language](TinyImperativeLanguage){.twikiLink} (TIL). They are called
\"chairmarks\" because they are too small to be called \"benchmarks\".
TIL is a very small imperative language with assignments, conditionals,
and loops, designed by [EelcoVisser](../Main/EelcoVisser){.twikiLink}
and [JamesCordy](../Main/JamesCordy){.twikiLink} as a basis for small
illustrative example transformations.

It is hoped that this page will grow to have a number of small example
benchmarks based on TIL and links to example solutions using a variety
of tools and systems. The idea is that the examples be reproduceable -
that is, the posted solution should contain everything neeeded for
someone else to run the task on their own computer using the tool or
system. In this way they can see all of the steps and artifacts involved
in doing the job.

The purpose is more one of understanding than one of comparison, and the
idea is to start small so that everyone will show their tool\'s method
here - although if things work out we may be able to grow this idea into
a set of real comparative benchmarks in the long run.

**TIL Training Set**:

-   [TIL Training Set](TILTrainingSet){.twikiLink}: A small set of
    example TIL programs to test on

**TIL Chairmark 1**: Parsing
([JamesCordy](../Main/JamesCordy){.twikiLink} - 29 Apr 2005)

-   Let\'s start small: the purpose of this one is to show differences
    in how the basic grammatical/lexical specs to support transformation
    of a language are done using different tools, and to create the
    basis in each tool for other Chairmarks. The TIL grammar can be
    found on the [Tiny Imperative
    Language](TinyImperativeLanguage){.twikiLink} page.

<!-- -->

-   *1.1 Basic Parser / Syntax Checker*: Parse input and check for
    syntax errors (output format irrelevant)
    -   [TIL Parser using TXL](TILParserUsingTXL){.twikiLink}

<!-- -->

-   *1.2 Pretty Printer*: Parse input and implement the identity
    transformation with pretty-printed output
    -   [TIL Pretty Printer using
        TXL](TILPrettyPrinterUsingTXL){.twikiLink}

<!-- -->

-   *1.3 Language Extensions*: Language extensions and dialects are the
    meat and potatoes of source transformation. Implement parsing of a
    language extension to TIL to the parser and pretty-printer above
    -   [TIL Begin-End Extension using
        TXL](TILBegin-EndExtensionUsingTXL){.twikiLink}
    -   [TIL Array Extension using
        TXL[^?^](http://www.program-transformation.org/edit/Sts/TILArrayExtensionUsingTXL?topicparent=Sts.TILChairmarks)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [TIL Function Extension using
        TXL[^?^](http://www.program-transformation.org/edit/Sts/TILFunctionExtensionUsingTXL?topicparent=Sts.TILChairmarks)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [TIL Module Extension using
        TXL[^?^](http://www.program-transformation.org/edit/Sts/TILModuleExtensionUsingTXL?topicparent=Sts.TILChairmarks)]{.twikiNewLink
        style="background : #FFFFCE;"}

**TIL Chairmark 2**: Restructuring
([JamesCordy](../Main/JamesCordy){.twikiLink} - 22 Aug 2005)

-   Classical restructuring: the purpose of this one is to show
    differences in how basic simple statement-level restructuring tasks
    are expressed using different tools. These solutions should normally
    be based on the parsers and pretty printers from Chairmark 1.
    However, because they are restructuring tasks, it would also be
    valid for them to assume well-formed input, since syntax-checking
    could be a separate screening task.

<!-- -->

-   *2.1 For-to-Nondeclaring-For*: TIL\'s for loop automatically
    declares the control variable; possibly this should not be the case.
    If that change happens, this transformation will fix old TIL
    programs by automatically introducing explicit declarations for
    control variables in all for statements
    -   [For-to-Nondeclaring-For using
        TXL](For-to-Nondeclaring-ForUsingTXL){.twikiLink}

<!-- -->

-   *2.2 For-to-While*: Possibly it was a mistake to add for loops to
    TIL. If for loops are removed, this transformation will restructure
    all for-loops in a TIL program to their while equivalents
    -   [For-to-While using TXL](For-to-WhileUsingTXL){.twikiLink}

<!-- -->

-   *2.3 Declarations-to-Global*: Even though TIL declarations seem to
    be able to appear anywhere according to the grammar, their meaning
    is apparently global (or is it?) In this transformation we make the
    true meaning of embedded declarations explicit by promoting all
    declarations to one global list at the beginning of the program
    -   [Declarations-to-Global using
        TXL](Declarations-to-GlobalUsingTXL){.twikiLink}

<!-- -->

-   *2.4 Declarations-to-Local*: Possibly TIL actually ought to have
    separate traditional nested scopes for each statement list (e.g.,
    inside each then part, else part, loop, etc.) If that is the case,
    then good style should keep all declarations as local as possible.
    In this transformation we move every declaration to its most local
    context. It might be interesting to run this one on the output of
    the previous one. Note that there are several quite distinct
    different ways to achieve this result
    -   [Declarations-to-Local using
        TXL](Declarations-to-LocalUsingTXL){.twikiLink}

<!-- -->

-   *2.5 Goto Elimination*: A popular and industrially relevant
    application of source transformation. In a dialect of TIL with
    statement labels and gotos added, recognize and eliminate
    while-equivalent goto structures
    -   [Goto Elimination using
        TXL](GotoEliminationUsingTXL){.twikiLink}

<!-- -->

-   *2.6 Refactoring*: Probably the most common application of source
    transformation. In the extension of TIL with functions, recognize
    and refactor one or more bad smells

<!-- -->

-   *2.7 Language Dialect Implementation*: Implement a language
    extension by transformation to the core language, with or without
    library calls. In the extension of TIL with modules (anonymous
    classes), implement the module extension by reduction to the
    function extension without modules
    -   [Module Dialect Implementation using
        TXL[^?^](http://www.program-transformation.org/edit/Sts/ModuleDialectImplementationUsingTXL?topicparent=Sts.TILChairmarks)]{.twikiNewLink
        style="background : #FFFFCE;"}

**TIL Chairmark 3**: Optimization
([JamesCordy](../Main/JamesCordy){.twikiLink} - 22 Aug 2005)

-   Classical source level optimizations: the purpose of this one is to
    show differences in how the basic source-level optimization tasks
    are expressed using different tools. These solutions should normally
    be based on the parsers and pretty printers from Chairmark 1.
    However, it would also be valid for them to assume well-formed input
    since syntax-checking could be a separate screening task.

<!-- -->

-   *3.1 Statement-level code motion*: Moving invariant assignments /
    computations out of while loops
    -   [Lift Invariant Assignments using
        TXL](LiftInvariantAssignmentsUsingTXL){.twikiLink}
    -   [Lift Invariant Assigned Computations using
        TXL](LiftInvariantAssignedComputationsUsingTXL){.twikiLink}
        (more sophisticated, with variable renaming)

<!-- -->

-   *3.2 Common subexpression elimination*: Recognizing and factoring
    out common subexpressions to new temporary variables
    -   [Common Subexpression Elimination using
        TXL](CommonSubexpressionEliminationUsingTXL){.twikiLink}

<!-- -->

-   *3.3 Strength reduction*: Recognizing and implementing opportunities
    to reduce \*\* to \*, or \* to + using loop iteration
    -   [Strength Reduction using
        TXL](StrengthReductionUsingTXL){.twikiLink}

<!-- -->

-   *3.4 Constant folding*: Recognizing and optimizing compile-time
    known variables and expressions
    -   [Constant Folding using
        TXL](ConstantFoldingUsingTXL){.twikiLink}

<!-- -->

-   *3.5 Statement folding*: Recognizing and optimizing compile-time
    known if statements, and possibly while and for statements
    -   [Statement Folding using
        TXL](StatementFoldingUsingTXL){.twikiLink}

<!-- -->

-   *3.6 Loop unrolling*: Unrolling for loops with known bounds

<!-- -->

-   *3.7 Function inlining*: In the dialect of TIL with functions and
    begin blocks, inline non-recursive functions using equivalent begin
    blocks

**TIL Chairmark 4**: Static and Dynamic Analysis
([JamesCordy](../Main/JamesCordy){.twikiLink} - 22 Aug 2005)

-   Software analysis tasks: the purpose of this one is to show
    differences in how simple static and dynamic analysis tasks are
    expressed using different tools. These solutions should normally be
    based on the parsers and pretty printers from Chairmark 1. However,
    it would also be valid for them to assume well-formed input since
    syntax-checking could be a separate screening task.

<!-- -->

-   *4.1 Something about redundant declarations*: Detecting and removing
    unused declarations
    -   [Removing Redundant Declarations using
        TXL](RemovingRedundantDeclarationsUsingTXL){.twikiLink}

<!-- -->

-   *4.2 Something about statistics*: Counting the numbers of statements
    of different kinds in a program
    -   [Statement Statistics using
        TXL](StatementStatisticsUsingTXL){.twikiLink}

<!-- -->

-   *4.3 Self Tracing Programs*: Transform a TIL program to a
    self-tracing version of itself, that prints out each statement as it
    is executed. This is a model for a large number of source
    transformations used in instrumentation and dynamic analysis tasks
    such as test coverage and dynamic flow analysis
    -   [Self Tracing Programs using
        TXL](SelfTracingProgramsUsingTXL){.twikiLink}

<!-- -->

-   *4.4 Type Inference*: TIL declares untyped variables, originally
    intended to be all integer. However, the addition of string values
    leads one to wonder if \"untyped\" means dynamically typed, allowing
    for string variables. If so, probably we want to make these types
    explicit and make TIL strongly typed sometime. This transformation
    infers the type of every variable in a TIL program from its uses and
    explicitly adds types to declarations using a new form: \"var x:
    integer;\" where the valid types are \"integer\" and \"string\".
    Variables of inconsistent type should be flagged as an error
    -   [Type Inference using TXL](TypeInferenceUsingTXL){.twikiLink}

<!-- -->

-   *4.5 Static Slicing*: Forward and / or backward slice of a program
    given a marked statement as criterion
    -   [Backward slicing using
        TXL](BackwardSlicingUsingTXL){.twikiLink}

<!-- -->

-   *4.6 Clone Detection*: Clone detection of repeated statements or
    sequences of statements in a program
    -   [Exact clones using TXL](ExactClonesUsingTXL){.twikiLink}
    -   [Consistently renamed clones using
        TXL](ConsistentlyRenamedClonesUsingTXL){.twikiLink}

<!-- -->

-   *4.7 Syntactic Markup*: Marking up program statements or expressions
    with some structural property
    -   [Syntactic markup using
        TXL](SyntacticMarkupUsingTXL){.twikiLink}

<!-- -->

-   *4.8 Unique Renaming*: Unique renaming gives scope-independent names
    to all declared items in a program, so that a relationship database
    extracted will not have ambiguities in entities. In the module
    extension to TIL, uniquely rename all declared items to reflect
    their scope
    -   [Unique renaming using
        TXL[^?^](http://www.program-transformation.org/edit/Sts/UniqueRenamingUsingTXL?topicparent=Sts.TILChairmarks)]{.twikiNewLink
        style="background : #FFFFCE;"}

<!-- -->

-   *4.9 Design Recovery*: Creation of a relationship database (fact
    extraction) for the entities of a program
    -   [Basic design recovery using
        TXL[^?^](http://www.program-transformation.org/edit/Sts/BasicDesignRecoveryUsingTXL?topicparent=Sts.TILChairmarks)]{.twikiNewLink
        style="background : #FFFFCE;"}

<!-- -->

-   *4.10 Design Analysis*: Querying of a relationship database to check
    for impact or architectural flaws

<!-- -->

-   *4.11 Semantic Markup*: Marking up program statements or expressions
    using some semantic property inferred from a relationship database

<!-- -->

-   *4.12 Semantic Transformation*: Transforming parts of a program
    using some semantic property inferred from a relationship database

<!-- -->

-   *4.12 Program metrics*:
    [McCabe[^?^](http://www.program-transformation.org/edit/Sts/McCabe?topicparent=Sts.TILChairmarks)]{.twikiNewLink
    style="background : #FFFFCE;"} cyclomatic complexity, function
    points or the like

<!-- -->

-   *4.13 Abstract Interpretation*: Interpret the TIL program in some
    semantic domain other than the value domain

**TIL Chairmark 5**: Language Implementation
([JamesCordy](../Main/JamesCordy){.twikiLink} - 22 Aug 2005)

-   Compilers and Interpreters: the purpose of this one is to show how
    simple imperative language compilers and interpreters are expressed
    using different tools. These solutions should normally be based on
    the parsers from Chairmark 1.

<!-- -->

-   *5.1 Interpretation*: Executing TIL programs by source
    transformation / rewriting
    -   [TIL Interpreter using TXL](TILInterpreterUsingTXL){.twikiLink}

<!-- -->

-   *5.2 Compilation*: Compiling TIL programs to byte code by source
    transformation / rewriting

<!-- -->

-   *5.3 Machine Simulation*: Byte code machine simulator using source
    transformation / rewriting

<!-- -->

-   *5.4 Translation*: Translating TIL to another high level language
    using source transformation / rewriting

------------------------------------------------------------------------

Page begun by [JamesCordy](../Main/JamesCordy){.twikiLink} - 29 Apr
2005; last revised by [JamesCordy](../Main/JamesCordy){.twikiLink} - 27
May 2009\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
