::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[PEPM 2013](WebHome){.twikiLink}**\
[Call for Papers](CallForPapers){.twikiLink}\
[Important Dates](ImportantDates){.twikiLink}\
[Program Committee](ProgramCommittee){.twikiLink}\
\
**Advice for Authors**\
[Research Paper](ResearchPaperAdvice){.twikiLink}\
[Tool Paper](ToolPaperAdvice){.twikiLink}\
[Submission](PaperSubmission){.twikiLink}\
\
**PEPM Program**\
[Invited Talks](InvitedTalks){.twikiLink}\
[Accepted Papers](AcceptedPapers){.twikiLink}\
[A Best Paper Award](ABestPaperAward){.twikiLink}\
[Program](Program){.twikiLink}\
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
    Page](http://www.program-transformation.org/edit/PEPM13/AcceptedPapers?t=1536827679)
-   [Rename
    Page](http://www.program-transformation.org/rename/PEPM13/AcceptedPapers)
-   [Attach
    File](http://www.program-transformation.org/attach/PEPM13/AcceptedPapers)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PEPM13/AcceptedPapers?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PEPM13/AcceptedPapers?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    19](http://www.program-transformation.org/view/PEPM13/AcceptedPapers?rev=1.19)
    [(diff 18)](http://www.program-transformation.org/rdiff/PEPM13/AcceptedPapers?rev1=1.19&rev2=1.18)
-   [Rev
    18](http://www.program-transformation.org/view/PEPM13/AcceptedPapers?rev=1.18)
    [(diff 17)](http://www.program-transformation.org/rdiff/PEPM13/AcceptedPapers?rev1=1.18&rev2=1.17)
-   [Rev
    17](http://www.program-transformation.org/view/PEPM13/AcceptedPapers?rev=1.17)
    [(diff 16)](http://www.program-transformation.org/rdiff/PEPM13/AcceptedPapers?rev1=1.17&rev2=1.16)
-   [Total
    History](http://www.program-transformation.org/rdiff/PEPM13/AcceptedPapers)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PEPM13/AcceptedPapers?template=oopsmore&param1=1.19&param2=1.19)
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
    \...](http://www.program-transformation.org/oops/PEPM13/AcceptedPapers?template=oopsmore&param1=1.19&param2=1.19)
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
ACM SIGPLAN 2013 Workshop on Partial Evaluation and Program Manipulation
:::

The list of accepted papers and their abstracts are shown below, in no
particular order.

**Regular Research Papers:**

-   Jeroen Weijers, Jurriaan Hage and Stefan Holdermans. **Security Type
    Error Diagnosis for Higher-Order, Polymorphic Languages**\
    \
    **Abstract:** We combine the type error slicing and heuristics based
    approaches to type error diagnostic improvement within the context
    of type based security analysis on a let-polymorphic call by value
    lambda calculus extended with lists, pairs and the security specific
    constructs declassify and protect. We define and motivate four
    classes of heuristics that help diagnose inconsistencies among the
    constraints, and show their effect on a selection of security
    incorrect programs.

<!-- -->

-   Marco Servetto and Elena Zucca. **A meta-circular language for
    active libraries**\
    \
    **Abstract:** We present a new Java-like language design coupling
    disciplined meta-programming features with a composition language.
    That is, programmers can write meta-expressions that combine class
    definitions, on top of a small set of composition operators,
    inspired by the seminal Bracha\'s Jigsaw framework. Moreover, such
    operators are deep, that is, they allow to manipulate (e.g., rename
    or duplicate) a nested class at any level of depth.\
    \
    This provides an effective language support for active libraries:
    namely, a (library) class can provide a method returning a
    customized version of a class, depending, e.g., on the execution
    platform. Since a class can contain nested classes, a whole library
    can be generated in this way. That is, deep operators allows the
    programmer to better exploit meta-programming capabilities, leading
    to a \"meta-programming in the large\" style.\
    \
    We adopt a mixed typechecking technique, which provides a good
    compromise between meta-programming systems with extreme
    expressiveness and no static type checking, and those with strong
    type system and only limited meta-programming capability. In
    particular, our technique ensures an important property, called
    meta-level soundness, stating that typing errors never originate
    from already compiled (meta-)code, that is, programmers can safely
    use (active) libraries.

<!-- -->

-   Álvaro García-Pérez and Pablo Nogueira. **A Syntactic and Functional
    Correspondence between Reduction Semantics and Reduction-Free Full
    Normalisers**\
    \
    **Abstract:** Olivier Danvy and others have shown the syntactic
    correspondence between reduction semantics (a small-step semantics)
    and abstract machines, as well as the functional correspondence
    between reduction-free normalisers (a big-step semantics) and
    abstract machines. The correspondences are established by
    program-transformation (so-called interderivation) techniques. A
    reduction semantics and a reduction-free normaliser are
    interderivable when the abstract machine obtained from them is the
    same. However, the correspondences fail when the underlying
    reduction strategy is hybrid, i.e., relies on another sub-strategy.
    Hybridisation is an essential structural property of full-reducing
    and complete strategies. Hybridisation is unproblematic in the
    functional correspondence. But in the syntactic correspondence the
    refocusing and inlining-of-iterate-function steps become context
    sensitive, preventing the refunctionalisation of the abstract
    machine. We show how to solve the problem and showcase the
    interderivation of normalisers for normal order, the standard,
    full-reducing and complete strategy of the pure lambda calculus. Our
    extension makes it possible to interderive, rather than contrive,
    full-reducing abstract machines. As expected, the machine we obtain
    is a variant of Pierre Crégut\'s full Krivine machine KN.

<!-- -->

-   Qiang Sun, Yuting Chen and Jianjun Zhao. **Constraint-Based Locality
    Analysis for X10 Programs**\
    \
    **Abstract:** X10, a HPC (High Performance Computing) programming
    language proposed by IBM, supports a PGAS (Partitioned Global
    Address Space) programming model offering a shared address space.
    The address space can be further partitioned into several logical
    locations where objects and activities (or threads) will be
    dynamically created. An analysis of locations can help to check the
    safety of object accesses through exploring which objects and
    activities may reside in which locations, while in practice the
    objects and activities are usually designated at runtime and their
    locations may also vary under different environments. In this paper,
    we propose a constraint-based locality analysis method called
    Leopard for X10. Leopard calculates the points-to relations for
    analyzing the objects and activities in a program and uses a place
    constraint graph to analyze their locations. We have developed a
    tool to support Leopard, and conducted an experiment to evaluate its
    effectiveness and efficiency. The experimental results show that
    Leopard can calculate the locations of objects and activities
    precisely.

<!-- -->

-   Bruno Oliveira and Andres Loh. **Abstract Syntax Graphs for Domain
    Specific Languages**\
    \
    **Abstract:** This paper shows a Haskell representation for embedded
    domain specific languages (EDSLs) using abstract syntax graphs
    (ASGs). The purpose of this representation is to deal with the
    important problem of defining operations that require observing or
    preserving sharing and recursion in EDSLs in an expressive, yet easy
    to use way. In contrast to more conventional representations based
    on abstract syntax trees, ASGs represent sharing and recursion
    explicitly as binder constructs. We use a functional representation
    of ASGs based on structured graphs, where binders are encoded with
    parametric higher-order abstract syntax. We show how adapt to this
    representation to well-typed ASGs. This is especially useful for
    EDSLs, which often reuse the type system of the host language. We
    also show a type-class based encoding of (well-typed) ASGs that
    enables extensible and modular well-typed EDSLs while allowing the
    manipulation of sharing and recursion.

<!-- -->

-   Emanuele De Angelis, Fabio Fioravanti, Alberto Pettorossi and
    Maurizio Proietti. **Verifying Programs via Iterated
    Specialization**\
    \
    **Abstract:** We present a method for verifying safety properties of
    imperative programs by using techniques based on the specialization
    of constraint logic programs (CLP). We consider a class of C
    programs with integer variables, and we define their operational
    semantics as a reachability relation between memory configurations.
    Then we address the problem of verifying safety properties, stating
    that error configurations cannot be reached from initial
    configurations.\
    \
    The reachability relation is encoded as a CLP program R, and the
    safety property to be verified is encoded as the negation of a
    predicate unsafe in R, meaning that an {error} configuration can be
    reached from the initial configuration.\
    \
    Then, we check whether or not the safety property holds by
    specializing the CLP program R with respect to the given C program,
    initial and error configurations, so as to derive a new CLP program
    R\_s where the evaluation of unsafe either finitely fails (safety
    holds) or succeeds (safety does not hold). The program
    specialization strategy we propose always terminates, but due to the
    undecidability of safety properties, it may be the case that in the
    residual program R\_s we are not able to decide whether unsafe
    finitely fails or succeeds.\
    \
    Then, we apply again program specialization and iterate this process
    in the hope of proving safety or unsafety. During the various
    specializations we may apply different strategies for propagating
    information (e.g., forward propagation from an initial
    configuration, or backward propagation from an error configuration)
    and different operators for generalizing predicate definitions
    (e.g., widening and convex hull).\
    \
    We have implemented the various strategies using the MAP
    transformation system. By an experimental evaluation on various
    examples taken from the literature, we show that our method is
    competitive with respect to state-of-the-art software model
    checkers.

<!-- -->

-   Ryosuke Sato, Hiroshi Unno and Naoki Kobayashi. **Towards a Scalable
    Software Model Checker for Higher-Order Programs**\
    \
    **Abstract:** In our recent paper, we have shown how to construct a
    fully-automated program verification tool (so called a \"software
    model checker\") for a tiny subset of functional language ML, by
    combining higher-order model checking, predicate abstraction, and
    CEGAR. This can be viewed as a higher-order counterpart of previous
    software model checkers for imperative languages like BLAST and
    SLAM. The naive application of the proposed approach, however,
    suffered from scalability problems, both in terms of efficiency and
    supported language features. To obtain more scalable software model
    checkers for full-scale functional languages, we propose several
    optimizations and extensions of the previous approach. Among others,
    we introduce (i) selective CPS transformation, (ii) selective
    predicate abstraction, (iii) refined predicate discovery as
    optimization techniques, and (iv) functional encoding of recursive
    data structures and control operations to support a larger subset
    of ML. We have implemented the proposed methods, and obtained
    promising results.

<!-- -->

-   Dominique Devriese, Ilya Sergey, Dave Clarke and Frank Piessens.
    **Fixing Idioms - A recursion primitive for applicative DSLs**\
    \
    **Abstract:** In a lazy functional language, the standard encoding
    of recursion in DSLs uses the host language\'s recursion, so that
    DSL algorithms automatically use the host language\'s least
    fixpoints, even though many domains require algorithms to produce
    different fixpoints. In particular, this is the case for DSLs
    implemented as Applicative functors (structures with a notion of
    pure computations and function application). We propose a recursion
    primitive afix that models a recursive binder in a finally tagless
    HOAS encoding, but with a novel rank-2 type that allows us to
    specify and exploit the effects-values separation that characterizes
    Applicative DSLs. Unlike related approaches for Monads and Arrows,
    we model effectful recursion, not value recursion.\
    \
    Using generic programming techniques, we define an arity-generic
    version of the operator to model mutually recursive definitions. We
    recover intuitive user syntax with a form of shallow syntactic
    sugar: an alet construct that syntactically resembles the let
    construct, which we have implemented in the GHC Haskell compiler. We
    describe a proposed axiom for the afix operator. We demonstrate
    usefulness with examples from Applicative parser combinators and
    functional reactive programming. We show how higher-order recursive
    operators like many can be encoded without special library support,
    unlike previous approaches, and we demonstrate an implementation of
    the left recursion removal transform.

<!-- -->

-   Axel Simon. **Deriving a Complete Type Inference for Hindley-Milner
    and Vector Sizes using Expansion**\
    \
    **Abstract:** Type inference and program analysis both infer static
    properties about a program. Yet, they are constructed using very
    different techniques. We reconcile both approaches by deriving a
    type inference from a denotational semantics using abstract
    interpretation. We observe that completeness results in the abstract
    interpretation literature can be used to derive type inferences that
    are abstract-complete, a property akin to the inference of principal
    typings. The resulting algorithm is similar to that of
    Milner-Mycroft, that is, it infers Hindley-Milner types while
    allowing for polymorphic recursion. Instead of type schemes, it uses
    *expansion* to instantiate types. Since our expansion operator is
    agnostic to the abstract domain, we are able to apply it not only to
    types. We illustrate this by inferring the size of vector types
    using systems of linear equalities.

<!-- -->

-   Francisco Javier López-Fraguas and Enrique Martin-Martin. **Typing
    as Functional-Logic Evaluation**\
    \
    **Abstract:** We present a transformational approach to type
    inference for functional logic programs. More concretely, we give a
    wide set of examples showing how, given a functional logic program
    P, we can synthesize a remarkably simple and natural functional
    logic program P\' such that the evaluation of expressions with
    respect to P\' corresponds to typing the expressions in the
    original P. We start developing those ideas for the case of type
    inference with standard Hindley-Milner types, and after that we
    consider some variations, like local definitions with different
    degrees of polymorphism, existential types, or type checking in
    presence of polymorphic recursion. For the basic case of
    Hindley-Milner types we provide also a formalization of the
    transformation and proofs of its adequacy. Besides its potential
    applicability to the implementation of different type systems, or to
    the educational use of the synthesized typing programs to explain
    different type inference/checking processes, the paper demonstrates
    vividly the expressive power of functional logic languages, as well
    as some of their limitations to the purpose of metaprogramming, that
    we have overcome by providing a suitable set of metalogical
    functions to inspect, classify and manipulate expressions according
    to their structure, similar to well known Prolog metapredicates for
    such purposes.

<!-- -->

-   Kostis Sagonas, Josep Silva and Salvador Tamarit. **Precise
    Explanation of Success Typing Errors**\
    \
    **Abstract:** Nowadays, many dynamic languages come with (some sort
    of) type inference in order to detect type errors statically. Often,
    in order not to unnecessarily reject programs which are allowed
    under a dynamic type discipline, their type inference algorithms are
    based on non-standard (i.e., not Hindley-Milner based) type
    inference techniques and employ aggressive forwards and backwards
    propagation of subtype constraints. Although such analyses are
    effective in locating real errors, the type errors they report are
    often extremely difficult for programmers to follow and convince
    themselves that something should be changed in their programs.\
    \
    We have observed this phenomenon in the context of Erlang: for a
    number of years now its implementation comes with a static analysis
    tool called Dialyzer which, among other software discrepancies,
    detects definite type errors (i.e., code points that will result in
    a runtime error if executed) by inferring success typings.\
    \
    In this work, we extend the analysis that infers success typings,
    with infrastructure that maintains additional information that can
    be used to provide precise (i.e., minimal) explanations about the
    cause of a discrepancy reported by Dialyzer using program slicing.\
    \
    An interesting aspect of the information that our analysis gathers
    is that it is not useful only for explaining definite type errors
    but also places in the code containing unreachable statements, dead
    code, etc., i.e. discrepancies which would normally be undetected by
    most type inference, static analysis, or testing techniques.\
    \
    We have implemented the techniques we describe in a publicly
    available development branch of Dialyzer.

<!-- -->

-   Bruno Martinez, Marcos Viera and Alberto Pardo. **Just Do It While
    Compiling!: Fast Extensible Records in Haskell**\
    \
    **Abstract:** The library for strongly typed heterogeneous
    collections HList provides an implementation of extensible records
    in Haskell that needs only a few common extensions of the language.
    In HList, records are represented as linked lists of label-value
    pairs with a look-up operation that is linear-time in the number of
    fields. In this paper, we use type-level programming techniques to
    develop a more efficient representation of extensible records for
    HList. We propose two internal encodings for extensible records that
    improve lookup at runtime without needing a total order on the
    labels. One of the encodings performs lookup in constant time but at
    a cost of linear time insertion. The other one performs lookup in
    logarithmic time while preserving the fast insertion of simple
    linked lists. Through staged compilation, the required slow search
    for a field is moved to compile time in both cases.

<!-- -->

-   María Alpuente, Marco A. Feliú and Alicia Villanueva. **Automatic
    Inference of Specifications using Matching Logic**\
    \
    **Abstract:** Formal specifications can be used for various software
    engineering activities ranging from finding errors to documenting
    software and automatic test-case generation. Automatically
    discovering specifications for heap-manipulating programs is a
    challenging task. In this paper, we propose a technique for
    automatically inferring formal specifications from code which is
    based on the symbolic execution and automated reasoning tandem
    \"Matching Logic / K framework\". We implemented our technique for a
    fragment of C, called
    [KernelC[^?^](http://www.program-transformation.org/edit/PEPM13/KernelC?topicparent=PEPM13.AcceptedPapers)]{.twikiNewLink
    style="background : #FFFFCE;"}, in the automated tool
    [KingSpec[^?^](http://www.program-transformation.org/edit/PEPM13/KingSpec?topicparent=PEPM13.AcceptedPapers)]{.twikiNewLink
    style="background : #FFFFCE;"}, which generates axioms that describe
    the precise input/output behavior of C routines that handle
    pointer-based structures, i.e., result values and state change.
    These specifications can be written either in Matching Logic itself,
    which is useful for further automated analysis within the K formal
    environment, or in sugared axiomatic form, which favors better human
    inspection. Since we rely on rewriting logic K semantics
    specification of programming languages, our approach can be easily
    extended to any language for which a formal semantics in K is given.

**Tool Demonstration Papers:**

-   Martin Sulzmann, Jürgen Nicklisch and Axel Zechner. **Traceability
    and Correctness of EDSL Abstractions**\
    \
    **Abstract:** EDSLs (embedded domain-specific languages) are in
    particular suitable for agile software projects. New abstractions
    can be coded quickly and easily in the EDSLs host language and are
    automatically transformed to the basic primitives of the EDSLs. In
    the context of formal software certification, it is paramount that
    these abstractions are *correct* and that the low-level code
    resulting from the EDSL primitives can be *traced* to some
    higher-level artifacts, let it be some concrete programming
    abstractions, software requirements etc. We have built an EDSL-based
    toolchain for implementing and testing mission critical applications
    which supports measures to guarantee traceability and correctness of
    EDSL abstractions. We give an overview of our approach and practical
    experiences applying the EDSLs in the industrial context.

<!-- -->

-   Marco Comini and Luca Torella. **TRSynth: a Tool for Automatic
    Inference of Term Equivalence in Left-linear Term Rewriting
    Systems**\
    \
    **Abstract:** This paper presents a technique to automatically infer
    algebraic property-oriented specifications from Term Rewriting
    Systems. Namely, given the source code of a TRS we infer a
    specification which consists of a set of equations relating (nested)
    terms (operation calls) that rewrite to the same set of values.\
    \
    In this paradigm there are several additional issues which arises
    with respect to the (first order) functional programming case,
    because free variables are admitted in queries and
    non-constructor-based rules are allowed.\
    \
    The (glass-box) semantic-based inference method that we propose can
    cope with this issues and achieves, to some extent, the correctness
    of the inferred specification, differently from other (black-box)
    approaches based on testing techniques.\
    \
    To experiment on the validity of our proposal we have considered an
    instance of the proposed method employing a novel (condensed)
    semantics for left-linear TRSs and we have implemented a \"proof of
    concept\" prototype in Haskell which is available online.

**Short Papers:**

-   Michael Carbin, Deokhwan Kim, Sasa Misailovic and Martin Rinard.
    **Verified Integrity Properties for Safe Approximate Program
    Transformations**\
    \
    **Abstract:** Approximate computations (for example, video, audio,
    and image processing computations, machine learning computations,
    and many scientific computations) have the freedom to generate a
    range of acceptable results. Approximate program transformations
    (for example, task skipping and loop perforation) exploit this
    freedom to produce computations that can execute at a variety of
    points in an underlying accuracy versus performance trade-off space.
    One potential concern is that these transformations may change the
    semantics of the program and therefore cause the program to crash,
    perform an illegal operation, or otherwise violate its integrity.\
    \
    We investigate verifying integrity properties \-- key correctness
    properties that the transformed computation must respect \-- to
    safely apply approximate program transformations. We present our
    experience developing and evaluating a compiler that verifies
    integrity properties of computations expressed as \`for\' loops,
    then leverages these verified properties to safely apply
    transformations that perforate the loops.

<!-- -->

-   Baris Aktemur, Yukiyoshi Kameyama, Oleg Kiselyov and Chung‐chieh
    Shan. **Shonan Challenge for Generative Programming (Short Position
    Paper)**\
    \
    **Abstract:** The appeal of generative programming is \"abstraction
    without guilt\": eliminating the vexing trade-off between writing
    high-level code and highly-performant code. Generative programming
    also promises to formally capture the domain-specific knowledge and
    heuristics used by high-performance computing (HPC) experts. How far
    along are we in fulfilling these promises? To gauge our progress, a
    recent Shonan Meeting on \"bridging the theory of staged programming
    languages and the practice of high-performance computing\" proposed
    to use a set of benchmarks, dubbed \"Shonan Challenge\".\
    \
    Shonan Challenge is a collection of crisp problems posed by HPC and
    domain experts, for which efficient implementations are known but
    were tedious to write and modify. The challenge is to generate a
    similar efficient implementation from the high-level specification
    of a problem, performing the same optimizations, but automatically.
    It should be easy to adjust optimizations and the specification,
    maintaining confidence in the generated code.\
    \
    We describe our initial set of benchmarks and provide two solutions
    to one of the problems. We hope that the Shonan Challenge will
    clarify the state of the art and stimulate the theory and technology
    of staging just as the POPLmark challenge did for meta-theory
    mechanization. Since each Shonan Challenge problem is a kernel of a
    significant HPC application, each solution has an immediate
    practical application.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
