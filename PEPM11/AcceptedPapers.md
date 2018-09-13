::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[PEPM 2011](WebHome){.twikiLink}**\
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
[Schedule](Program){.twikiLink}\
\
**Local Information**\
[Venue](WorkshopVenue){.twikiLink}\
[Registration & Accommodation](RegistrationAndAccomodation){.twikiLink}\
\
**History**\
[Previous Meetings](PreviousMeetings){.twikiLink}\
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
    Page](http://www.program-transformation.org/edit/PEPM11/AcceptedPapers?t=1536827667)
-   [Rename
    Page](http://www.program-transformation.org/rename/PEPM11/AcceptedPapers)
-   [Attach
    File](http://www.program-transformation.org/attach/PEPM11/AcceptedPapers)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PEPM11/AcceptedPapers?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PEPM11/AcceptedPapers?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    11](http://www.program-transformation.org/view/PEPM11/AcceptedPapers?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/PEPM11/AcceptedPapers?rev1=1.11&rev2=1.10)
-   [Rev
    10](http://www.program-transformation.org/view/PEPM11/AcceptedPapers?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/PEPM11/AcceptedPapers?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/PEPM11/AcceptedPapers?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/PEPM11/AcceptedPapers?rev1=1.9&rev2=1.8)
-   [Total
    History](http://www.program-transformation.org/rdiff/PEPM11/AcceptedPapers)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PEPM11/AcceptedPapers?template=oopsmore&param1=1.11&param2=1.11)
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
    \...](http://www.program-transformation.org/oops/PEPM11/AcceptedPapers?template=oopsmore&param1=1.11&param2=1.11)
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
ACM SIGPLAN 2011 Workshop on Partial Evaluation and Program Manipulation
:::

The following papers (in no particular order) will be presented at the
workshop.

**Regular research papers:**

-   Torben Mogensen. **Partial Evaluation of the Reversible Language
    Janus**\
    \
    **Abstract:** A reversible programming language is a programming
    language in which you can only write reversible programs, i.e.,
    programs that can be run both forwards (computing outputs from
    inputs) and backwards (computing inputs from outputs). It is
    interesting to study reversible programs and languages because
    computations on reversible computers (computers that only allow
    reversible programs) in theory can be done using less energy than
    computations on traditional irreversible computers. Janus is a
    reversible, structured imperative programming language. The partial
    evaluator for Janus presented in this paper is believed to be the
    first partial evaluator for a reversible programming language. The
    requirement that residual programs must be reversible adds some
    complications, which we address in the paper.

<!-- -->

-   Yuta Ikeda and Susumu Nishimura. **Calculating Tree Navigation with
    Symmetric Relational Zipper**\
    \
    **Abstract:** Navigating through tree structures is a core operation
    in tree processing programs. Most notably, XML processing programs
    intensively use XPath, the path specification language that locates
    particular nodes in a given document structure. In functional
    programming languages, such tree navigation operations can be
    implemented by means of Huet\'s zipper, without using destructive
    updates on the tree structure. The expected natural symmetry, e.g.,
    the symmetry between the operation for going one-level down in the
    tree structure and that for coming back the other way around, is not
    a perfect inverse, because those operations cannot be modeled neatly
    by functional programs due to partiality and non-injectivity.This
    paper develops a theory for reasoning about equalities of tree
    navigation operations. We model basic tree navigation operations,
    which have a perfect symmetry, by relations over zippers. The
    relational specification allows us to derive equations by simple
    calculations. We apply the calculational method to derivation of
    certain equalities of XPath expressions. The point-free relational
    reasoning not only leads to a concise justification of some known
    results derived from the symmetry but also establishes equations for
    a larger class of tree navigation, including those with negative
    constraints and those beyond XPath expressibility.

<!-- -->

-   Enrique Martin-Martin. **Type Classes in Functional Logic
    Programming**\
    \
    **Abstract:** Type classes provide a clean, modular and elegant way
    of writing overloaded functions. Functional logic programming
    languages(FLP in short) like Toy or Curry have adopted the
    Damas-Milner type system, so it seems natural to adopt also type
    classes in FLP.However, type classes has been barely introduced in
    FLP. A reason for this lack of success is that the usual translation
    of type classes using dictionaries presents some problems in FLP
    like the absence of expected answers due to a bad interaction of
    dictionaries with the call-time choice semantics for non-determinism
    adopted in FLP systems.In this paper we present a type-passing
    translation of type classes based on type-indexed functions and type
    witnesses that is well-typed with respect to a new liberal type
    system recently proposed for FLP. We argue the suitability of this
    translation for FLP because it improves the dictionary-based one in
    in three aspects. First, it obtains programs which run as fast or
    faster\-\--with a speedup from 1.05 to 2.30 in our experiments.
    Second, it solves the mentioned problem of missing answers. Finally,
    the proposed translation generates shorter and simpler programs.

<!-- -->

-   Tim Bauer, Martin Erwig, Alan Fern and Jervis Pinto.
    **Adaptation-Based Programming in Java**\
    \
    **Abstract:** Writing deterministic programs is often difficult for
    problems whose optimal solutions depend on unpredictable properties
    of the programs\' inputs.Difficulty is also encountered for problems
    where the programmer is uncertain about how to best implement
    certain aspects of a solution. For such problems a mixed strategy of
    deterministic programming and machine learning can often be very
    helpful: Initially, define those parts of the program that are well
    understood and leave the other parts loosely defined through default
    actions,but also define how those actions can be improved depending
    on results from actual program runs. Then run the program repeatedly
    and let the loosely defined parts adapt.In this paper we present a
    library for Java that facilitates this style of programming, called
    adaptation-based programming. We motivate the design of the library,
    define the semantics of adaptation-based programming,and demonstrate
    through two evaluations that the approach works well in
    practice.Adaptation-based programming is a form of program
    generation in which the creation of programs is controlled by
    previous runs. It facilitates a whole new spectrum of programs
    between the two extremes of totally deterministic programs and
    machine learning.

<!-- -->

-   Hugo Pacheco and Alcino Cunha. **Calculating with Lenses: Optimising
    Bidirectional Transformations**\
    \
    **Abstract:** This paper presents an equational calculus to reason
    about bidirectional transformations specified in the point-free
    style. In particular, it focuses on the so-called lenses as a
    bidirectional idiom,and shows that many standard laws characterising
    point-free combinators and recursion patterns are also valid on that
    setting. A key result is that uniqueness also holds for
    bidirectional folds and unfolds, thus unleashing the power of fusion
    as a program optimisation technique. A rewriting system for
    automatic lens optimisation is also presented, thus proving the
    usefulness of the proposed calculus.

<!-- -->

-   Rinus Plasmeijer, Peter Achten, Pieter Koopman, Bas Lijnse, Thomas
    van Noort and John van Groningen. **iTasks for a Change - Type-safe
    run-time change in dynamically evolving workflows**\
    \
    **Abstract:** Workflow management systems (WFMS) are software
    systems that coordinate the tasks human workers and computers have
    to perform to achieve a certain goal based on a given workflow
    description. Due to changing circumstances, it happens often that
    some tasks in a running workflow need to be performed differently
    than originally planned and specified. Most commercial WFMSs cannot
    deal with the required run-time changes properly. These changes have
    to be specified at the level of the underlying Petri-Net based
    semantics. Moreover, the implicit external state has to be adapted
    to the new task as well. Such low-level updates can easily lead to
    wrong behaviour and other errors. This problem is known as the
    dynamic change bug. In the iTask WFMS, workflows are specified using
    a radically different approach: workflows are constructed in a
    compositional style, using pure functions and combinators as
    self-contained building blocks. This paper introduces a change
    concept for the iTask system where self-contained tasks can be
    replaced by other self-contained tasks, thereby preventing dynamic
    change bugs. The static and dynamic typing system furthermore
    guarantees that these tasks have compatible types.

<!-- -->

-   Joao Paulo Fernandes, Joao Saraiva, Daniel Seidel and Janis
    Voigtlander. **Strictification of Circular Programs**\
    \
    **Abstract:** Circular functional programs (necessarily evaluated
    lazily) have been used as algorithmic tools, as attribute grammar
    implementations,and as target for program transformation techniques.
    Classically,Richard Bird \[1984\] showed how to transform certain
    multi-traversal programs (which could be evaluated strictly or
    lazily) into one-traversal ones using circular bindings. Can we go
    the other way, even for programs that are not in the image of his
    technique?That is the question we pursue in this paper. We develop a
    methodology that on the one hand lets us deal with typical examples
    corresponding to attribute grammars, but on the other hand also
    helps to derive new algorithms for problems not previously in reach.

<!-- -->

-   Carl Friedrich Bolz, Antonio Cuni, Maciej Fijalkowski, Michael
    Leuschel, Samuele Pedroni and Armin Rigo. **Allocation Removal by
    Partial Evaluation in a Tracing JIT**\
    \
    **Abstract:** The performance of many dynamic language
    implementations suffers from high allocation rates and runtime type
    checks. This makes dynamic languages less applicable to purely
    algorithmic problems, despite their growing popularity. In this
    paper we present a simple compiler optimization based on online
    partial evaluation to remove object allocations and runtime type
    checks in the context of a tracing JIT. We evaluate the optimization
    using a Python VM and find that it gives good results for all our
    (real-life) benchmarks.

<!-- -->

-   Rafael Caballero. **A Program Transformation for Returning States in
    Functional-Logic Programs**\
    \
    **Abstract:** This paper studies the conditions necessary to safely
    introduce new values as part of the results of function rules in
    functional-logic programs. The idea is to consider an initial
    functional-logic program and to produce, by means of a program
    transformation, a new program including states. Each rule of the new
    program returns pairs of values, with the first value the same as in
    the original program, and the second one a new value that can be
    defined in terms of the values returned by the function calls
    occurring in the rule. We prove that the transformation ensures the
    equivalence of the two programs with respect to the
    constructor-based
    [ReWriting[^?^](http://www.program-transformation.org/edit/PEPM11/ReWriting?topicparent=PEPM11.AcceptedPapers)]{.twikiNewLink
    style="background : #FFFFCE;"} Logic, a suitable semantics for
    functional-logic programs.

<!-- -->

-   Dimitrios Vardoulakis and Olin Shivers. **Ordering Multiple
    Continuations on the Stack**\
    \
    **Abstract:** Passing multiple continuation arguments to a function
    in CPS form allows one to encode a wide variety of direct-style
    control constructs, such as conditionals, exceptions, and
    multi-return function calls. We show that, with a simple syntactic
    restriction on the CPS language, one can prove that these
    multi-continuation arguments can be compiled into stack frames in
    the traditional manner. The restriction comes with no loss in
    expressive power, since we can still encode the same control
    mechanisms.In addition, we show that tail calls can be generalized
    efficiently for many continuations because the run-time check to
    determine which continuation to pop to can be avoided with a simple
    static analysis. A prototype implementation shows that our analysis
    is very precise, with small additional cost in compilation time.

<!-- -->

-   Olaf Chitil. **A Semantics for Lazy Assertions**\
    \
    **Abstract:** Lazy functional programming languages need lazy
    assertions to ensure that assertions preserve the meaning of
    programs. Examples in this paper demonstrate that previously
    proposed lazy assertions nonetheless break basic semantic
    equivalences, because they include a non-deterministic disjunction
    combinator. The objective of this paper is to determine \"correct\"
    definitions for lazy assertions. The starting point is our
    formalisation of basic properties such as laziness, taking them as
    axioms of our design space. We develop the first denotational
    semantics for lazy assertions where assertions denote subdomains. We
    define a weak disjunction combinator and together with a conjunction
    combinator assertions form a bounded distributive lattice. From the
    established laws we derive an efficient prototype implementation of
    lazy assertions for Haskell as a library.

<!-- -->

-   Peter A. Jonsson and Johan Nordlander. **Taming Code Explosion in
    Supercompilation**\
    \
    **Abstract:** Supercompilation algorithms can perform great
    optimizations but sometimes suffer from the problem of code
    explosion. This results in huge binaries which might hurt the
    performance on a modern processor. We present a supercompilation
    algorithm that is fast enough to speculatively supercompile
    expressions and discard the result if it turned out bad. This allows
    us to supercompile large parts of the imaginary and spectral parts
    of nofib in a matter of seconds while keeping the binary size
    increase below 5%.

<!-- -->

-   Jacques Carette, Mustafa Elsheikh and Spencer Smith. **A Generative
    Geometric Kernel**\
    \
    **Abstract:** We present the design and implementation of a
    generative geometric kernel. The kernel generator is generic,
    type-safe, parametrized by many design-level choices and extensible.
    The resulting code has minimal traces of the design abstractions. We
    achieve genericity through a layered design deriving concepts from
    affine geometry, linear algebra and abstract algebra. We achieve
    parametrization and type-safety by using OCaml\'s module system,
    including higher order modules. The cost of abstraction is removed
    by using
    [MetaOCaml[^?^](http://www.program-transformation.org/edit/PEPM11/MetaOCaml?topicparent=PEPM11.AcceptedPapers)]{.twikiNewLink
    style="background : #FFFFCE;"}\'s support for code generation
    coupled with some annotations atop the code type.

<!-- -->

-   Yan Wang and Veronica Gaspes. **An Embedded Language for Programming
    Protocol Stacks in Embedded Systems**\
    \
    **Abstract:** Protocol stack specifications are well-structured
    documents that follow a number of conventions and notations that
    have proven very useful for the design and dissemination of
    communication protocols.Protocol stack implementations on the other
    hand, are done in low-level languages, using error-prone programming
    techniques resulting in programs that are difficult to relate to the
    specifications,difficult to maintain, modify, extend and reuse. To
    overcome these problems we propose a domain-specific language that
    provides abstractions close to the notations used in protocol
    specifications.From descriptions in our language we generate C
    programs that can be integrated with other systems software. The
    language provides constructs to describe packet formats, including
    physical layout, constraints and dependencies. It also provides
    constructs for state machines and for layering protocols into
    stacks. Experiments show that the C programs we generate are
    comparable in performance and binary size to hand-crafted C
    programs.

**Tool demonstration papers:**

-   Elvira Albert, Richard Bubel, Samir Genaim, Reiner Hahnle, German
    Puebla and Guillermo Roman Diez. **Verified Resource Guarantees
    using COSTA and KeY**\
    \
    **Abstract:** Resource guarantees allow being certain that programs
    will run within the indicated amount of resources, which may refer
    to memory consumption, number of instructions executed, etc. This
    information can be very useful, especially in real-time and
    safety-critical applications. Nowadays, a number of automatic tools
    exist, often based on type systems or static analysis, which produce
    such resource guarantees. In spite of being based on theoretically
    sound techniques, the implemented tools may contain bugs which
    render the resource guarantees thus obtained not completely
    trustworthy. Performing full-blown verification of such tools is a
    daunting task, since they are large and complex. In this work we
    investigate an alternative approach whereby, instead of the tools,
    we formally verify the results of the tools. We have implemented
    this idea using COSTA, a state-of-the-art static analysis system,
    for producing resource guarantees and
    [KeY[^?^](http://www.program-transformation.org/edit/PEPM11/KeY?topicparent=PEPM11.AcceptedPapers)]{.twikiNewLink
    style="background : #FFFFCE;"}, a state-of-the-art verification
    tool, for formally verifying the correctness of such resource
    guarantees. Our preliminary results show that the proposed tool
    cooperation can be used for automatically producing verified
    resource guarantees.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
