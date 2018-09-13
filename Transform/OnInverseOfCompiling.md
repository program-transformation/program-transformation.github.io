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
    Page](http://www.program-transformation.org/edit/Transform/OnInverseOfCompiling?t=1536826524)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/OnInverseOfCompiling)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/OnInverseOfCompiling)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/OnInverseOfCompiling?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/OnInverseOfCompiling?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/OnInverseOfCompiling?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/OnInverseOfCompiling?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/OnInverseOfCompiling?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/OnInverseOfCompiling?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/OnInverseOfCompiling?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/OnInverseOfCompiling?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/OnInverseOfCompiling)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/OnInverseOfCompiling?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/OnInverseOfCompiling?template=oopsmore&param1=1.4&param2=1.4)
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
On Inverse Of Compiling {#on-inverse-of-compiling .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#ON_THE_INVERSE_OF_COMPILING} ON THE INVERSE OF COMPILING
------------------------------------------------------------

[]{#W_L_Caudle}

W.L. Caudle

[]{#Sperry_UNIVAC}

Sperry-UNIVAC

[]{#26_April_1980}

26 April 1980

### []{#1_INTRODUCTION} 1. INTRODUCTION

It is fitting that the subject of program conversion aids and
portability be a major topic at this conference held in San Diego. For,
it was from this city that the first decompiler description was
published by the late Dr. Maurice H. Halstead in his book entitled
Machine Independent Computer Programming\[20\]. Though its major topic
was the description of the ALGOL dialect called NELIAC, it contained a
brief report on the implementation of a decompiler for the UNIVAC M-460
Countess computer. That work was done under his direction at the Navy
Electronics Laboratory on Point Loma where he began his pioneering
efforts on portability, conversion aids, and, ultimately, the invariant
properties of languages \[18\].

At that time, high level languages (HLL) were in their infancy. There
was a continuing debate on the feasibility of programming any but the
most mundane of applications in HLL. The suggestion that a program
written in machine language could be translated automatically to NELIAC
was generally received as a jest. It is not surprising, then, that the
first decompiler got its motivation from a friendly wager that the
process was infeasible. There were the usual reasons for its
impossibility, such as \"there is no way to find out what the programmer
had in mind when the program was written.\" This is, of course,
irrelevant since a computer program must be completely unambiguous for
its correct operation. The term decompiler was coined then to identify
the inverse of compiling.

In addition to the M-460 decompiler, two other decompilers were
implemented with the guidance or consultation of Maury Halstead: the IBM
7094 to UNIVAC 1108 NELIAC decompiler at Lockheed Missiles and Space,
and the UNIVAC 494 to 1100 Series Inverse Compiler at Sperry\*UNIVAC in
Minnesota. This paper will describe some of the techniques, problems,
and experiences which are the result of the author\'s association with
the development of these two decompilers and their application within
conversion projects.

### []{#2_THE_INVERSE_OF_COMPILING} 2. THE INVERSE OF COMPILING

The inverse of compiling, or decompiling, is part of the idealized
software cycle: canonicalization, compilation, optimization, and
decompilation \[18\]. It is a natural process which is applied each time
a program is examined with the objective of abstracting its global
properties. Decompilation deals with the processes of raising the
language level from that in which a program is written to a level which
allows translation to a different language, and possible transport to a
different architecture, where the process is reversed by compiling.
Ideally, decompilation results in the complete decoupling of data and
algorithms, i.e., data declarations and procedures.

More commonly, decompiling applies to the conversion of a machine or
assembler program to HLL. However, many of the processes used in
decompilation are applicable to the conversion of HLL programs which
have not been written in an easily portable manner.

Decompiling is distinguished from other forms of language conversion,
such as direct translation, by the use of level raising techniques.
These techniques rely extensively upon the same kind of processes used
for optimization during compilation. However, optimization is not the
goal, for a compiler can accomplish this. Rather, the goal is the
representation of programs at a high level, with a minimum volume, to
achieve readability, maintainability, and portability.

Data base conversion is a related, and necessary, part of the conversion
process \[29,39,50,55\]. To be effective, a program conversion aid must
perform in tandem with a data base conversion aid. While the two
problems cannot be solved separately, this paper will concentrate on the
process of decompilation and its relation to data conversion, but not on
data base conversion itself.

### []{#3_AN_INVERSE_COMPILATION_MODEL} 3. AN INVERSE COMPILATION MODEL

There are several papers \[23,24,26,27,28,30,31\] which provide models
for the decompilation process, although there are few accounts of actual
implementations. The following model was implemented as the UNIVAC 494
to 1100 Series Inverse Compiler at the Roseville Software Development
Center in Minnesota. The model consists of the following processes:
input processing, basic block generation, local data usage analysis,
control and data flow analysis, data mapping, reporting, intermediate
form preparation, level transformations, and target language production.
The model is distinguished from prior models by the extensive use of
analysis techniques to derive data structures in recognition of the fact
that data conversion is of primary importance.

A general description of the model follows and includes some of the
problems in each of the processes involved. Major portions of the
processes are independent of the source architecture, and could be made
completely independent by using a machine description language \[4\] to
specify the machine language being decompiled.

#### []{#3_1_INPUT_PROCESSING} 3.1. INPUT PROCESSING

The minimum input required for this model is the absolute code of a
program which executes on the UNIVAC 494. In this case, language
statements produced by the decompiler will reference generated names,
unless names are present in the absolute in the form of diagnostic
tables.

If assembly and collection (linkage editor) listings are available in
machine readable form, these are used to supplement the information
derivable from the absolute program. Names are generated from these
sources where applicable. Note that raw source statements are not an
input: the information available from the source assembly and collection
listings replaces much processing which would be required if raw source
were used. Specifically, all of the mappings between labels and the
absolute code are obtainable from these listings.

The user interface provides a third form of input. It allows every kind
of information derived by the decompiler to be changed by the user, an
important facility for any conversion aid.

A Subprogram Library, accessible through the user interface, allows the
global properties of subprograms to be collected, either by the user
prior to processing or by the decompiler during its processing, so that
the decompilation of subprograms need only occur once. Through it, the
user can provide supplemental information such as calling sequences,
type of return, and data usage. This is valuable where unconventional
calling sequences are employed. Replacement routines can be defined so
that a substitute call is made wherever the original is encountered.

Finally, no changes to the program being converted are allowed either
prior to, or during, its decompilation. This is an important
requirement, since a change to a program should require revalidation of
the program prior to its decompilation.

#### []{#3_2_BASIC_BLOCK_GENERATION} 3.2. BASIC BLOCK GENERATION

This process identifies instructions and data by developing the basic
block structure and control flow graph of the program. Each basic block,
a sequence of instructions having a single entry and exit, is linked to
its predecessors and successors in control flow. Block generation begins
at the entry point to the program, which is obtained automatically or as
input by the user, and analyzes and simulates control flow variables,
iterating until no new links or blocks are found.

Since the identification of instruction blocks is performed without
knowledge of program input data values, it is usually incomplete and
requires some manual assistance. If assembly listings are part of the
input, the Disassembly Report provides an aid by flagging program words
which are coded as instructions, and which are not found within a basic
block. While an item is coded as an instruction in assembler language,
it need not actually be an instruction, or it may not be reachable by
program flow. It is not unusual to find instruction sequences which have
been isolated, but not removed, during maintenance operations.

#### []{#3_3_DATA_USAGE_ANALYSIS} 3.3. DATA USAGE ANALYSIS

Data usage analysis constructs the local view of operand usage. No
assumptions are made, that is, only those instructions which have been
found to reside in a basic block are examined to obtain operand usage.
The data type, data length, and reference type for each operand are
recorded in a local data dictionary. Machine registers are treated in
the same way as other instruction operands.

A classification is made of instructions by grouping them by their
general usage of operands. As an example, an integer add instruction and
a floating point add instruction are considered to be identical. This
classification greatly simplifies data flow analysis by providing a
smaller set of cases to consider. It also provides machine independence
to the process with its general treatment.

#### []{#3_4_CONTROL_AND_DATA_FLOW_ANALYS} 3.4. CONTROL AND DATA FLOW ANALYSIS

Using the derived control flow structure and the local data dictionary,
control flow analysis derives the interval and loop structure of the
program, and includes the computation of operand status, finally
resulting in reach information \[1\].

A critical part of the conversion of programs is the conversion of data,
both internal and external, to a form which is represented by the target
language and which represents the usage implied by the program. Data
flow analysis, based on control flow analysis, develops a global data
dictionary of operand usage to support the declaration of operands in
the target language. That analysis requires the propagation of local
type and length information to operands which can reach, and which can
be reached by, an operand reference from a basic block.

As a simple example of this process, consider the following instruction
sequence.

L AO,ABC Load register AO from ABC FA AO,FPT Floating add FPT to AO S
AO,DEF Store AO in DEF

The following inferences can be drawn:

ABC, FPT, and DEF are floating point operands If either AO or DEF are
busy on exit from the block containing these instructions, then the
floating point type can be propagated to the forward reached blocks If
ABC or FPT is busy on entry, then the floating point type can be
propagated to the backward reached blocks which reference them

This kind of analysis may also be used to determine various dependencies
among operands, such as input, output, control flow, and data bounding
operands. Length information is also propagated in order to derive
implied field definitions which are not explicit.

#### []{#3_5_DATA_MAPPING} 3.5. DATA MAPPING

The local and global data usage of operands are combined and used to
derive a data mapping from the source machine to the target machine.
This mapping is used as input to target language data declaration
production and is a major part of input required by a data base
conversion program.

In the UNIVAC 494 to 1100 Series application, the 30 bit word storage
and registers are mapped one-to-one into the 36 bit storage. Each
different usage of data then requires redefinition of the storage
involved. In the case of [COBOL](COBOL){.twikiLink} output, which has no
declarable pointer variables (for based addressing), special program
linking methods were employed to achieve the required mappings.

There are obvious problems with such a mapping, particularly where
multiple word compact operands are involved. These include double
precision or multiple word character operands. The problems caused by
such mappings depend on how the operands are referenced and what
percentage of code is affected. For the usual program, the percentage is
small or is localized. For some programs, such a mapping may render the
resulting program useless.

It is during the data mapping process that the results of data flow
analysis are indispensable. The concern is the relaxation of the strict
30 bit mapping to a 36 bit mapping so that a minimum of code is
generated during recompilation. For this purpose, as an example, the
knowledge that an operand is used, or contains results derived by, only
single precision binary integer arithmetic, allows the operand to be
mapped safely to a 36 bit full word in the target Language.

#### []{#3_6_REPORTS} 3.6. REPORTS

The reporting phase usually concludes the first attempt at decompiling a
program. The reports generated by this model provide the user with
information to aid completion of the decompilation.

A Disassembly report provides a listing of the program, in assembly code
format, showing the control flow structure, operand usage, and reach
information. It is a useful report even if the program is converted
manually.

A report on the data mapping is provided so that any particular data
item mapping can be changed, via the user interface, on a subsequent
decompilation of the same program.

Other reports include a basic block and block link listing, a cross
reference, and program statistics.

After analyzing these reports, providing additional information to
ensure that all basic blocks and links have been found, and verifying
data mappings, the complete process is repeated from the beginning: two
or three iterations are usually required. If no additional input is
necessary, then the decompilation is completed by specifying that the
target language is to be produced.

#### []{#3_7_INTERMEDIATE_FORM_PREPARATIO} 3.7. INTERMEDIATE FORM PREPARATION

Each instruction in a basic block is translated to an intermediate form
represented by an N-tuple. Twenty-five intermediate forms are provided
to represent all basic statement types, including labels, transfer of
control, and subroutine invocation. The N-tuples reference the Data
Dictionary and Data Map and provide a convenient machine independent
data structure for level transformations prior to generating the target
language statements.

#### []{#3_8_LEVEL_TRANSFORMATIONS} 3.8. LEVEL TRANSFORMATIONS

Level transformations are another objective of the analyses performed by
the decompiler and result in more compact, easily understandable, and
maintainable source language. Some of these, being of the form of
classical optimizations, could be provided by an optimizing compiler
during recompilation. However, this would not provide the natural,
readable expression of the statements which is the desired result.

Redundant operand references are removed. The majority of such redundant
references arise from operands which represent machine registers.

Subprogram calls are introduced at this point. The detection of
subprogram calls and the identification of actual and formal parameters
is, in general, an unsolved problem. However, the variety of calling
sequences found in assembler programs is limited, due to
standardization, and minimizes the effects of having an incomplete
general solution.

Conditional statements are transformed to minimize the number of
transfers needed to represent the conditions.

Translation of idioms must be performed to free the target program from
nonsensical expressions. An idiom is an instruction or group of
instructions which have an effect contrary to the usual or literal
meaning. Shifting to perform multiplication or division is a simple
idiom. As a more complex example, the particular conversion of integer
to floating point illustrated below is an idiom.

L A0,INT Load AO from integer INT OR A0,(0233000000000) OR in the
characteristic FA,U A1,0 Floating add to normalize S A1,REAL REAL is the
floating result

A direct translation of this sequence would generally result in an
incorrect result, since its correctness is dependent on mixed mode
arithmetic and the order of the instructions produced on recompilation.

#### []{#3_9_TARGET_LANGUAGE_PRODUCTION} 3.9. TARGET LANGUAGE PRODUCTION

The final step in this model is the production of the target language
statements to represent the program. No analysis is required in this
process; all statements are produced directly from the intermediate
forms using the data mapping table, the data dictionary, and the
Subprogram Library.

In the implementation of this model, two target languages were provided:
ASCII [COBOL](COBOL){.twikiLink} and PLUS, a Sperry\*UNIVAC systems
programming language. [COBOL](COBOL){.twikiLink} was added as the second
language and required only that the data mapping and target language
productions be modified.

### []{#4_INVERSE_COMPILATION_MAJOR_TECH} 4. INVERSE COMPILATION - MAJOR TECHNICAL PROBLEMS

The major technical problems in inverse compilation result primarily
from the incomplete specification of the input program by its code. That
is, while the code is an unambiguous statement of an algorithm, the
algorithm may also be highly data dependent in ways which are difficult
or impossible to derive from the code. Indeed, the control flow of the
program and the references it makes to data may not be identifiable
without the information which resides in possibly hundreds of data input
files.

It is easy to construct programs which are impossible to decompile with
complete success, either automatically or manually, from the program\'s
code. It is also easy to construct programs which do decompile with
complete success. What is the difference, and why aren\'t all programs
written so that the latter is achievable? Most likely, the lack of
portability objectives is the culprit.

The two examples below are simple demonstrations of intractable control
structures.

Example - Incomplete Subprogram Knowledge

I = RANDOM (expression) GO TO I

Example - External Data Dependency

READ (5, 50) I GO TO I

The first example above assumes that a function RANDOM computes an
integer label, of bounded value known by the programmer, which is used
to select the execution of the code at the label I. Unless the
decompiler can analyze the subroutine RANDOM, a complete control
structure cannot be determined. This example also demonstrates that
decompilation must be performed on complete program units, unless
information is provided for the missing units (e.g., through the
Subprogram Library facility of the model.)

In the second example, the control structure is determined from input to
the program, and cannot be determined by any amount of analysis which
does not consider data input.

In either of the examples, a data reference using the value of I as an
index, rather than to effect a control transfer, will result in an
indeterminate data structure.

These examples might lead a decompiler designer to consider the dynamic
analysis of programs together with appropriate sets of input data.
However, such analysis is expensive and guarantees failure, because the
appropriate data sets cannot be determined. It is simpler to allow the
user to supply the missing links directly.

Either of the examples above can be rewritten to provide the complete
specification of control paths by using conditional statements.

#### []{#4_1_CONTROL_FLOW_DETERMINATION} 4.1. CONTROL FLOW DETERMINATION

The examples above demonstrate some of the problems with basic block
generation. In the application of the block generation program at
Sperry\*Univac, about 95% of all blocks in the average program were
automatically identified with user input required to specify the missing
links, entries, and exits. It is possible, of course, that a single
missing link can hide 99% of the blocks on an initial run with the
decompiler.

While the process may find all blocks, it may not find all links, and
may result in incorrect level transformations.

#### []{#4_2_CONTROL_AND_DATA_FLOW_ANALYS} 4.2. CONTROL AND DATA FLOW ANALYSIS

Interval Analysis techniques require that either the control flow graph
be reducible, or that it be made reducible by node splitting \[1\].
Techniques for node splitting are available, but none provide an optimal
solution, That is, the number of nodes introduced may not be the minimum
possible and may incur a performance penalty on analysis using the
interval structure.

Programs written in assembler language are more likely, than are HLL
programs, to contain flow structures which are irreducible, because the
programmer has complete freedom to transfer into the middle of loops.
Thus for assembler language programs, irreducibility is a problem.

Data flow analysis and level transformations require a complete and
correct program flow structure. Bounds on data indices must be derivable
so that data structures can be identified and translated to a higher
level representation.

#### []{#4_3_ALGORITHM_SYNTHESIS} 4.3. ALGORITHM SYNTHESIS

The most complex of the problems remaining to be solved is that of
decoupling data structures and algorithms and representing these in a
form allowing an algorithm, which references different data structures,
to be synthesized. That is, if data structures are represented at a
higher level, then the algorithms which reference these must also be
translated to a higher level.

The simplest case of decoupling involves, for example, a load, add, and
store sequence. The problem here is to insure that mapping a word
reference into storage of possibly another size has no effect on the
result in the sequence.

Such transformations require complete identification of the use of each
data structure, not only by a single program, but also by all programs
which may reference it. This implies that decompilation, or conversion
of any sort, can not be done by considering only single programs,
Rather, the properties of a system of programs must be examined globally
to achieve the conversion. Just as optimization is made ineffective by
applying it to small units of code, decompilation is ineffective on
single routines or, in some cases single programs. The solution to
global examination of systems of programs may become possible with the
availability of such software support systems as RDL/RDP \[25\] which
may be employed to manage the global information.

#### []{#4_4_CHOICE_OF_A_TARGET_LANGUAGE} 4.4. CHOICE OF A TARGET LANGUAGE

Given the current state of the art in decompilation techniques, the
choice of a target language is critical. The language must be rich in
data declaration facilities, must allow the same storage to be described
with declarations of differing types, and must allow precise mapping
into the storage of the target system. The language must be capable of
high level expressions and must allow low level statements where
required. Low level statements are required to express instructions
which have no direct high level counterpart. Where low level language
statements are not available, assembler interfaces must be written.

### []{#5_EVALUATION_OF_DECOMPILATION_AS} 5. EVALUATION OF DECOMPILATION AS A CONVERSION AID

#### []{#5_1_FIGURE_OF_MERIT} 5.1. FIGURE OF MERIT

The evaluation of decompilation involves measuring its figure of merit,
that is, the removed cost in resources required to successfully convert
a program with the decompiler in ratio with the cost to convert the
program manually. Since such an evaluation is not usually practical, the
evaluation must deal with averages. While this may lead to dangerous
extrapolations in particular instances, it is nevertheless useful.

Based on results of studies and on the conversion of production programs
performed at Sperry\*UNIVAC and customer sites, the rate of conversion
using the decompiler is projected to be between 25 to 40 lines of
assembler code per programmer hour, or 150 to 320 lines per day. These
figures are based on expert usage of the tool and assume that the person
performing the conversion has comprehensive knowledge of the source and
target system and languages. They also assume a high degree of
motivation in the use of the decompiler.

As a comparison, figures provided by the Federal
[COBOL](COBOL){.twikiLink} Compiler Testing Service \[44\] specify a
potential manual conversion rate of 20 to 100 lines per man day for an
assembler to [COBOL](COBOL){.twikiLink}/FORTRAN manual conversion. This
indicates a figure of merit of 67 to 87 percent for the UNIVAC 494 to
1100 Series Inverse Compiler. On a conversion project using the IBM 7094
to NELIAC decompiler, rates as high as 250 lines per man day were
attained. This particular high rate was achieved on a 24000 line
assembler program which had no documentation, and which performed
primarily data decoding and reformatting. The high rate is partially
attributable to the similarities of the IBM 7094 and the UNIVAC 1108.

#### []{#5_2_COST} 5.2. COST

Over the Last twenty years, there have been many attempts, and some
successes, at developing usable conversion aids. There probably have
been many more conversion aids developed and discarded than there have
been conversion projects completed. It is relatively simple to develop
specific one-shot conversion aids which attack a few, common, conversion
problems. It is very difficult to develop a general conversion aid which
attacks all or most of the conversion problems. There is, in fact, a
point beyond which generality does not make good economic sense. That
point depends on the amount of conversion to be done, the cost to
increase generality, and the increase in the figure of merit of the
conversion aid \[21\].

The cost of a decompiler with a high figure of merit is similar to the
cost of a modern HLL compiler. Such cost cannot be amortized unless it
is used extensively, as in the case of a compiler. Because of the high
cost and of fear of conversion by users, it is unlikely that a
decompiler will be constructed other than at the direction of a computer
vendor, and then only if there is no alternative to migration. However,
the techniques involved in decompilation are widely applicable in other
areas of software development, and with the correct development
strategies, a decompiler may become a byproduct of other tools.

#### []{#5_3_WHAT_ME_USE_A_CONVERSION_AID} 5.3. WHAT? ME [USE](USE){.twikiLink} A CONVERSION AID?

In practice a conversion aid may turn out, instead, to be a hindrance.
This can happen even if the aid has a high figure of merit. The
individuals using the aid may be motivated against its use because they
have a need to show their creativity. While creativity is commendable,
it causes problems in conversion. This is a problem in the life of a
conversion project, regardless of the tools being used. Errors are
introduced by rewriting code that could have been translated
automatically. Problems are created by the refusal to admit that the
output of a good conversion aid, while not always esthetically pleasing,
is a giant step ahead of a rewrite from specifications, if any exist.

#### []{#6_APPLICATION_OF_TECHNIQUES_TO_O} 6. APPLICATION OF TECHNIQUES TO OTHER AREAS

Decompilation, when viewed as a method to raise the level of a language,
is applicable to areas of software development other than conversion.
The language being decompiled may be a HLL, a common intermediate
compiler language, or a design language. The result of such
decompilation may be another programming language, a design language, or
simply a tabulation of the properties of the language statements being
decompiled.

#### []{#6_1_CAPTURE_OF_EXISTING_DESIGN} 6.1. CAPTURE OF EXISTING DESIGN

The use of current design, analysis, and documentation tools such as
PSL/PSA of the ISDOS Project \[51\], or RDL/RDP at Sperry\*UNIVAC \[25\]
requires a large initial investment to capture the properties of code
which already exists. As with code conversion, the abstraction of design
information from existing code involves, at least in principle,
decompilation of the programs. While much of the information can be
derived quite easily, the abstraction of useful data structure
definitions is a nontrivial task, and involves global analysis
techniques such as are found in the decompilation model described in
this paper.

#### []{#6_2_DESIGN_CODE_VERIFICATION} 6.2. DESIGN/CODE VERIFICATION

In order to get software development on a solid foundation, the
verification that a particular implementation agrees with its
corresponding design must become possible by some automatic or
semiautomatic method.

Unless the refinement of design to increasingly lower levels is done
automatically, then it is necessary to verify that the lower level
description is consistent with the higher. If the design is recorded
using a design language such as RDL, then decompilation of the code or
intermediate level design statement can be used to check data
relationships and assertions against the design.

#### []{#7_SUMMARY} 7. SUMMARY

A decompiler model has been described which was implemented and which
achieved a relatively high figure of merit. There are, however, many
fundamental problems which remain to be solved before decompilation can
be considered as a generally accepted method of conversion. Why has
there been no solution to these problems? Admittedly, they are very
complex, but there has been very little visible evidence of any
concerted effort to solve them. A glance at the attached bibliography
contains only a few expositions on the techniques. No published account
of a commercial decompiler is to be found within the last ten years
\[21\].

The most recent survey of conversion techniques \[13\] indicates that a
general solution for decompilation, will not be seen within five years
(from 1978). This seems optimistic considering the amount of published
material on the subject. The problems remaining cannot be solved without
a firm foundation which goes far beyond that which now exists.

The problems which remain to be solved are not unique to decompilation
as a conversion tool. They appear in all aspects of software development
from definition and design through maintenance and evolution of systems.

With the explosion of hardware technology during the last decade and
that predicted for the next, and with the predicted shortage of software
professionals, conversion aids and portability will become increasingly
important, if not imperative, for the advancement of software
development.

Innovation by major computer vendors is seriously threatened by the
monumental conversion process required of its customer base that new
hardware and software systems have been canceled short of implementation
or release. All the while, more machine dependent software is produced
by computer vendors, users, and software houses. The cost of a solution
is high \-- the cost to do business without a solution is even higher.

#### []{#BIBLIOGRAPHY} BIBLIOGRAPHY

1\. Allen, F.E., Cocke, J. *A Program Data Flow Analysis Procedure*. CACM
19,3, (Mar 1976) pp 137-147.

2\. Baird, G.N. and Johnson, A.L. *System for Efficient Program
Portability*. Proc. AFIPS Natl. Comp. Conf. Expo. Vol. 43 (1974) p
423-429.

3\. Barbe, Penny. *Techniques for Automatic Program Translation*.
Software Engineering, Vol. 1, 1970, p 151-165. (CR21549).

4\. Boulton, P.I.P. and Goguen, J.R. *A Machine Description Language*.
Computing Journal (CB) 22,2, p 132-135, 1979.

5\. Boyce, Raymond F. *Topological Reorganization as an Aid to Program
Simplification*. PhD Thesis, Purdue University, June 1972.

6\. Brown P.J. (Ed) *Theory of Program Portability*. Software
portability: An Advanced Course, Cambridge Press, 1977, p 7-19.

7\. Buck, B.W., Evans, D.J. (Ed). *Conversion - a Doddle or a Disaster?*
Software World, Software 73, 1974, p 149-153.

8\. Cartmell, D.J. *The Intermediate Language (IL) Table*.
TM-555/050/009. Systems Development Corp., Santa Monica, California,
1972.

9\. Dahlstrand, I; Cowell, W. (Editor) *A Study of Portability in
Technical and Scientific Computing*. Portability of Numerical Software,
Springer-Verlag-Hill, p 529-539.

10\. Dellert, G. *A Use of Macros in Translation of Symbolic Assembly
Language of One Computer to Another*. CACM 8,12 (Dec 1963) p 742-748
(CR9336).

11\. Frailey, Dennis J. *A Study of Code Optimization Using a General
Purpose Optimizer*. PhD Thesis, Purdue University, Jan 1971.

12\. Friedman, Frank L. *Inverse Compilation Feasibility*. Proc.
[ACM](ACM){.twikiLink}\'74, San Diego, (Nov 1974) p 750.

13\. Fry, James P., et al. *Assessment of the Technology for Data and
Program Related Conversion*. Proc. AFIPS Natl. Computer Conf. Expo., Vol
47, 1978, p 887-907.

14\. Gaines, R. Stockton. *On the Translation of Machine Language
Programs*. CACM 8,12 (1965) p 736-741.

15\. Gordon W.L. *Liberator, The Concept and the Hardware*.
[ACM](ACM){.twikiLink} Symp. Reprogramming Problem, Princeton, New
Jersey, June, 1965.

16\. Graham S. *The Semi-Automatic Computer Conversion System (SACCS)*.
[ACM](ACM){.twikiLink} Symp. Reprogramming Problem, Priceton, New
Jersey, June, 1965.

17\. Gunn J.H. *Problems in Programming Interchangeability*. Symbolic
Languages in Data Processing, Gordon and Breach Science Publ., New York,
1962, p 770-790.

18\. Halstead, Maurice H. *Elements of Software Science*. Operating and
Programming Systems Series, Elsevier, 1977.

19\. \-\-\-\-\-\--. *Machine Independence and Third Generation Hardware*.
Proc. Spring Joint Computer Conference, 1967, p 587-592.

20\. \-\-\-\-\-\--. *Machine Independent Computer Programming*. Chapter
11, Decompiling. Spartan Books, Washington D.C., 1962.

21\. \-\-\-\-\-\--. *Using the Computer for Program Conversion*.
Datamation (May 1970) p 125-129.

22\. Halstead, Maurice H. and Bayer, Rudolf. *Algorithm Dynamics*. Purdue
University, May, 1972.

23\. Hollander, Clifford R. *Decompilation of Object Programs*. PhD
Thesis, Stanford University, Jan 1973.

24\. \-\-\-\-\-\--. *A Syntax-Directed Approach to Inverse Compilation*.
Proc. [ACM](ACM){.twikiLink}\'74, San Diego, Nov 1974, p 750.

25\. Heacox, H.C. *RDL: A Language for Software Development*.
[ACM](ACM){.twikiLink} [SIGPLAN](SIGPLAN){.twikiLink} Notices 12,12 (Dec
1979).

26\. Hopwood, Cregory L. *Inverse Compiling for Program Documentation*.
Proc. [ACM](ACM){.twikiLink}\'74, San Diego, Nov 1974, p 751.

27\. \-\-\-\-\-\--. *Decompilation*, PhD Dissertation, Dept. of
Information & Computer Science. U of Calif., Irvine, March 1978.

28\. Housel Barron C. *A Study of Decompiling Machine Languages into High
Level Machine Independant Languages*. PhD Thesis, Purdue University,
August 1973.

29\. \-\-\-\-\-\--. *A Unified Approach to Program and Data Conversion*.
Proc, Intl. Conf. on Very Large Data Bases, Oct 1977, p 327-335.

30\. \-\-\-\-\-\--. *On Inverse Translation of Machine Language*, Proc.
[ACM](ACM){.twikiLink}\'74, San Diego, Nov 1974, p 752.

31\. Housel, Barren C. and Halstead, M.H. *A Methodology for Machine
Language Decompilation.* IBM Research Report \#RJ1316, Dec 1973.

32\. IBM. *1400 Autocoder to [COBOL](COBOL){.twikiLink} Conversion Aid
Program.* (360 A-SE-19x), Version 2 Application Description Manual,
(GH29-1352-2), White Plains, N.Y. IBM 1967.

33\. Lichstein, Henry A. *When Should You Emulate?* Datamation. November,
1969, P 205-210.

34\. Lowry, Edward S. and Medlock, C.W. *Object Code Optimization.* CACM,
January 1969, p 13-23.

35\. McEwan, A. *An Atlas Autocode to Algol 60 Translator.* Computer
Journal 9,4 (Feb 1967) p 353-359, (CR12746).

36\. McKeeman, W.M. *Peephole Optimization.* CACM 8 (July 1965), p
443-444.

37\. Mendicino, Sam F.; Hughes Robert A; Martin, Jeanne T.; McMahon,
Frank H.; Ranelletti, John E.; and Swakenburg, Richard G. *The LRLTRAN
Compiler.* CACM, Nov 1968, p 747-755.

38\. Mock O.; Olsztyn, J.; Steel,T.; Teitter,A,; and Wegstein,J. \_The
Problem of Programming Communications with Changing Machines: A Proposed
Solution.\_ CACM 1,8 p 12-18; 1,9 p 9-15, (1958).

39\. Morenoff, E. *The Transferability of Computer Programs and the Data
on Which They Operate.* Proc. AFIPS Spring Joint Computer Conf., 1969, p
609-610, AFIPS Press, Montvale, New Jersey, 1969.

40\. Morenoff E. and McLean, J.B. *An Approach to Standardizing Computer
Systems.* Proc. Natl. [ACM](ACM){.twikiLink} Conf., Washington, D.C.,
1967, p 527-535, MOI Publ., 1969.

41\. Nunamaker, J.F.,Jr. Nylin, W.C.,Jr.; and Konsynski, Benn, Jr.
*Processing Systems Optimization Through Automatic Design and
Reorganization of Program Modules.* Purdue University, 1972.

42\. \-\-\-\-\-\--. *A Methodology for the Design and Optimization of
Information Processing Systems*, Proc, Spring Joint Comp. Conf. 1971, p
238-294,

43\. Nylin, William C., Jr. *Structural Reorganization of Multipass
Computer Programs.* PhD Thesis, Purdue University, June, 1972.

44\. Oliver, Paul. *Guidelines to Software Conversion.* Proc. AFIPS Natl.
Computer Conf. Expo., Vol 47, 1978, p 877-886.

45\. Olsen, T. *Philco/IBM Translation at Problem-Oriented, Symbolic and
Binary Levels.* [ACM](ACM){.twikiLink} Symp. Reprogramming Problem,
Princeton, New Jersey, June, 1965.

46\. Opler, A. *Automatic Program Translation.* Datamation, 9,5 (1963) pp
45-48.

47\. Opler, A., et al. *Automatic Translation of Programs from One
Computer to Another.* Information Processing, 1962, North-Holland
Publishing Co., Amsterdam, 1963. p 550-553.

48\. Pazel, D.P. *Mathematical Construct for Program Reorganization.* IBM
Journal of R&D., 19,6 (Nov 1975) p 575-581.

49\. Sassaman, W.A. *A Computer Program to Translate Machine Language
into FORTRAN.* Proc. Spring Joint Computer Conf. 1966. p 235-239.

50\. Su, Stanley Y.W. *Applications Program Conversion due to Data Base
Changes.* Proc. 2nd Intl. Conf. on Very Large Data Bases, 1977. p
143-157.

51\. Teichroew, D. and Hershey, E.A. *PSL/PSA: A Computer Aided Technique
for Structured Documentation and Analysis of Information Processing
Systems.* [IEEE](IEEE){.twikiLink} Trans. Soft. Eng. 3,1 (1977), p
41-48.

52\. Weller, Maria F. *A Pragmatic Look at Decompilation.* Proc.
[ACM](ACM){.twikiLink}\'74, San Diego, Nov 1974, p 753.

53\. Williams, Douglas A. *Conversion at Lockheed Missiles and Space.*
Datamation, January 1967, p 39-45.

54\. Wilson, Donald J. and Mossr David J. *CAT; A 7090-3600
Computer-Aided Translation.* CACM 8,12 (1965) p 777-781.

55\. Wolberg, J.R.; Rafal, M. *CONVERT - A Language for Program and Data
File Conversions.* Software Practice and Exp. 8,2 (Mar-Apr 1978) p
187-198.

------------------------------------------------------------------------

Copyright © 1998 Bill Caudle, All Rights Reserved.\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
