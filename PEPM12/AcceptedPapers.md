::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[PEPM 2012](WebHome){.twikiLink}**\
[Call for Papers](CallForPapers){.twikiLink}\
[Important Dates](ImportantDates){.twikiLink}\
[Program Committee](ProgramCommittee){.twikiLink}\
\
**Advice for Authors**\
[Research Paper](ResearchPaperAdvice){.twikiLink}\
[Tool Paper](ToolPaperAdvice){.twikiLink}\
[Submission](PaperSubmission){.twikiLink}\
\
**[PEPM Program](Program){.twikiLink}**\
[Invited Talks](InvitedTalks){.twikiLink}\
[Accepted Papers](AcceptedPapers){.twikiLink}\
[A Best Paper Award](ABestPaperAward){.twikiLink}\
\
**Local Information**\
[Venue](WorkshopVenue){.twikiLink}\
[Registration & Accommodation](RegistrationAndAccomodation){.twikiLink}\
\
**History**\
[Previous Meetings](PreviousMeetings){.twikiLink}\
[Journal Special Issues](SpecialIssues){.twikiLink}\
[Statistics](HistoricalStatistics){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/PEPM12/AcceptedPapers?t=1536827673)
-   [Rename
    Page](http://www.program-transformation.org/rename/PEPM12/AcceptedPapers)
-   [Attach
    File](http://www.program-transformation.org/attach/PEPM12/AcceptedPapers)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PEPM12/AcceptedPapers?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PEPM12/AcceptedPapers?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    13](http://www.program-transformation.org/view/PEPM12/AcceptedPapers?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/PEPM12/AcceptedPapers?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/PEPM12/AcceptedPapers?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/PEPM12/AcceptedPapers?rev1=1.12&rev2=1.11)
-   [Rev
    11](http://www.program-transformation.org/view/PEPM12/AcceptedPapers?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/PEPM12/AcceptedPapers?rev1=1.11&rev2=1.10)
-   [Total
    History](http://www.program-transformation.org/rdiff/PEPM12/AcceptedPapers)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PEPM12/AcceptedPapers?template=oopsmore&param1=1.13&param2=1.13)
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
    \...](http://www.program-transformation.org/oops/PEPM12/AcceptedPapers?template=oopsmore&param1=1.13&param2=1.13)
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
Accepted Papers {#accepted-papers .twikiTopicTitle}
===============

::: {.twikiWebTitle}
ACM SIGPLAN 2012 Workshop on Partial Evaluation and Program Manipulation
:::

The following papers (in no particular order) will be presented at the
workshop.

**Regular research papers:**

-   Naoki Kobayashi, Kazutaka Matsuda and Ayumi Shinohara. **Functional
    Programs as Compressed Data**\
    \
    **Abstract:** We propose an application of programming language
    techniques to lossless data compression, where tree data are
    compressed as functional programs that generate them. The approach
    has several advantages. First, it follows from the standard argument
    of Kolmogorov complexity that the size of compressed data can be
    optimal up to an additive constant. Secondly, a compression
    algorithm is clean: it is just a sequence of beta-expansions for
    lambda-terms. Thirdly, one can use program verification and
    transformation techniques (higher-order model checking, in
    particular) to apply certain operations on data without
    decompression. In the paper, we present algorithms for data
    compression and manipulation based on the approach, and prove their
    correctness. We also report preliminary experiments on prototype
    data compression/transformation systems.

<!-- -->

-   Kazutaka Matsuda, Kazuhiro Inaba and Keisuke Nakano.
    **Polynomial-Time Inverse Computation for Accumulative Functions
    with Multiple Data Traversals**\
    \
    **Abstract:** Inverse computation has many applications such as
    implementation of serialization/deserialization, providing support
    for undo, and test-case generation for software testing. In this
    paper, we propose an inverse computation method that always
    terminates for a class of functions known as parameter-linear macro
    tree transducers, which involves multiple data traversals and the
    use of accumulations. The key to our method is the observation that
    a function in the class can be seen as a non-accumulating
    context-generating transformation without multiple data traversals.
    We demonstrate that this observation makes it easy to achieve
    terminating inverse computation for the class by context-wise
    memoization of inverse computation results. We also show that, when
    we use a tree automaton to express the inverse computation result,
    our inverse computation runs in time polynomial to the size of an
    original output and the textual program size.

<!-- -->

-   Dana N. Xu. **Hybrid Contract Checking via Symbolic
    Simplification**\
    \
    **Abstract:** Program errors are hard to detect or prove absent.
    Allowing programmers to write formal and precise specification,
    especially in the form of contracts, is one popular approach to
    program verification and error discovery. We formalize and implement
    a hybrid contract checker for a subset of OCaml. The key technique
    we use is symbolic simplification, which makes integrating static
    and dynamic contract checking easy and effective. It tries to
    statically verify that a function satisfies its contract or
    precisely blames functions at fault when there is a contract
    violation. When a contract satisfaction is undecidable, it leaves
    the residual code for dynamic contract checking.

<!-- -->

-   Susumu Katayama. **An Analytical Inductive Functional Programming
    System that Avoids Unintended Programs**\
    \
    **Abstract:** Inductive functional programming (IFP) is a research
    field extending from software science to artificial intelligence
    that deals with functional program synthesis based on generalization
    from ambiguous specifications, usually given as input-output example
    pairs. Currently, the approaches to IFP can be categorized into two
    general groups: the analytical approach that is based on analysis of
    the input-output example pairs, and the generate-and-test approach
    that is based on generation and testing of many candidate programs.
    The analytical approach is more hopeful for application to greater
    problems because the search space is restricted by the given example
    set, but it requires much more examples written in order to yield
    results that reflect the user\'s intention, which bothers and
    actually makes the algorithm slow down. On the other hand, the
    generate- and-test approach does not require long description of
    input-output examples, but does not restrict the search space using
    the example set. This paper proposes a new approach taking the best
    of the two, called \`\`analytically-generate-and-test approach\'\',
    which is based on analytical generation and testing of many program
    candidates. For generating many candidate programs, the proposed
    system uses a new variant of IGORII , the exemplary analytical
    inductive functional programming algorithm. This new system
    preserves the efficiency features of analytical approaches, while
    minimizing the possibility of generating unintended programs even
    when using fewer input-output examples.

<!-- -->

-   Roberto Giacobazzi, Neil Jones and Isabella Mastroeni. **Obfuscation
    by Partial Evaluation of Distorted Interpreters**\
    \
    **Abstract:** How to construct a general program obfuscator? We
    present a novel approach to automatically generating obfuscated code
    P\' from any program P with source clear code. Start with a
    (program-executing) interpreter interp for the language in which P
    is written. Then \`\`distort\'\' interp so it is still correct, but
    its specialization P\' with respect to P is transformed code that is
    equivalent to the original program, but harder to understand or
    analyze. Potency of the obfuscator is proved with respect to a
    general model of the attacker, modeled as an approximate (abstract)
    interpreter. A systematic approach to distortion is to make program
    P obscure by transforming it to P\' on which (abstract)
    interpretation is incomplete. Interpreter distortion can be done by
    making residual in the specialization process sufficiently many
    interpreter operations to defeat an attacker in extracting sensible
    information from transformed code. Our method is applied to: code
    flattening, data-type obfuscation, and opaque predicate insertion.
    The technique is language independent and can be exploited for
    designing obfuscating compilers.

<!-- -->

-   Michael Gorbovitski, Yanhong A. Liu, Scott Stoller and Tom Rothamel.
    **Composing Transformations for Instrumentation and Optimization**\
    \
    **Abstract:** When transforming programs for complex instrumentation
    and optimization, it is essential to understand the effect of the
    transformations, to best optimize the transformed programs, and to
    speedup the transformation process. This paper describes a powerful
    method for composing transformation rules to achieve these goals.\
    We specify the transformations declaratively as instrumentation
    rules and invariant rules, the latter for transforming complex
    queries in instrumentation and in programs into efficient
    incremental computations. Our method automatically composes the
    transformation rules and optimizes the composed rules before
    applying the optimized composed rules. The method allows (1) the
    effect of transformations to be accumulated in composed rules and
    thus easy to see, (2) the replacements in composed rules to be
    optimized without the difficulty of achieving the optimization on
    large transformed programs, and (3) the transformation process to be
    sped up by applying a composed rule in one pass of program analyses
    and transformations instead of applying the original rules in
    multiple passes. We have implemented the method for Python, and
    successfully used it for instrumentation in ranking peers in
    [BitTorrent[^?^](http://www.program-transformation.org/edit/PEPM12/BitTorrent?topicparent=PEPM12.AcceptedPapers)]{.twikiNewLink
    style="background : #FFFFCE;"}, and for optimization of complex
    queries in the instrumentation of
    [BitTorrent[^?^](http://www.program-transformation.org/edit/PEPM12/BitTorrent?topicparent=PEPM12.AcceptedPapers)]{.twikiNewLink
    style="background : #FFFFCE;"}, in evaluating connections of network
    hosts using
    [NetFlow[^?^](http://www.program-transformation.org/edit/PEPM12/NetFlow?topicparent=PEPM12.AcceptedPapers)]{.twikiNewLink
    style="background : #FFFFCE;"}, and in generating efficient
    implementations of Constrained RBAC. We present experimental results
    that demonstrate the benefits and effectiveness of the method.

<!-- -->

-   Elvira Albert, Jesús Correas Fernández, Germán Puebla and Guillermo
    Román-Díez. **Incremental Resource Usage Analysis**\
    \
    **Abstract:** The aim of incremental global analysis is, given a
    program, its analysis results and a series of changes to the
    program, to obtain the new analysis results as efficiently as
    possible and, ideally, without having to (re-)analyze fragments of
    code which are not affected by the changes. Incremental analysis can
    significantly reduce both the time and the memory requirements of
    analysis. This paper presents an incremental resource usage (a.k.a.
    cost) analysis for a sequential Java-like language. Our main
    contributions are (1) a multidomain incremental fixed-point
    algorithm which can be used by all global (pre-)analyses required to
    infer the cost (including class, sharing, cyclicity, constancy, and
    size analyses) and which takes care of propagating dependencies
    among such domains, and (2) a novel form of cost summaries which
    allows us to incrementally reconstruct only those components of cost
    functions affected by the change. Experimental results in the COSTA
    system show that the proposed incremental analysis can perform very
    efficiently in practice.

<!-- -->

-   Takumi Goto and Isao Sasano. **An approach to completing variable
    names for implicitly typed functional languages**\
    \
    **Abstract:** This paper presents an approach to complete variable
    names when writing programs in implicitly typed functional
    languages. As a first step toward developing practical systems, we
    considered a simple case: up to the cursor position the program text
    is given completely. With this assumption we specify a variable
    completion problem for an implicitly typed core functional language
    with let-polymorphism and show an algorithm for solving the problem.
    Based on the algorithm we have implemented variable completion
    system for the language as an Emacs-mode.

<!-- -->

-   Martin Hirzel and Bugra Gedik. **Streams that Compose using Macros
    that Oblige**\
    \
    **Abstract:** Since the end of frequency scaling, the programming
    languages community has started to embrace multi-core and even
    distributed systems. One paradigm that lends itself well to
    distribution is stream processing. In stream processing, an
    application consists of a directed graph of streams and operators,
    where streams are infinite sequences of data items, and operators
    fire in infinite loops to process data. This model directly exposes
    parallelism, requires no shared memory, and is a good match for
    several emerging application domains such as algorithmic trading,
    telecommunications, health monitoring, and large-scale data
    processing. Unfortunately, streaming languages have so far been
    lacking in abstraction. This paper introduces higher-order composite
    operators, which encapsulate stream subgraphs, and contracts, which
    specify pre- and post-conditions for where a composite can be used.
    Composites are expanded at compile time, in a manner similar to
    macros. Their contractual obligations are also checked at
    compile-time. We build on existing work on macros and contracts to
    implement our higher-order composites. The user-visible language
    features provide a consistent look-and-feel for the streaming
    language, whereas the underlying implementation provides
    high-quality static error messages and prevents accidental name
    capture.

<!-- -->

-   Vlad Ureche, Tiark Rompf, Arvind Sujeeth, Hassan Chafi and Martin
    Odersky. **StagedSAC: A Case Study in Performance-Oriented DSL
    Development**\
    \
    **Abstract:** Domain-specific languages (DSLs) can bridge the gap
    between high-level programming and efficient execution. However,
    implementing compiler tool-chains for performance oriented DSLs
    requires an enormous effort. Recent research has produced
    methodologies and frameworks that promise to lower this burden
    significantly by allowing an easy transition from a purely embedded,
    library-only DSL implementation to one that introduces optimizing
    compilation.\
    In this paper we report on our experience implementing
    [StagedSAC[^?^](http://www.program-transformation.org/edit/PEPM12/StagedSAC?topicparent=PEPM12.AcceptedPapers)]{.twikiNewLink
    style="background : #FFFFCE;"}, a DSL for arithmetic processing with
    multidimensional arrays that is heavily inspired by the stand-alone
    language Single Assignment C. Its main feature is shape-generic
    loops that allow concise implementations of many interesting
    algorithms. At the same time, the functional, side-effect free
    semantics enable many advanced compiler optimizations.\
    The case study will present the path we took to implement the
    compiler, tradeoffs we made, program transformations we implemented
    to speed up the resulting code, all at a fraction of the effort
    normally put into developing a full compiler from scratch.

<!-- -->

-   Markus Degen, Peter Thiemann and Stefan Wehr. **The Interaction of
    Contracts and Laziness**\
    \
    **Abstract:** Contract monitoring for strict higher-order functional
    languages has an intuitive meaning, an established theoretical
    basis, and a standard implementation. For lazy functional languages,
    the situation is less clear-cut. There is no agreed-upon intended
    meaning or theory, and there are competing implementations with
    subtle semantic differences.\
    This paper proposes meaning preservation and completeness as
    formally defined properties for evaluating implementations of
    contract monitoring. Both properties have simple definitions that
    are straightforward to check. A survey of existing implementations
    reveals that some are meaning preserving, some are complete, and
    some have neither property. The main result is that contract
    monitoring for lazy functional languages cannot be complete and
    meaning preserving at the same time, although both properties can be
    achieved in isolation.

<!-- -->

-   Surinder Kumar Jain, Chenyi Zhang and Bernhard Scholz. **Translating
    Flowcharts to Non-Deterministic Languages**\
    \
    **Abstract:** Modelling languages are used to verify software. With
    the deployment of non-deterministic modelling languages in program
    language tools, more sophisticated program analyses and
    transformation techniques are possible due to non-determinism.
    However, control flow graphs are pre-dominantly used as intermediate
    language in programming language tools, which belong to the family
    of deterministic flowchart languages.\
    In this work, we translate programs in a deterministic flowchart
    language to a non-deterministic algebraic modelling language. For
    the translation, we employ the technique of converting a finite
    state automata to a regular expression. The states of the finite
    state automata represent states in the control flow graph, and the
    edges represent the edges in the control flowgaph. We construct a
    homomorphism to show that the translation is sound, i.e., we prove
    that the semantics of the program in the deterministic flowchart
    language is preserved in the translation. Experiments on our
    implemented algorithm are conducted on the SPEC benchmark suite.

<!-- -->

-   Francisco Javier López-Fraguas, Enrique Martin-Martin and Juan
    Rodriguez-Hortala. **Well-typed Narrowing with Extra Variables in
    Functional-Logic Programming**\
    \
    **Abstract:** Narrowing is the usual computation mechanism in
    functional-logic programming (FLP), where bindings for free
    variables are found at the same time that expressions are reduced.
    These free variables may be already present in the goal expression,
    but they can also be introduced during computations by the use of
    program rules with extra variables. However, it is known that
    narrowing in FLP generates problems from the point of view of types,
    problems that can only be avoided using type information at
    run-time. Nevertheless, most FLP systems use static typing based on
    Damas-Milner type system and they do not carry any type information
    in execution, thus ill-typed reductions may be performed in these
    systems. In this paper we prove, using the let-narrowing relation as
    the operational mechanism, that types are preserved in narrowing
    reductions provided the substitutions used preserve types. Based on
    this result, we prove that types are also preserved in narrowing
    reductions without type checks at run-time when higher order (HO)
    variable bindings are not performed and most general unifiers are
    used in unifications, for programs with transparent patterns. That
    is then used to show that a simulation of needed narrowing via
    program transformation also preserves types. To conclude, we
    characterize a restricted class of programs for which no binding of
    HO variables happens in reductions, identifying some problems
    encountered in the definition of this class.

<!-- -->

-   Geoff Hamilton and Neil Jones. **Superlinear Speedup by
    Distillation: A Semantic Basis**\
    \
    **Abstract:** In this paper, we provide a semantic basis for the
    distillation pro- gram transformation algorithm. We show that
    superlinear speedups can be obtained using distillation which cannot
    be obtained using other fully automatic program transformation
    techniques such as deforestation, positive supercompilation and
    partial evaluation, and we explain how these superlinear speedups
    occur.

**Short papers:**

-   Jacques Carette and Aaron Stump. **Towards Typing for Small-Step
    Direct Reflection**\
    \
    **Abstract:** Direct reflection is a form of meta-programming in
    which program terms can intensionally analyze other program terms.
    Previous work defined a big-step semantics for a directly reflective
    language called Archon, with a conservative approach to variable
    scoping based on operations for opening a lambda-abstraction and
    swapping the order of nested lambda-abstractions. In this short
    paper, we give a small-step semantics for a revised version of
    Archon, based on operations for opening and closing lambda
    abstractions. We then discuss challenges for designing a static type
    system for this language, which is our ultimate goal.

<!-- -->

-   Janis Voigtländer. **Ideas for Connecting Inductive Program
    Synthesis and Bidirectionalization**\
    \
    **Abstract:** We share a vision of connecting the topics of
    bidirectional transformation and inductive program synthesis, by
    proposing to use the latter in approaching problematic aspects of
    the former. Specifically, we argue that analytical inductive program
    synthesis, with its focus on modelling and emulating programmer
    strategies, has much to offer to bidirectionalization (the act of
    automatically producing a backwards from a forwards transformation,
    so far typically lacking a way to integrate programmer intentions
    and expectations). This research perspective does not present
    accomplished results, rather opening discussion and describing
    experiments designed to explore this promising potential.

**Tool demonstration papers:**

-   Edvard K. Karlsen, Einar W. Høst and Bjarte M. Østvold. **Finding
    and fixing Java naming bugs with the Lancelot Eclipse plugin**\
    \
    **Abstract:** The Lancelot plugin extends the integrated development
    environment Eclipse with support for finding and fixing \`naming
    bugs\' in Java programs. A naming bug is a mismatch between the name
    and implementation of a method, in the sense that the pairing of
    name and implementation do not correspond to the implicit method
    naming conventions used by many well-known open source
    applications.\
    Lancelot has not been presented before, but its theoretical
    foundations and evaluation have been published. The contribution of
    the present paper is to present a publicly available tool building
    on our theory, explain the design of the tool, including some
    necessary adaptations to the interactive use setting, and report on
    our experience with it. The source code of Lancelot is available
    under an open source license.

<!-- -->

-   Adriaan Moors, Tiark Rompf, Philipp Haller and Martin Odersky.
    **Scala-Virtualized**\
    \
    **Abstract:** This paper describes the Scala-Virtualized compiler,
    which extends the mainline Scala compiler with a small number of
    features that enable combining the benefits of shallow and deep
    embeddings of DSLs. We demonstrate our approach by showing how to
    embed three different domain-specific languages in Scala. Moreover,
    we summarize how others have been using our extended compiler in
    their own research and teaching. Supporting artifacts of our tool
    include web-based tutorials, nightly builds, and an Eclipse update
    site hosting an up-to-date version of the Scala IDE for Eclipse
    based on the Virtualized Scala compiler and standard library.

<!-- -->

-   Elvira Albert, Puri Arenas, Samir Genaim, Miguel Gómez-Zamalloa and
    Germán Puebla. **COSTABS: A Cost and Termination Analyzer for ABS**\
    \
    **Abstract:** ABS is an Abstract Behavioural Specification language
    to model distributed concurrent systems. Characteristic features of
    ABS are that: (1) it allows abstracting from implementation details
    while remaining executable: a functional sub-language over abstract
    data types is used to specify internal, sequential computations;
    and (2) the imperative sub-language provides flexible concurrency
    and synchronization mechanisms by means of asynchronous method
    calls, release points in method definitions, and cooperative
    scheduling of method activations. This paper presents COSTABS, a
    COSt and Termination analyzer for ABS programs, which is able to
    obtain resource usage upper bounds for both the imperative and
    functional fragments of a program. The resources that COSTABS can
    infer include termination, number of execution steps, memory
    consumption, number of asynchronous calls, among others. The
    analysis bounds provide formal guarantees that the execution of the
    program will never exceed the inferred amount of resources. The
    system can be downloaded as free software from its web site, where a
    repository of examples and a web interface are also provided. To the
    best of our knowledge, COSTABS is the first system able to perform
    resource analysis for a concurrent language.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
