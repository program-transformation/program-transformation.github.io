[]{#PageTop}

------------------------------------------------------------------------

+-----------------------+-----------------------+-----------------------+
| ![](http://www.progra | []{#2002_ACM_SIGPLAN} | ![](http://www.progra |
| m-transformation.org/ |  2002 ACM SIGPLAN     | m-transformation.org/ |
| acm.gif)              | --------------------- | acm.gif)              |
|                       | -----------------     |                       |
|                       |                       |                       |
|                       | Workshop on Rule-Base |                       |
|                       | d Programming         |                       |
|                       | ===================== |                       |
|                       | =============         |                       |
|                       |                       |                       |
|                       | ### []{#RuleProgram_W |                       |
|                       | orkshop_Program}[]{#_ |                       |
|                       | RuleProgram_Workshop_ |                       |
|                       | Program_} [Workshop P |                       |
|                       | rogram](RuleProgram){ |                       |
|                       | .twikiLink}           |                       |
|                       |                       |                       |
|                       | Satellite event of    |                       |
|                       | [PLI](PLI){.twikiLink |                       |
|                       | }\'02                 |                       |
|                       |                       |                       |
|                       | Saturday, October 5,  |                       |
|                       | 2002\                 |                       |
|                       | Pittsburgh, USA       |                       |
|                       |                       |                       |
|                       | [http://www.program-t |                       |
|                       | ransformation.org/Tra |                       |
|                       | nsform/WorkshopOnRule |                       |
|                       | BasedProgramming](Wor |                       |
|                       | kshopOnRuleBasedProgr |                       |
|                       | amming)               |                       |
+-----------------------+-----------------------+-----------------------+

------------------------------------------------------------------------

[Call for
Papers](pub/Transform/WorkshopOnRuleBasedProgramming/rule02-cfp.pdf)

------------------------------------------------------------------------

Program of the 2002 [ACM](ACM){.twikiLink}
[SIGPLAN](SIGPLAN){.twikiLink} [Workshop on Rule Based
Programming](WorkshopOnRuleBasedProgramming){.twikiLink}
([RULE](RULE){.twikiLink}\'02)

October 5, 2002, Pittsburgh, Pensylvania, USA.

  [Time](WorkshopOnRuleBasedProgramming@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Title](WorkshopOnRuleBasedProgramming@sortcol=1&table=1&up=0#sorted_table "Sort by this column")        [Authors](WorkshopOnRuleBasedProgramming@sortcol=2&table=1&up=0#sorted_table "Sort by this column")
  -------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------
  10:30                                                                                              Design Patterns for Functional Strategic Programming                                                     Ralf Laemmel (Vrije Universiteit) and Joost Visser ([CWI](CWI){.twikiLink})
  11:00                                                                                              Towards Generic Refactoring                                                                              Ralf Laemmel ([CWI](CWI){.twikiLink} &Vrije Universiteit)
  11:30                                                                                              Simple Termination of Context-Sensitive Rewriting                                                        Bernhard Gramlich (Technische Universitaet Wien) and Salvador Lucas (Universidad Politecnica de Valencia)
  12:00                                                                                              On Implementing Behavioral Rewriting                                                                     Grigore Rosu (University of Illinois at Urbana-Champaign)
  12:30                                                                                              *lunch*                                                                                                   
  14:00                                                                                              [BURG](BURG){.twikiLink}, IBURG, WBURG, GBURG: So Many Trees to Rewrite, So Little Time (Invited Talk)   Todd Proebsting (Microsoft Research)
  15:00                                                                                              Pattern-matching and Rewriting Rules for Group Indexed Data-Structure                                    Jean-Louis Giavitto and Olivier Michel (Universited Evry)
  15:30                                                                                              *Tea break*                                                                                               
  16:00                                                                                              A Rule-Based Language for Programming Software Updates                                                   Martin Erwig and Deling Ren (Oregon State University)
  16:30                                                                                              Some Prolog Macros for Rule-Based Programming: Why? How?                                                 Tim Menzies (University of West Virgina) and Lindsay Mason (University of British Columbia)
  17:00                                                                                              An Asynchronous Rule-Based Approach for Business Process Automation Using Obligations                    Alan Abrahams, David Eyers and Jean Bacon (University of Cambridge)

------------------------------------------------------------------------

### []{#Description} Description

The rule-based programming paradigm is characterized by the repeated,
localized transformation of a shared data object such as a term, graph,
proof, or constraint store. The transformations are described by *rules*
which separate the description of the sub-object to be replaced (the
*pattern*) from the calculation of the replacement. Optionally, rules
can have further conditions that restrict their applicability. The
transformations are controlled by explicit or implicit *strategies*.

The basic concepts of rule-based programming appear throughout computer
science, from theoretical foundations to practical implementations.
[Term rewriting](TermRewriting){.twikiLink} is used in semantics in
order to describe the meaning of programming languages, as well as in
the implementation of [program
transformation](ProgramTransformation){.twikiLink} systems. It is used
implicitly or explicitly to perform computations, e.g., in Mathematica,
OBJ, or [ELAN](ELAN){.twikiLink}, or to perform deductions, e.g., by
using inference rules to describe or implement a logic, theorem prover
or constraint solver. Extreme examples of rule-based programming include
the mail system in Unix which uses rules in order to rewrite mail
addresses to canonical forms, or the transition rules used in model
checkers.

Rule-based programming is currently experiencing a renewed period of
growth with the emergence of new concepts and systems that allow a
better understanding and better usability. On the theoretical side,
after the in-depth study of rewriting concepts during the eighties, the
nineties saw the emergence of the general concepts of rewriting logic
and of the rewriting calculus. On the practical side, new languages such
as ASM, [ASF+SDF](ASFandSDF){.twikiLink}, [BURG](BURG){.twikiLink},
Claire, [ELAN](ELAN){.twikiLink}, Maude, and
[Stratego](Stratego/StrategoLanguage){.twikiLink}, new systems such as
[LRR](LRR){.twikiLink} and commercial products such as [Ilog
Rules](IlogRules){.twikiLink} and [Eclipse](EclipseLanguage){.twikiLink}
have shown that rules are a useful programming tool.

The practical application of rule-based programming prompts research
into the algorithmic complexity and optimization of rule-based programs
as well as into the expressivity, semantics and implementation of
rules-based languages. Here, a particular focus is the use and specific
ation of strategies as a high-level control flow concept for the
application of the rules.

The purpose of this workshop is to bring together researchers from the
various communities working on rule-based programming to foster
fertilisation between theory and practice, as well as to favour the
growth of this programming paradigm.

### []{#Topics} Topics

We solicit original papers on all topics of rule-based programming,
including but not restricted to

-   Languages for rule-based programming
    -   Expressivity
    -   Semantics
    -   Implementation techniques
-   Applications of rule-based programming
    -   Analysis of rule-based programs
    -   Programming methods
-   Environments for rule-based programming
    -   (Partial) Evaluation
    -   Abstract machines for rewriting
-   Combination of rule-based programming with other paradigms
-   System descriptions

### []{#Invited_Speaker} Invited Speaker

-   [Todd Proebsting](ToddProebsting){.twikiLink} (Microsoft Research):
    BURG, IBURG, WBURG, GBURG: So Many Trees to Rewrite, So Little Time

### []{#Submission} Submission

Papers should not exceed 12 pages in length, including figures,
references, and appendices; authors should use at least a 10pt style.
Accepted papers will be published by [ACM](ACM){.twikiLink} and will
become part of the [ACM](ACM){.twikiLink} Digital Library.

For submission, a single self-contained .ps-file or .pdf-file should be
emailed to the program co-chairs

-   Bernd Fischer (<fisch@email.arc.nasa.gov>)
-   Eelco Visser (<visser@cs.uu.nl>)

no later than June 10, 2002. Please send a short email with title and
abstract to the program co-chairs no later than June 3, 2002, the
original deadline. Please make sure the files print on standard printers
- garbled submissions will not be reviewed!

### []{#Important_Dates} Important Dates

-   Abstract: June 3, 2002
-   Submission: June 10, 2002
-   Notification: August 10, 2002
-   Final version: August 19, 2002
-   Workshop: October 5, 2002

### []{#Past_Events} Past Events

-   PLI 2001: <http://www.cwi.nl/~markvdb/RULE2001/>
-   PLI 2000: <http://www.loria.fr/~ckirchne/=rule2000/>

### []{#Program} Program

-   [Accepted Papers](RuleAcceptedPapers){.twikiLink}
-   [Rule Program](RuleProgram){.twikiLink}
-   [Rule Proceedings](RuleProceedings){.twikiLink}

### []{#Program_Committee} Program Committee

[![](http://www.cs.ukc.ac.uk/people/staff/sjt/fdpe02/pli2002.gif){width="170"
height="215"}](http://pli2002.cs.brown.edu/)

-   [Mark van den Brand](MarkVanDenBrand){.twikiLink}
-   [James Cordy](JamesCordy){.twikiLink}
-   [Francois Fages](FrancoisFages){.twikiLink}
-   [Bernd Fischer](BerndFischer){.twikiLink} (Co-Chair)
-   [Thom
    Fruehwirth[^?^](http://www.program-transformation.org/edit/Transform/ThomFruehwirth?topicparent=Transform.WorkshopOnRuleBasedProgramming)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [Claude Kirchner](ClaudeKirchner){.twikiLink}
-   [Herbert Kuchen](HerbertKuchen){.twikiLink}
-   [Mark Minas](MarkMinas){.twikiLink}
-   [Oege de Moor](OegeDeMoor){.twikiLink}
-   [Eelco Visser](EelcoVisser){.twikiLink} (Co-Chair)

### []{#Organization} Organization

-   [Bernd Fischer](BerndFischer){.twikiLink}
-   [Eelco Visser](EelcoVisser){.twikiLink}

### []{#Conference_Venue_and_Related_Eve} Conference Venue and Related Events

[RULE](RULE){.twikiLink} 2002 is part of a federation of colloquia known
as Principles, Logics and Implementations of high-level programming
languages ([PLI](PLI){.twikiLink} 2002) which includes the
[ACM](ACM){.twikiLink} [SIGPLAN](SIGPLAN){.twikiLink} International
Conference on Functional Programming ([ICFP](ICFP){.twikiLink} 2002) and
the first [ACM](ACM){.twikiLink} [SIGPLAN](SIGPLAN){.twikiLink}
Conference on Generators and Components
([GCSE](GCSE){.twikiLink}/SAIG\'02) . The colloquia and affiliated
workshops will run from October 4 to October 8, 2002 and will be held in
Pittsburgh, USA. Details about the affiliated conferences and workshops
will appear at the [URL](URL){.twikiLink}
<http://pli2002.cs.brown.edu/>.

### []{#Call_for_Papers} Call for Papers

The call for papers is also available in
[PostScript](http://www.program-transformation.org/rule02/rule02-cfp.ps)
and [PDF](http://www.program-transformation.org/rule02/rule02-cfp.pdf).

------------------------------------------------------------------------

This web site is hosted by
[http://www.program-transformation.org](index.html)

[CategoryConference](CategoryConference){.twikiLink}

------------------------------------------------------------------------

[]{#PageBottom}
