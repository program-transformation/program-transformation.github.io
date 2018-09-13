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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoTutorialAtETAPS?t=1536825557)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoTutorialAtETAPS)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoTutorialAtETAPS)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoTutorialAtETAPS?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoTutorialAtETAPS?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Stratego/StrategoTutorialAtETAPS?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/StrategoTutorialAtETAPS?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Stratego/StrategoTutorialAtETAPS?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/StrategoTutorialAtETAPS?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/StrategoTutorialAtETAPS?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/StrategoTutorialAtETAPS?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoTutorialAtETAPS)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoTutorialAtETAPS?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoTutorialAtETAPS?template=oopsmore&param1=1.9&param2=1.9)
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
[]{#Strategies_for_Program_Transform} Strategies for Program Transformation
===========================================================================

[]{#Stratego_Tutorial_at_ETAPS} Stratego Tutorial at ETAPS
----------------------------------------------------------

Full Day Tutorial on April 14, 2002 at
[ETAPS](../Transform/ETAPS){.twikiLink} 2002 in Grenoble, France

------------------------------------------------------------------------

Handouts are now available from the
[StrategoDocumentation](StrategoDocumentation){.twikiLink} page

------------------------------------------------------------------------

**Abstract**

Program transformation has applications in many areas of software
engineering including compilation, optimization, refactoring, program
synthesis, software renovation, and reverse engineering. Program
transformation increases programmer productivity by automating
programming tasks, thus enabling programming at a higher-level of
abstraction, and increasing maintainability and re-usability.

This tutorial gives an introduction to principles and practice of
program transformation with rewriting strategies. Programmable rewriting
strategies allow the separation of transformation rules from the
strategies for applying them, thus providing support for concise,
declarative, and reusable specification of program transformation
systems.

The tutorial discusses all aspects of transformation with strategies;
after a taxonomy of program transformation and a discussion of program
representation, it covers specification of program transformations with
rewrite rules, combinators for composing rewriting strategies, in
particular combinators for generic traversal, exchange of
context-dependent information through scoped dynamic rewrite rules,
pragmatics of programming with strategies in Stratego, and applications
of these techniques.

**Contents**

::: {.twikiToc}
-   [Strategies for Program
    Transformation](StrategoTutorialAtETAPS#Strategies_for_Program_Transform)
    -   [Stratego Tutorial at
        ETAPS](StrategoTutorialAtETAPS#Stratego_Tutorial_at_ETAPS)
        -   [Introduction](StrategoTutorialAtETAPS#Introduction)
        -   [Material](StrategoTutorialAtETAPS#Material)
            -   [Program](StrategoTutorialAtETAPS#Program)
            -   [A Taxonomy of Program
                Transformation](StrategoTutorialAtETAPS#A_Taxonomy_of_Program_Transforma)
            -   [Program
                Representation](StrategoTutorialAtETAPS#Program_Representation)
            -   [Term Rewriting and Program
                Transformation](StrategoTutorialAtETAPS#Term_Rewriting_and_Program_Trans)
            -   [Rewriting
                Strategies](StrategoTutorialAtETAPS#Rewriting_Strategies)
            -   [Dynamic Rewrite
                Rules](StrategoTutorialAtETAPS#Dynamic_Rewrite_Rules)
            -   [Pragmatics](StrategoTutorialAtETAPS#Pragmatics)
            -   [Lab Session](StrategoTutorialAtETAPS#Lab_Session)
            -   [Applications](StrategoTutorialAtETAPS#Applications)
        -   [Audience](StrategoTutorialAtETAPS#Audience)
            -   [Relevance
                to](StrategoTutorialAtETAPS#Relevance_to_Transform_ETAPS_200)[ETAPS](../Transform/ETAPS){.twikiLink}
                2002
            -   [Intended
                Audience](StrategoTutorialAtETAPS#Intended_Audience)
            -   [Researchers](StrategoTutorialAtETAPS#Researchers)
            -   [Potential
                Users](StrategoTutorialAtETAPS#Potential_Users)
            -   [Required
                Background](StrategoTutorialAtETAPS#Required_Background)
            -   [Learning
                Objectives](StrategoTutorialAtETAPS#Learning_Objectives)
        -   [History of the
            Tutorial](StrategoTutorialAtETAPS#History_of_the_Tutorial)
        -   [Instructor](StrategoTutorialAtETAPS#Instructor)
:::

### []{#Introduction} Introduction

Program transformation has applications in many areas of software
engineering including compilation, optimization, refactoring, program
synthesis, software renovation, and reverse engineering. The aim of
program transformation is to increase programmer productivity by
automating programming tasks, thus enabling programming at a
higher-level of abstraction, and increasing maintainability and
re-usability.

Rewrite rules provide a good formalism for specification of basic
transformation steps. However, since sets of rewrite rules for a
programming language are usually not confluent and terminating, standard
rewriting techniques are not adequate for implementing program
transformation systems.

[Stratego](http://www.stratego-language.org) is a modular language for
the specification of fully automatic program transformation systems
based on the paradigm of rewriting strategies. Basic transformation
steps are defined using \_labeled conditional rewrite rules\_. Rules are
combined into complete transformations by means of programmable
[rewriting strategies](RewritingStrategy){.twikiLink}. An important
aspect of these strategies are combinators for generic traversal.
[Scoped dynamic rewrite rules](ScopedDynamicRewriteRules){.twikiLink}
overcome the limitations posed by the context-free nature of rewrite
rules. Together these features support concise and declarative
specification of program transformation systems. The Stratego
distribution contains the Stratego Compiler and the Stratego Standard
Library, and is distributed under the GNU General Public License.

This full day tutorial gives an introduction to principles and practice
of program transformation with rewriting strategies.

### []{#Material} Material

This section outlines the material presented in the tutorial. First an
overview of the tutorial is given in the form of a schedule.

#### []{#Program} Program

  --------------- ----------------------------------------------------
  9:00\--9:30     Introduction: A taxonomy of program transformation
  9:30\--10:00    Program representation
  10:15\--11:00   Term rewriting and program transformation
  11:15\--12:30   Rewriting strategies
  14:00\--14:45   Scoped dynamic rewrite rules
  15:00\--15:20   Pragmatics
  15:20\--16:20   Lab session: try it out yourself
  16:30\--17:30   Applications
  --------------- ----------------------------------------------------

The lab session in the afternoon is optional and depends on the interest
of the audience and the availability of computers. It can be skipped in
favour of a longer session about applications.

#### []{#A_Taxonomy_of_Program_Transforma} A Taxonomy of Program Transformation

Program transformation is used in many areas of software engineering,
including compiler construction, software visualization, documentation
generation, and automatic software renovation. At the basis of all these
different applications lie the main program transformation *scenarios*
of translation and rephrasing. These main scenarios can be refined into
a number of typical *sub-scenarios*.

In a *translating* scenario a program is transformed from a source
language into a program in a *different* target language. Examples of
translating scenarios are synthesis, migration, compilation, and
analysis. In
[ProgramSynthesis](../Transform/ProgramSynthesis){.twikiLink} an
implementation is derived from a high-level specification such that the
implementation satisfies the specification. A prime example of program
synthesis is parser generation. In
[ProgramMigration](../Transform/ProgramMigration){.twikiLink} a program
is transformed to another language. For example, transforming a
Fortran77 program to an equivalent Fortran90 program.
[ProgramCompilation](../Transform/ProgramCompilation){.twikiLink} is a
form of synthesis in which a program in a high-level language is
transformed to a program in a lower-level language. In
[ProgramAnalysis](../Transform/ProgramAnalysis){.twikiLink} a program is
reduced to some property, or value. Type-checking is an example of
program analysis.

In a rephrasing scenario a program is transformed into a different
program in the *same* language, i.e., source and target language are the
same. Examples of rephrasing scenarios are normalization, renovation,
refactoring, and optimization. In a *normalization* a program is reduced
to a program in a sub-language. In *renovation* some aspect of a program
is improved. For example, repairing a Y2K bug. A *refactoring* is a
transformation that improves the design of a program while preserving
its functionality. An *optimization* is transformation that improves the
run-time and/or space performance of the program.

The introduction session gives a short overview of the transformation
taxonomy with typical examples of the various transformations to put the
rest of the material into perspective.

#### []{#Program_Representation} Program Representation

Although some transformation systems work directly on text, in general a
textual representation is not adequate for performing complex
transformations. Therefore, a structured representation is used by most
systems. Since programs are written as texts by programmers, parsers are
needed to convert from text to structure and unparsers are needed to
convert structure to text.

A number of issues should be considered when choosing a program
representation: to use parse trees or abstract syntax trees, trees or
graphs, how to represent variables and variable bindings, and how to
exchange programs between transformation components.

In this session these issues are discussed and the ATerm representation
used in Stratego is presented. The ideas are illustrated with the
abstract syntax of several (small) languages that will be used in the
rest of the tutorial.

#### []{#Term_Rewriting_and_Program_Trans} Term Rewriting and Program Transformation

Rewrite rules provide a good formalism for expressing program
transformations. A rewrite rule defines a local transformation derived
from an algebraic equality of programs.

In this session the basics of term rewriting are reviewed including
rewrite rules, conditional rewrite rules, substitution, standard
(exhaustive) rewriting strategies, and the notions of confluence and
termination. The application of rewriting to program transformation is
illustrated using several examples.

#### []{#Rewriting_Strategies} Rewriting Strategies

Exhaustive application of all rules to the entire abstract syntax tree
of a program is not adequate for most transformation problems. The
system of rewrite rules expressing basic transformations is often
non-confluent and/or non-terminating.

An ad hoc solution that is often used is to encode control over the
application of rules into the rules themselves by introducing additional
function symbols. This intertwining of rules and strategy obscures the
underlying program equalities, incurs a programming penalty in the form
of rules that define a traversal through the abstract syntax tree, and
disables the reuse of rules in different transformations.

The paradigm of programmable rewriting strategies solves the problem of
control over the application of rules while maintaining the separation
of rules and strategies. A strategy is a little program that makes a
selection from the available rules and defines the order and position in
the tree for applying the rules. Thus rules remain pure, are not
intertwined with the strategy, and can be reused in multiple
transformations.

Support for strategies is provided by a number of transformation systems
in various forms. In [TAMPR](../Transform/TAMPR){.twikiLink} a
transformation is organized as a sequence of canonical forms. For each
canonical form a tree is normalized with respect to a subset of the
rules in the specification. [ELAN](../Transform/ELAN){.twikiLink}
provides non-deterministic sequential strategies. Stratego provides
generic primitive traversal operators that can be used to compose
generic tree traversal schemas. For more information about related
formalisms see [a survey of rewriting strategies in program
transformation
systems](../Transform/ASurveyOfRewritingStrategiesInProgramTransformationSystems){.twikiLink}.

In this central session of the tutorial the notion of a strategy is
defined and the operators for combining strategies are presented. In
particular, the specification of (generic) traversal strategies will get
much attention.

#### []{#Dynamic_Rewrite_Rules} Dynamic Rewrite Rules

Another problem of rewriting is the context-free nature of rewrite
rules. A rule has only knowledge of the construct it is transforming.
However, transformation problems are often context-sensitive. For
example, when inlining a function at a call site, the call is replaced
by the body of the function in which the actual parameters have been
substituted for the formal parameters. This requires that the formal
parameters and the body of the function are known at the call site, but
these are only available higher-up in the syntax tree.

There are many similar problems in program transformation; examples are
bound variable renaming, typechecking, constant and copy propagation,
and dead code elimination. Although the basic transformations in all
these applications can be expressed by means of rewrite rules, they need
contextual information.

The usual solution to this problem is to extend the traversal over the
tree (be it hand-written or generic) such that it distributes the data
needed by transformation rules. The disadvantage of these solutions is
that the traversal strategy becomes data heavy instead of just handling
control flow. That is, all traversal functions become infected with
additional parameters carrying context information.

The concept of [scoped dynamic rewrite
rules](ScopedDynamicRewriteRules){.twikiLink} is an extension of
rewriting strategies that overcomes the context-free nature of rewrite
rules. A dynamic rule is a normal rewrite rule that is generated at
run-time and that can access information from its generation context.
For example, to define an inliner, a rule that inlines function calls
for a specific function can be generated at the point where the function
is declared, and used at call sites of the function.

Dynamic rules are introduced using several examples: bound variable
renaming, function inlining, and dead code elimination.

#### []{#Pragmatics} Pragmatics

In this short session the pragmatics of working with Stratego are
discussed and demonstrated. First it is shown how to write, compile and
run Stratego programs. Then a short overview of the architecture of
transformation systems is given, including the specification of parsers
and pretty-printers using tools from [XT a bundle of program
transformation
tools](XTABundleOfProgramTransformationTools){.twikiLink}.

#### []{#Lab_Session} Lab Session

The lab session is an optional component of the tutorial. Depending on
feasibility (see below) and interest from the participants this session
can occupy the rest of the tutorial or be skipped in favour of a longer
session on applications.

In the lab session participants can try out the techniques presented in
the earlier sessions by writing several small Stratego programs solving
small transformation problems.

The lab session depends on the availability of computers. This requires
a room with computers running Linux or Unix with an installation of
XT-0.9 and the tutorial package. If it is not feasible to provide a
computer room for just one hour, an alternative solution is to have
participants bring their own laptops. It is conceivable that two
participants can work together on one laptop, such that not all
participants need computers. This requires that participants install the
software prior to the conference. A page on the stratego-language.org
site will provide download and installation instructions. Alternatively,
the lab session can be done in the form of a demonstration.

#### []{#Applications} Applications

The earlier sessions present the principles of transformation with
strategies using many examples. To consolidate the understanding of the
participants and to show more possibilities this session presents some
further applications from the following areas (depending on the interest
of the audience):

-   Compilation by transformation
-   Optimization
-   Refactoring
-   Document transformation (XML)
-   Program visualization

### []{#Audience} Audience

#### []{#Relevance_to_Transform_ETAPS_200} Relevance to [ETAPS](../Transform/ETAPS){.twikiLink} 2002

The material presented in this tutorial is closely related to the themes
of the CC and ESOP conferences and the LDTA workshop.

#### []{#Intended_Audience} Intended Audience

The tutorial is directed at researchers in the field of program
transformation and potential users, both academic and industrial.

#### []{#Researchers} Researchers

Researchers working on tools or formal methods for program
transformation can use the tutorial to get a complete overview of the
ideas underlying the strategic programming idiom. Either as a direct
source of study (the sources of Stratego and XT are available for
experimentation) or as inspiration for their own setting.

#### []{#Potential_Users} Potential Users

Academic and industrial developers of language processing systems such
as compilers, optimizers, program generators, and program visualization
tools can use the tutorial to learn to use a powerful set of tools for
compact implementation of their systems. The tools are readily available
and distributed under GNU GPL.

#### []{#Required_Background} Required Background

Participants are expected to have a basic understanding of compiler
construction and programming language syntax and semantics.

#### []{#Learning_Objectives} Learning Objectives

After the tutorial participants will understand the principles of
programming transformation systems with rewriting strategies. In
particular, they will understand the ideas and advantages of generic
term traversal and dynamic rules. With this understanding the
participants should be able to start writing Stratego specifications.

### []{#History_of_the_Tutorial} History of the Tutorial

The tutorial as proposed above has not been given before. The material
for the tutorial has evolved over the last couple of years for numerous
seminar presentations, several university lectures, and tutorials at
Stratego Users Days.

The [First Stratego Users Day](FirstStrategoUsersDay){.twikiLink} was
held in March 2000 at CWI, Amsterdam, The Netherlands and included a two
hour tutorial on the basics of program transformation with rewriting
strategies.

Prior to the [Second Stratego Users
Day](SecondStrategoUsersDay){.twikiLink} that was held in February 2001
at Utrecht University a full day tutorial was given about Stratego. The
tutorial was given in demonstration mode involving the participants in
solving several transformation problems.

The material for this tutorial draws on the material recently developed
for the course on [Software
Generation](http://www.stratego-language.org/Sg) taught at Utrecht
University in the academic years 2000\--2001 and 2001-2002.

### []{#Instructor} Instructor

Eelco Visser is

-   Designer of the [StrategoLanguage](StrategoLanguage){.twikiLink} and
    main implementor of the
    [StrategoCompiler](StrategoCompiler){.twikiLink} and
    [StrategoStandardLibrary[^?^](http://www.program-transformation.org/edit/Stratego/StrategoStandardLibrary?topicparent=Stratego.StrategoTutorialAtETAPS)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   One of developers of the XT bundle of transformation tools

<!-- -->

-   Designer of the Syntax Definition Formalism
    [SDF2](../Sdf/WebHome){.twikiLink} used in XT

<!-- -->

-   Author of numerous papers on program transformation, including
    papers on the design, implementation, and application of Stratego,
    and a recent survey exploring the role of rewriting strategies in
    program transformation

<!-- -->

-   Teacher of program transformation at Utrecht University

<!-- -->

-   Founder of [program-transformation.org](../index.html), a
    collaborative web-site based on wiki technology dedicated to
    surveying the field of program tranformation.

<!-- -->

-   Program committee member of the LDTA workshops in 2001 and 2003 and
    program chair of the RULE workshop on rule-based programming
    in 2002.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.StrategoTutorialAtETAPS moved from Stratego.EtapsTutorial on
06 Jan 2002 - 21:01 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Stratego/StrategoTutorialAtETAPS?newweb=Stratego&newtopic=EtapsTutorial&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
