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
    Page](http://www.program-transformation.org/edit/Transform/HistoryOfDecompilation2?t=1536826289)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/HistoryOfDecompilation2)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/HistoryOfDecompilation2)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation2?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation2?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    20](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation2?rev=1.20)
    [(diff 19)](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation2?rev1=1.20&rev2=1.19)
-   [Rev
    19](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation2?rev=1.19)
    [(diff 18)](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation2?rev1=1.19&rev2=1.18)
-   [Rev
    18](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation2?rev=1.18)
    [(diff 17)](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation2?rev1=1.18&rev2=1.17)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation2)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/HistoryOfDecompilation2?template=oopsmore&param1=1.20&param2=1.20)
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
    \...](http://www.program-transformation.org/oops/Transform/HistoryOfDecompilation2?template=oopsmore&param1=1.20&param2=1.20)
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
History Of Decompilation 2 {#history-of-decompilation-2 .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#History_of_Decompilation_1980_19} History of Decompilation (1980-1999)
==========================================================================

See also [On the Inverse of
Compiling](OnInverseOfCompiling){.twikiLink}, April 1980.

[]{#TopicZebra}

### []{#Zebra_1981} Zebra, 1981

The Zebra prototype was developed at the Naval Underwater Systems Centre
in an attempt to achieve portability of assembler programs. Zebra took
as input a subset of the ULTRA/32 assembler, called AN/UYK-7, and
produced assembler for the PDP11/70. The project was described by
D.L.Brinkley in \[
[Brin81](HistoryOfDecompilation2#RefBrin81){.twikiAnchorLink} \].

The Zebra decompiler was composed of 3 passes: a lexical and flow
analysis pass, which parsed the program and performed control flow
analysis in the graph of basic blocks. The second pass was concerned
with the translation of the program to an intermediate form, and the
third pass simplified the intermediate representation by eliminating
extraneous loads and stores, in much the same way described by Housel \[
[Hous73](HistoryOfDecompilation2#RefHous73){.twikiAnchorLink} ,
[Hous73b](HistoryOfDecompilation2#RefHous73b){.twikiAnchorLink} \]. It
was concluded that it was hard to capture the semantics of the program
and that decompilationwas economically impractical, but it could aid in
the transportation process.

*This project made use of known technology to develop a decompiler of
assembler programs. No new concepts were introduced by this research,
but it raised the point that decompilation is to be used as a tool to
aid in the solution of a problem, but not as tool that will give all
solutions to the problem, given that a 100% correct decompiler cannot be
built.*

[]{#TopicDML}

### []{#Decompilation_of_DML_programs_19} Decompilation of DML programs, 1982

A decompiler of database code was designed to convert a subset of
Codasyl DML programs, written with procedural operations, into a
relational system with a nonprocedural query specification. An Access
Path Model is introduced to interpret the semantic accesses performed by
the program. In order to determine how FIND operations implement
semantic accesses, a global data flow reaching analysis is performed on
the control flow graph, and operations are matched to templates. The
final graph structures are remapped into a relational structure. This
method depends on the logical order of the objects and a standard
ordering of the DML statements \[
[Katz82](HistoryOfDecompilation2#RefKatz82){.twikiAnchorLink} \].

Another decompiler of database code was proposed to decompile well-coded
application programs into a proposed semantic representation is
described in \[
[Dors82](HistoryOfDecompilation2#RefDors82){.twikiAnchorLink} \]. This
work was induced by changes in the use requirements of a Database
Management System (DBMS), where application programs were written in
Cobol-DML. A decompiler of Cobol-DML programs was written to analyse and
convert application programs into a model and schema-independent
representation. This representation was later modified or restructured
to account for database changes. Language templates were used to match
against key instructions of a Cobol-DML programs.

*In the context of databases, decompilation is viewed as the process of
grouping a sequence of statements which represent a query into another
(nonprocedural) specification. Data flow analysis is required, but all
other stages of a decompiler are not implemented for this type of
application.*

[]{#TopicForth}

### []{#Forth_Decompiler_1982_1984} Forth Decompiler, 1982, 1984

A recursive Forth decompiler is a tool that scans through a compiled
dictionary entry and decompiles words into primitives and addresses \[
[Dudl82](HistoryOfDecompilation2#RefDud82){.twikiAnchorLink} \]. Such a
decompiler is considered one of the most useful tools in the Forth
toolbox \[ [Hill84](HistoryOfDecompilation2#RefHill84){.twikiAnchorLink}
\]. The decompiler implements a recursive descent parser so that
decompiled words can be decompiled in a recursive fashion.

*These works present a deparsing tool rather than a decompiler. The tool
recursively scans through a dictionary table and returns the primitives
or addresses associated with a given word.*

[]{#TopicDataflex}

### []{#Dataflex_Decompilers_1984} Dataflex Decompilers, 1984

DataFlex is a macro-based language. Some macros include over 80 DataFlex
commands in one macro command. The Database Managers company Dataflex
Decompilers have the capability of recovering the highest-level macro
command instead of the low-level commands that compose such a macro. The
techniques used in this decompiler include pattern matching and the
recovery of control structures such as if\'s and loops. The generated
code is functionally equivalent to the original source and is guaranteed
to be recompilable without changes.

[]{#TopicSoft}

### []{#Software_Transport_System_1985} Software Transport System, 1985

C.W.Yoo describes an automatic Software Transport System (STS) that
moves assembler code from one machine to another. The process involves
the decompilation of an assembler program for machine m1 to a high-level
language, and the compilation of this program in a machine m2 to
assembler. An experimental decompiler was developed on the Intel 8080
architecture; it took as input assembler programs and produced PL/M
programs. The recompiled PL/M programs were up to 23% more efficient
than their assembler counterpart. An experimental STS was developed to
develop a C cross-compiler for the Z-80 processor. The project
encountered problems in the lack of data type in the STS \[
[Woo85](HistoryOfDecompilation2#RefWoo85){.twikiAnchorLink} \].

The STS took as input an assembler program for machine m1 and an
assembler grammar for machine m2, and produced an assembler program for
machine m2. The input grammar was parsed and produced tables used by the
abstract syntax tree parser to parse the input assembler program and
generate an abstract syntax tree (AST) of the program. This AST was the
input to the decompiler, which then performed control and data flow
analyses, in much the same way described by Hollander \[
[Holl73](HistoryOfDecompilation2#RefHoll73){.twikiAnchorLink} \],
Friedman \[
[Frie74](HistoryOfDecompilation2#RefFrie74){.twikiAnchorLink} \], and
Barbe \[ [Barb74](HistoryOfDecompilation2#RefBarb74){.twikiAnchorLink}
\], and finally generated high-level code. The high-level language was
then compiled for machine m2.

*This work does not present any new research into the decompilation
area, but it does present a novel approach to the transportation of
assembler programs by means of a grammar describing the assembler
instructions of the target architecture.*

[]{#TopicDecomp}

### []{#Decomp_1988} Decomp, 1988

See [DecompDecompiler](DecompDecompiler){.twikiLink} for information
about a decompiler for the Vax BSD 4.2 which took as input object files,
and produced C-like programs.

[]{#TopicFermat}

### []{#FermaT_1989_to_present} [FermaT](FermaT){.twikiLink}, 1989 to present

[Martin Ward](MartinWard){.twikiLink}\'s PhD thesis \[
[War89](HistoryOfDecompilation2#RefWar89){.twikiAnchorLink} \] is about
formal, provable program transformations. He has written a program
transformation engine called [FermaT](FermaT){.twikiLink} which
facilitates forward and reverse engineering from assembly language to
specifications and back again. The technology is marketed through the
company [SoftwareMigrations](SoftwareMigrations){.twikiLink}. Real-world
decompilation of assembly language programs (such as IBM-370 assembler)
to C \[ [War99](HistoryOfDecompilation2#RefWar99){.twikiAnchorLink} \]
and [COBOL](COBOL){.twikiLink} have been performed, and recently from
80186 assembly language to C \[
[SML03](HistoryOfDecompilation2#RefSML03){.twikiAnchorLink} \].

[]{#TopicAustin}

### []{#exe2c_1990} exe2c, 1990

The Austin Code Works sponsored the development of the exe2c decompiler,
targetted at the PC compatible family of computers running the DOS
operating system \[
[Aust91](HistoryOfDecompilation2#RefAust91){.twikiAnchorLink} \]. The
project was announced in April 1990 \[
[Guth90](HistoryOfDecompilation2#RefGuth90){.twikiAnchorLink} \], tested
by about 20 people, and it was decided that it needed some more work to
decompile in C. A year later, the project reached a beta operational
level \[ [Guth91a](HistoryOfDecompilation2#RefGuth91a){.twikiAnchorLink}
\], but was never finished \[
[Guth91b](HistoryOfDecompilation2#RefGuth91b){.twikiAnchorLink} \]. I
([Cristina Cifuentes](CristinaCifuentes){.twikiLink}) was a beta tester
of this release.

exe2c is a multipass decompiler that consists of 3 programs: e2a,
a2aparse, and e2c. e2a is the disassembler. It converts executable files
to assembler, and produces a commented assembler listing as well.
e2aparse is the assembler to C front-end processor, which analyzes the
assembler file produced by e2a and generates .cod and .glb files.
Finally, the e2c program translates the files prepared by a2aparse and
generates pseudo-C. An integrated environment, envmnu, is also provided.

Programs decompiled by exe2c make use of a header file that defines
registers, types and macros. The output C programs are hard to
understand because they rely on registers and condition codes
(represented by Boolean variables). Normally, one machine instruction is
decompiled into one or more C instructions that perform the required
operation on registers, and set up condition codes if required by the
instruction. Expressions and arguments to subroutines are not
determined, and a local stack is used for the final C programs. It is
obvious from this output code that a data flow analysis was not
implemented in exe2c. This decompiler has implemented a control flow
analysis stage; looping and conditional constructs are available. The
choice of control constructs is generally adequate. Case tables are not
detected correctly, though. The number and type of procedures decompiled
shows that all library routines, and compiler start-up code and runtime
support routines found in the program are decompiled. The nature of
these routines is normally low-level, as they are normally written in
assembler. These routines are hard to decompile as, in most cases, there
is no high-level counterpart (unless it is low-level type C code).

*This decompiler is a first effort in many years to decompile executable
files. The results show that a data flow analysis and heuristics are
required to produce better C code. Also, a mechanism to skip all
extraneous code introduced by the compiler and to detect library
subroutines would be beneficial.*

[]{#TopicPLM}

### []{#PLM_80_Decompiler_1991} PLM-80 Decompiler, 1991

The Information Technology Division of the Australian Department of
Defence researched into decompilation for defence applications, such as
maintenance of obsolete code, production of scientific and technical
intelligence, and assessment of systems for hazards to safety or
security. This work was described by S.T. Hood in \[
[Hood91](HistoryOfDecompilation2#RefHood91){.twikiAnchorLink} \].

Techniques for the construction of decompilers using definite-clause
grammars, an extension of context-free grammars, in a Prolog environment
are described. A Prolog database is used to store the initial assembler
code and the recognised syntactic structures of the grammar. A prototype
decompiler for Intel 8085 assembler programs compiled by a PLM-80
compiler was written in Prolog. The decompiler produced target programs
in Small-C, a subset of the C language. The definite-clause grammar
given in this report was capable of recognizing if-then control
structures, and while loops, as well as static (global) and automatic
(local) variables of simple types (i.e. character, integers, and longs).
A graphical user interface was written to display the assembler and
pseudo-C programs, and to enable the user to assign variable names, and
comments. This interface also asked the user for the entry point to the
main program, and allowed him to select the control construct to be
recognized.

*The analysis performed by this decompiler is limited to the recognition
of control structures and simple data types. No analysis on the use of
registers is done or mentioned. Automatic variables are represented by
an indexed variable that represents the stack. The graphical interface
helps the user document the decompiled program by means of comments and
meaningful variable names. This analysis does not support optimized
code.*

[]{#TopicOGorman}

### []{#J_O_Gorman_PhD_thesis_1991} J. O\'Gorman PhD thesis, 1991

The Systematic Decompilation thesis by John O\'Gorman \[
[OGor91](HistoryOfDecompilation2#RefOGor91){.twikiAnchorLink} \],
University of Limerick, describes a pattern matching technique used for
decompiling VAX binaries into Pascal source code. The technique requires
the availability of the compiler used, performs a coverage of constructs
available in the language, and creates small test programs that use the
constructs, in order to derive the patterns of machine code used for
each high-level construct. When decompiling a Pascal executable, the
patterns are matched to determine which Pascal construct to recreated.
Unoptimized code is used.

The thesis is available for downloading (ftp) in postscript format:
<ftp://www.csis.ul.ie/techrpts/ul-91-12.ps>.

[]{#TopicDecompComp}

### []{#Decompiler_compiler_1991_1994} Decompiler compiler, 1991-1994

A decompiler compiler is a tool that takes as input a compiler
specification and the corresponding portions of object code, and returns
the code for a decompiler; i.e. it is an automatic way of generating
decompilers, much in the same way that yacc is used to generate
compilers \[
[Bowe91a](HistoryOfDecompilation2#RefBowe91a){.twikiAnchorLink},
[Bowe91b](HistoryOfDecompilation2#RefBowe91b){.twikiAnchorLink},
[Breu94](HistoryOfDecompilation2#RefBreu94){.twikiAnchorLink} \].

Two approaches are described to generate such a decompiler compiler: a
logic and a functional programming approach. The former approach makes
use of the bidirectionality of logic programming languages such as
Prolog, and runs the specification of the compiler backwards to obtain a
decompiler \[Bowe91a, Bowe91b, Bowe93b\]. In theory this is correct, but
in practice this approach is limited to the implementation of the Prolog
interpreter, and therefore problems of strictness and reversibility are
encountered \[
[Breu92](HistoryOfDecompilation2#RefBreu92){.twikiAnchorLink},
[Breu93](HistoryOfDecompilation2#RefBreu93){.twikiAnchorLink} \]. The
latter approach is based on the logic approach but makes use of lazy
functional programming languages like Haskell, to generate a more
efficient decompiler \[
[aBowe91a](HistoryOfDecompilation2#RefBowe91){.twikiAnchorLink},
[Bowe91b](HistoryOfDecompilation2#RefBowe91b){.twikiAnchorLink},
[Bowe93b](HistoryOfDecompilation2#RefBowe93b){.twikiAnchorLink} \]. Even
if a non-lazy functional language is to be used, laziness can be
simulated in the form of objects rather than lists.

The decompiler produced by a decompiler compiler will take as input
object code and return a list of source codes that can be compiled to
the given object code. In order to achieve this, an enumeration of all
possible source codes would be required, given a description of an
arbitrary inherited attribute grammar. It is proved that such an
enumeration is equivalent to the Halting Problem \[
[Breu92](HistoryOfDecompilation2#RefBreu92){.twikiAnchorLink},
[Breu93](HistoryOfDecompilation2#RefBreu93){.twikiAnchorLink} \], and is
therefore non-computable. Even further, there is no computable method
which takes an attribute grammar description and decides whether or not
the compiled code will give a terminating enumeration for a given value
of the attribute \[
[Breu92](HistoryOfDecompilation2#RefBreu92){.twikiAnchorLink},
[Breu93](HistoryOfDecompilation2#RefBreu93){.twikiAnchorLink} \], so it
is not straightforward which grammars can be used. Therefore, the class
of grammars acceptable to this method needs to be restricted to those
that produce a complete enumeration, such as non left-recursive
grammars.

An implementation of this method was firstly done for a subset of an
Occam-like language using a functional programming language. The
decompiler grammar was an inherited attribute grammar which took the
intended object code as an argument \[
[Breu92](HistoryOfDecompilation2#RefBreu92){.twikiAnchorLink},
[Breu93](HistoryOfDecompilation2#RefBreu93){.twikiAnchorLink} \]. A
Prolog decompiler was also described based on the compiler
specification. This decompiler applied the clauses of the compiler in a
selective and ordered way, so that the problem of non-termination would
not be met, and only a subset of the source code programs would be
returned (rather than an infinite list) \[
[Bowe91c](HistoryOfDecompilation2#RefBowe91c){.twikiAnchorLink},
[Bowe93](HistoryOfDecompilation2#RefBowe93){.twikiAnchorLink} \].
Recently, this method made use of an imperative programming language,
C++, due to the inefficiencies of the functional and logic approach. In
this prototype, C++ object\'s were used as lazy lists, and a set of
library functions was written to implement the operators of the
intermediate representation used \[
[Breu94](HistoryOfDecompilation2#RefBreu94){.twikiAnchorLink} \].
Problems with optimized code have been detected.

*As illustrated by this research, decompiler compilers can be
constructed automatically if the set of compiler specifications and
object code produced for each clause of the specification is known. In
general, this is not the case as compiler writers do not disclose their
compiler specifications. Only customized compilers and decompilers can
be built by this method. It is also noted that optimizations produced by
the optimization stage of a compiler are not handled by this method, and
that real executable programs cannot be decompiled by the decompilers
generated by the method described. The problem of separating
instructions from data is not addressed, nor is the problem of
determining the data types of variables used in the executable program.
In conclusion, decompiler compilers can be generated automatically if
the object code produced by a compiler is known, but the generated
decompilers cannot decompile arbitrary executable programs.*

[]{#TopicEightOhEightSix}

### []{#8086_C_Decompiling_System_1991_1} 8086 C Decompiling System, 1991-1993

This decompiler takes as input executable files from a DOS environment
and produces C programs. The input files need to be compiled with
Microsoft C version 5.0 in the small memory model \[
[Fuan93](HistoryOfDecompilation2#RefFuan93){.twikiAnchorLink} \]. Five
phases were described: recognition of library functions, symbolic
execution, recognition of data types, program transformation, and C code
generation. The recognition of library functions and intermediate
language was further described in \[
[Fuan91](HistoryOfDecompilation2#RefFuan91){.twikiAnchorLink},
[Hung91](HistoryOfDecompilation2#RefHung91){.twikiAnchorLink} \].

The recognition of library functions for Microsoft C was done to
eliminate subroutines that were part of a library, and therefore produce
C code for only the user routines. A table of C library functions is
built-into the decompiling system. For each library function, its name,
characteristic code (sequence of instructions that distinguish this
function from any other function), number of instructions in the
characteristic code, and method to recognize the function were stored.
This was done manually by the decompiler writer. The symbolic execution
translated machine instructions to intermediate instructions, and
represented each instruction in terms of its symbolic contents. The
recognition of data types is done by a set of rules for the collection
of information on different data types and analysis rules to determine
the data type in use. The program transformation transforms storage
calculation into address expressions, e.g. array addressing. Finally,
the C code generator transforms the program structure by finding control
structures, and generates C code.

8086C seems to be based on a Unix/68000 decompiler called 68000C \[
[Zong88](HistoryOfDecompilation2#RefZong88){.twikiAnchorLink} \]. See
also [DECLER](HistoryOfDecompilation2#TopicDECLER){.twikiAnchorLink}.

*This decompiling system makes use of library function recognition to
generate more readable C programs. The method of library recognition is
hand-crafted, and therefore inefficient if other versions of the
compiler, other memory models, or other compilers were used to compile
the original programs. The recognition of data types is a first attempt
to recognize types of arrays, pointers and structures, but not much
detail is given in the paper. No description is given as to how an
address expression is reached in the intermediate code, and no examples
are given to show the quality of the final C programs.*

[]{#TopicAlpha}

### []{#Alpha_AXP_Migration_Tools_1993} Alpha AXP Migration Tools, 1993

When Digital Equipment Corporation designed the Alpha AXP architecture,
the AXP team got involved in a project to run existing VAX and MIPS code
on the new Alpha AXP computers. They opted for a binary translator which
would convert a sequence of instructions of the old architecture into a
sequence of instructions of the new architecture. The process needed to
be fully automatic and to cater for code created or modified during
execution. Two parts to the migration process were defined: a binary
translation, and a runtime environment \[
[Site93](HistoryOfDecompilation2#RefSite93){.twikiAnchorLink} \].

The binary translation phase took binary programs and translated them
into AXP opcodes. It made use of decompilation techniques to understand
the underlying meaning of the machine instructions. Condition code usage
analysis was performed as these conditions do not exist on the Alpha
architecture. The code was also analyzed to determine function return
values and find bugs (e.g. uninitialized variables). MIPS has standard
library routines which are embedded in the binary program. In this case,
a pattern matching algorithm was used to detect routines that were
library routines, such routines were not analysed but replaced by their
name. Idioms were also found and replaced by an optimal instruction
sequence. Finally, code was generated in the form of AXP opcodes. The
new binary file had both, the new code and the old code.

The runtime environment executes the translated code and acts as a
bridge between the new and old operating systems (e.g. different calling
standards, exception handling). It had a built-in interpreter of old
code to run old code not discovered or nonexistent at translation time.
This was possible because the old code was also saved as part of the new
binary file.

Two binary translators were written: VEST, to translate from the OpenVMS
VAX system to the OpenVMS AXP system, and mx, to translate ULTRIX MIPS
images to DEC OSF/1 AXP images. The runtime environments for these
translators were TIE and mxr respectively.

*This project illustrates the use of decompilation techniques in a
modern translation system. It proved successful for a large class of
binary programs. Some of the programs that could not be translated were
programs that were technically infeasible to translate, such as programs
that use privileged opcodes, or run with superuser privileges.*

[]{#TopicSourcePROM}

### []{#Source_PROM_Comparator_1993} Source/PROM Comparator, 1993

A tool to demonstrate the equivalence of source code and PROM contents
was developed at the Nuclear Electric plc, UK, to verify the correct
translation of PL/M-86 programs into PROM programs executed by safety
critical computer controlled systems \[
[Pave93](HistoryOfDecompilation2#RefPave93){.twikiAnchorLink} \].

Three stages are identified: the reconstitution of object code files
from the PROM files, the disassembly of object code to an assembler-like
form with help from a name-table built up from the source code, and
decompilation of assembler programs and comparison with the original
source code. In the decompiling stage, it was noted that it was
necessary to eliminate intermediate jumps, registers and stack
operations, identify procedure arguments, resolve indexes of structures,
arrays and pointers, and convert the expresssions to a normal form. In
order to compare the original program and the decompiled program, an
intermediate language was used. The source program was translated to
this language with the use of a commercial product, and the output of
the decompilation stage was written in the same language. The project
proved to be a practical way of verifying the correctness of translated
code, and to demonstrate that the tools used to create the programs
(compiler, linker, optimizer) behave reliably for the particular safety
system analyzed.

*This project describes a use of decompilation techniques, to help
demonstrate the equivalence of high-level and low-level code in a
safety-critical system. The decompilation stage performs much of the
analysis, with help from a symbol table constructed from the original
source program. The task is simplified by the knowledge of the compiler
used to compile the high-level programs.*

[]{#TopicDCC}

### []{#Cristina_Cifuentes_PhD_Thesis_Re}[]{#_Cristina_Cifuentes_PhD_Thesis_R} [Cristina Cifuentes](CristinaCifuentes){.twikiLink}\' PhD Thesis \"Reverse Compilation Techniques\", 1994

Considered by some to be the definitive work on general decompilation
from binary files. You can download the thesis from [Cristina
Cifuentes](CristinaCifuentes){.twikiLink}\' page, as a compressed
postscript file (474K). This work draws heavily on standard forward
engineering techniques such as data flow analysis, applied to
decompilation. Similarly, graph techniques are used to restructure the
generated code into standard loops, conditional statements, and other
high level constructs. Type recovery is limited to built-in types (no
arrays or structures). Cristina demonstrated her techniques in a
research prototype called
[dcc](http://www.itee.uq.edu.au/~cristina/dcc.html).

After her PhD, Cristina worked for some years on [Binary
Translation](http://www.program-transformation.org/twiki/bin/view/Transform/BinaryTranslation),
for example see the [UQBT
page](http://www.itee.uq.edu.au/~cristina/uqbt.html). Cristina is
currently associate advisor for [Mike Van
Emmerik](MikeVanEmmerik){.twikiLink}\'s current PhD research, also on
decompilation.

[]{#TopicDECLER}

### []{#DECLER_Decompiler_1995} DECLER Decompiler, 1995

DECLER \[ [DRM95](HistoryOfDecompilation2#RefDRM95){.twikiAnchorLink}
\], \[ [Zong96](HistoryOfDecompilation2#RefZong96){.twikiAnchorLink} \],
\[ [CL00](HistoryOfDecompilation2#RefCL00){.twikiAnchorLink} \] is a
five stage decompiler, based on
[8086C](HistoryOfDecompilation2#TopicEightOhEightSix){.twikiAnchorLink}
and 68000C. The stages are disassembler, library function recogniser,
symbolic executer, \"AB transformer\", and \"C transformer\". The AB
transformer appears to be a formal transformation system that recovers
types as a side effect. The C transformer is the structuring back end.

[]{#TopicUQBT}

### []{#University_of_Queensland_Binary}[]{#University_of_Queensland_Binary_} University of Queensland Binary Translator, 1997-2001

The University of Queensland Binary Translator (UQBT), 1997-2001 . This
Binary Translator uses a standard C compiler as the \"back end\"; in
other words, it emits C source code. However, this is not the same as a
decompiler, where the goal is human readable high level code. As a
result, UQBT can\'t be used in any of the applications that come under
the heading of \"comprehension aid\" or \"maintainable code\". Work on
UQBT was not completed, however it was capable of producing low level
source code for moderate sized programs, such as the smaller SPEC
benchmarks \[
[CVE00](HistoryOfDecompilation2#RefCVE00){.twikiAnchorLink},
[CVEU+99](HistoryOfDecompilation2#RefCVEU99){.twikiAnchorLink} \].

[]{#TopicMycroft}

### []{#A_Mycroft_s_Type_Reconstruction}[]{#A_Mycroft_s_Type_Reconstruction_} A. Mycroft\'s Type Reconstruction for Decompilation, 1999

One of the hardest problems to solve in decompilation is that of
recovering high-level data types from machine code in a correct way.
Such types include structures, arrays and more. In this work, Alan
Mycroft presents a system for infering high-level types from
assembler-based (RTL) code \[
[Mycr99](HistoryOfDecompilation2#RefMycr99){.twikiAnchorLink} \].
Alan\'s type inference system is based on Milner\'s work for ML. The
paper presents a type system, the constraints on types and
worked-through examples that include structures and arrays as part of
their output. Experimental results for the system are not available.

This is the best type system that I am aware of that currently deals
with recoverying high-level data types in a machine-independent way, as
it is based on RTLs and makes no unreasonable assumptions on the shape
of the RTLs. Implementation results are needed in order to determine how
feasible this system is in real practice.

[History Of Decompilation 1](HistoryOfDecompilation1){.twikiLink}
(1960-1979)\
[History Of Decompilation 3](HistoryOfDecompilation3){.twikiLink}
(2000-present)

------------------------------------------------------------------------

#### []{#References} References

[]{#RefHoll73}

 Holl73
:   C.R. Hollander. Decompilation of Object Programs. PhD dissertation,
    Stanford University, Computer Science, January 1973.

[]{#RefHous73}

 Hous73
:   B.C. Housel. A Study of Decompiling Machine Languages into
    High-Level Machine Independent Languages. PhD dissertation, Purdue
    University, Computer Science, August 1973.

[]{#RefHous73b}

 Hous73b
:   B.C. Housel and M.H. Halstead. A methodology for machine language
    decompilation. Technical Report RJ 1316 (\#20557), Purdue
    University, Department of Computer Science, December 1973.

[]{#RefBarb74}

 Barb74
:   P. Barbe. The Piler system of computer program translation.
    Technical report, Probe Consultants Inc., September 1974.

[]{#RefFrie74}

 Frie74
:   F.L. Friedman. Decompilation and the Transfer of Mini-Computer
    Operating Systems. PhD dissertation, Purdue University, Computer
    Science, August 1974.

[]{#RefBake77}

 Bake77
:   B.S. Baker. An algorithm for structuring flowgraphs. Journal of the
    [ACM](ACM){.twikiLink}, 24(1):98-120, January 1977.

[]{#RefBrin81}

 Brin81
:   D.L. Brinkley. Intercomputer transportation of assembly language
    software through decompilation. Technical report, Naval Underwater
    Systems Center, October 1981.

[]{#RefBert81}

 Bert81
:   M.N. Bert and L. Petrone. Decompiling context-free languages from
    their Polish-like representations. pages 35-57, 1981.

[]{#RefKatz82}

 Katz82
:   R.H. Katz and E. Wong. Decompiling CODASYL DML into relational
    queries. [ACM](ACM){.twikiLink} Transactions on Database Systems,
    7(1):1-23, March 1982.

[]{#RefDors82}

 Dors82
:   L.M. Dorsey and S.Y. Su. The decompilation of
    [COBOL](COBOL){.twikiLink}-DML programs for the purpose of program
    conversion. In Proceedings of [COMPSAC](COMPSAC){.twikiLink} 82.
    [IEEE](IEEE){.twikiLink} Computer Society\'s Sixth International
    Computer Software and Applications Conference, pages 495-504,
    Chicago, USA, November 1982. [IEEE](IEEE){.twikiLink}.

[]{#RefDud82}

 Dudl82
:   R. Dudley. A recursive decompiler. FORTH Dimensions, 4(2):28,
    Jul-Aug 1982.

[]{#RefHill84}

 Hill84
:   N.L. Hills and D. Moines. Revisited: Recursive decompiler. FORTH
    Dimensions, 5(6):16-18, Mar-Apr 1984.

[]{#RefWoo85}

 Woo85
:   C.W. Yoo. An approach to the transportation of computer software.
    Information Processing Letters, 21:153-157, September 1985.

[]{#RefMay88}

 May88
:   W. May. A simple decompiler. Dr.Dobb\'s Journal, pages 50-52,
    June 1988.

[]{#RefReut88}

 Reut88
:   J. Reuter. Formerly available from
    <ftp://ftp.cs.washington.edu/pub/decomp.tar.Z>. Public domain
    software, 1988. Now downloadable from the
    [DecompDecompiler](DecompDecompiler){.twikiLink} page.

[]{#RefZong88}

 Zong88
:   Liu Zongtian and Zhu Yifen, The Application of the Symbolic
    Execution to the 68000 C Anti-compiler, Chinese Journal of
    Computers, 11(10):633-637, 1988.

[]{#RefWar89}

 War89
:   M. Ward, \"Proving Program Refinements and Transformations\", Oxford
    University, PhD Thesis, 1989.

[]{#RefGuth90}

 Guth90
:   S. Guthery. exe2c. News item in comp.compilers USENET newsgroup, 30
    Apr 1990.

[]{#RefGuth91a}

 Guth91a
:   S. Guthery. exe2c. News item in comp.compilers USENET newsgroup, 23
    Apr 1991.

[]{#RefReut91}

 Reut91
:   J. Reuter. Private communication. Email, 1991.

[]{#RefAust91}

 Aust91
:   Austin Code Works. exe2c. Beta release, 1991. Email: <info@acw.com>.

[]{#RefBowe91a}

 Bowe91a
:   J.P. Bowen, P.T. Breuer, and K.C. Lano. The REDO project: Final
    report. Technical Report PRG-TR-23-91, Oxford University Computing
    Laboratory, 11 Keble Road, Oxford OX1 3QD, December 1991.

[]{#RefBowe91b}

 Bowe91b
:   J. Bowen and P. Breuer. Decompilation techniques. Internal to ESPRIT
    REDO project no. 2487 2487-TN-PRG-1065 Version 1.2, Oxford
    University Computing Laboratory, 11 Keble Road, Oxford OX1 3QD,
    March 1991.

[]{#RefBowe91c}

 Bowe91c
:   J. Bowen. From programs to object code using logic and logic
    programming. In R. Giegerich and S.L. Graham, editors, Code
    Generation - Concepts, Tools, Techniques, Workshops in Computing,
    pages 173-192, Dagstuhl, German

[]{#RefHood91}

 Hood91
:   S.T. Hood. Decompiling with definite clause grammars. Technical
    Report ERL-0571-RR, Electronics Research Laboratory, DSTO Australia,
    PO Box 1600, Salisbury, South Australia 5108, September 1991.

[]{#RefHung91}

 Hung91
:   L. Hungmong, L. Zongtian, and Z. Yifen. Design and implementation of
    the intermediate language in a PC decompiler system. Mini-Micro
    Systems, 12(2):23-28,46, 1991.

[]{#RefFuan91}

 Fuan91
:   C. Fuan and L. Zongtian. C function recognition technique and its
    implementation in 8086 C decompiling system. Mini-Micro Systems,
    12(11):33-40,47, 1991.

[]{#RefGuth91b}

 Guth91b
:   S. Guthery. Private communication. Austin Code Works, 11100 Leafwood
    Lane, Austin, TX 78750-3587, 14 Dec 1991.

[]{#RefOGor91}

 OGor91
:   J. O\'Gorman. Systematic Decompilation. PhD Thesis. Technical Report
    UL-CSIS-91-12, University of Limerick, 1991. [URL](URL){.twikiLink}:
    <ftp://www.csis.ul.ie/techrpts/ul-91-12.ps>

[]{#RefBrue92}

 Breu92
:   P.T. Breuer and J.P. Bowen. Decompilation: The enumeration of types
    and grammars. Technical Report PRG-TR-11-92, Oxford University
    Computing Laboratory, 11 Keble Road, Oxford OX1 3QD, 1992.

[]{#RefBowe93}

 Bowe93
:   J. Bowen. From programs to object code and back again using logic
    programming: Compilation and decompilation. Journal of Software
    Maintenance: Research and Practice. 5(4):205-234, 1993.

[]{#RefBreu93}

 Breu93
:   P.T. Breuer and J.P. Bowen. Decompilation: the enumeration of types
    and grammars. Transaction of Programming Languages and
    Systems, 1993.

[]{#RefBowe93b}

 Bowe93b
:   J. Bowen, P. Breuer, and K. Lano. A compendium of formal techniques
    for software maintenance. Software Engineering Journal, pages
    253-262, September 1993.

[]{#RefPave93}

 Pave93
:   D.J. Pavey and L.A. Winsborrow. Demonstrating equivalence of source
    code and PROM contents. The Computer Language, 36(7):654-667, 1993.

[]{#RefFuan93}

 Fuan93
:   C. Fuan, L. Zongtian, and L. Li. Design and implementation
    techniques of the 8086 C decompiling system. Mini-Micro Systems,
    14(4):10-18,31, 1993. Chinese language.

[]{#RefBreu94}

 Breu94
:   P.T. Breuer and J.P. Bowen. Generating decompilers. Information and
    Software Technology Journal, 1994.

[]{#RefSite93}

 Site93
:   R.L. Sites, A. Chernoff, M.B. Kirk, M.P. Marks, and S.G. Robinson.
    Binary translation. Communications of the [ACM](ACM){.twikiLink},
    36(2):69-81, February 1993.

[]{#RefCifu94}

 Cifu94
:   C. Cifuentes. Reverse Compilation Techniques. PhD Dissertation.
    Queensland University of Technology, Department of Computing
    Science, 1994.

[]{#RefDRM95}

 DRM95
:   DECLER User Guide and Reference Manual. Microcomputer Institute,
    Hefei University of Technology, 1995.3.

[]{#RefZong96}

 Zong96
:   Liu Zongtian. DECLER: the C Lanuage Decompilation System.
    Microelectronics and Computer, 17(5):1-3.

[]{#RefMycr99}

 Mycr99
:   A. Mycroft. Type-Based Decompilation. Proceedings of ESOP\'99,
    [LNCS](LNCS){.twikiLink} 1576, Springer-Verlag, 1999.

[]{#RefWar99}

 War99
:   M. P. Ward. Assembler to C Migration using the
    [FermaT](FermaT){.twikiLink} Transformation System. Proceedings of
    ACSM\'99, pp67-76.

[]{#RefCVEU99}

 CVEU+99
:   C. Cifuentes, M. Van Emmerik, D. Ung, D. Simon, and T. Waddington.
    Preliminary experiences with the use of the UQBT binary translation
    framework. In *Proc. Workshop on Binary Translation*, Newport Beach,
    pages 12-22. Technical Committee on Technical Architecture
    Newsletter, [IEEE](IEEE){.twikiLink} CS-Press, Dec 1999.

[]{#RefCL00}

 CL00
:   Kaiming Chen, Zongtian Liu, Recognition and Recovery of Switch
    Structure in Decompilation System, Mini-Micro Systems,
    21(12):1279-1281, 2001. Chinese language.

[]{#RefCVE00}

 CVE00
:   C. Cifuentes and M. Van Emmerik. UQBT: Adaptable Binary Translation
    at low cost. *Computer* 33(3) pages 60-66, March 2000.

[]{#RefSML03}

 SML03
:   M. P. Ward. Pigs from Sausages? Reengineering from Assembler to C
    via [FermaT](FermaT){.twikiLink} Transformation. White paper,
    <http://www.smltd.com/migration-t.pdf>, April 2003. Published in
    *Science of Computer Programming Special Issue: Transformations
    Everywhere* 52(1-3):213-255, 2004.

------------------------------------------------------------------------

Portions Copyright 1998 Cristina Cifuentes, All Rights Reserved.\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
