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
    Page](http://www.program-transformation.org/edit/Transform/HistoryOfDecompilation1?t=1536826289)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/HistoryOfDecompilation1)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/HistoryOfDecompilation1)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation1?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation1?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    19](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation1?rev=1.19)
    [(diff 18)](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation1?rev1=1.19&rev2=1.18)
-   [Rev
    18](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation1?rev=1.18)
    [(diff 17)](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation1?rev1=1.18&rev2=1.17)
-   [Rev
    17](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation1?rev=1.17)
    [(diff 16)](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation1?rev1=1.17&rev2=1.16)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation1)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/HistoryOfDecompilation1?template=oopsmore&param1=1.19&param2=1.19)
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
    \...](http://www.program-transformation.org/oops/Transform/HistoryOfDecompilation1?template=oopsmore&param1=1.19&param2=1.19)
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
History Of Decompilation 1 {#history-of-decompilation-1 .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#History_of_Decompilation_1960_19} History of Decompilation (1960-1979)
--------------------------------------------------------------------------

Decompilers have been written for a variety of applications since the
development of the first compilers. The very first decompiler was
written by Joel Donnelly in 1960 at the Naval Electronic Labs to
decompile machine code to Neliac on a Remington Rand Univac M-460
Countess computer. The project was supervised by Professor Maurice
Halstead, who worked on decompilation during the 1960s and 70s, and
published techniques which form the basis for today\'s decompilers. It
is for this reason that we dedicate this page to the memory of Prof
Maurice Halstead and award him the title of [Father of
Decompilation](FatherOfDecompilation){.twikiLink}.

Throughout the last decades, different uses have been given to
decompilers. In the 1960s, decompilers were used to aid in the program
conversion process from second to third generation computers; in this
way, manpower would not be spent in the time-consuming task of rewriting
programs for the third generation machines. During the 70s and 80s,
decompilers were used for the portability of programs, documentation,
debugging, re-creation of lost source code, and the modification of
existing binaries. In the 90s, decompilers have become a reverse
engineering tool capable of helping the user with such tasks as checking
software for the existence of malicious code, checking that a compiler
generates the right code, translation of binary programs from one
machine to another, and understading of the implementation of a
particular library function.

The following descriptions illustrate the best-known decompilers and/or
research performed into decompiler topics by individual researchers or
companies. Most of these descriptions first appeared in [Cristina
Cifuentes](CristinaCifuentes){.twikiLink}\' [PhD
thesis](HistoryOfDecompilation1#RefCifu94){.twikiAnchorLink} *Reverse
Compilation Techniques*. They are reproduced herein with permission from
the author.

Part 1

  ---------------- -------------------------------------------------------------------------------------------
  1960, 1962       [D-Neliac decompiler](HistoryOfDecompilation1#TopicDNeliac){.twikiAnchorLink}
  1963-7           [The Lockheed Neliac decompiler](HistoryOfDecompilation1#TopicLockheed){.twikiAnchorLink}
  1966             [W.Sassaman](HistoryOfDecompilation1#TopicSassaman){.twikiAnchorLink}
  1967             [Autocoder to Cobol translator](HistoryOfDecompilation1#TopicAutocoder){.twikiAnchorLink}
  1972-6           [The Inverse Compiler](HistoryOfDecompilation1#TopicInverse){.twikiAnchorLink}
  1973             [C.R.Hollander PhD thesis](HistoryOfDecompilation1#TopicHollander){.twikiAnchorLink}
  1973             [B.C.Housel PhD thesis](HistoryOfDecompilation1#TopicHousel){.twikiAnchorLink}
  1974             [The Piler System](HistoryOfDecompilation1#TopicPiler){.twikiAnchorLink}
  1974             [F.L.Friedman PhD thesis](HistoryOfDecompilation1#TopicFriedman){.twikiAnchorLink}
  1974             [Ultrasystems](HistoryOfDecompilation1#TopicUltrasystems){.twikiAnchorLink}
  1974             [V.Schneider and G.Winiger](HistoryOfDecompilation1#TopicSchneider){.twikiAnchorLink}
  1977-9           [L Peter Deutsch](HistoryOfDecompilation1#TopicDeutsch){.twikiAnchorLink}
  1977,1981,1988   [Decompilation of Polish code](HistoryOfDecompilation1#TopicPilish){.twikiAnchorLink}
  1978             [G.L.Hopwood PhD thesis](HistoryOfDecompilation1#TopicHopwood){.twikiAnchorLink}
  1978             [D.A.Workman](HistoryOfDecompilation1#TopicWorkman){.twikiAnchorLink}
  ---------------- -------------------------------------------------------------------------------------------

Part 2

  ----------- ---------------------------------------------------------------------------------------------------------------
  1981        [Zebra](HistoryOfDecompilation2#TopicZebra){.twikiAnchorLink}
  1982        [Decompilation of DML programs](HistoryOfDecompilation2#TopicDML){.twikiAnchorLink}
  1982,1984   [Forth Decompiler](HistoryOfDecompilation2#TopicForth){.twikiAnchorLink}
  1984        [Dataflex Decompilers](HistoryOfDecompilation2#TopicDataflex){.twikiAnchorLink}
  1985        [Software transport system](HistoryOfDecompilation2#TopicSoft){.twikiAnchorLink}
  1988        [J.Reuter\'s Decomp VAX BSD decompiler](HistoryOfDecompilation2#TopicDecomp){.twikiAnchorLink}
  1989        [FermaT](HistoryOfDecompilation2#TopicFermat){.twikiAnchorLink}
  1990        [Austin Code Works\' exe2c DOS decompiler](HistoryOfDecompilation2#TopicAustin){.twikiAnchorLink}
  1991        [PLM-90 decompiler](HistoryOfDecompilation2#TopicPLM){.twikiAnchorLink}
  1991        [O\'Gorman\'s PhD thesis](HistoryOfDecompilation2#TopicOGorman){.twikiAnchorLink}
  1991-94     [Decompiler compiler](HistoryOfDecompilation2#TopicDecompComp){.twikiAnchorLink}
  1991-93     [8086 C Decompiling System](HistoryOfDecompilation2#TopicEightOhEightSix){.twikiAnchorLink}
  1993        [Alpha AXP Migration Tools](HistoryOfDecompilation2#TopicAlpha){.twikiAnchorLink}
  1993        [Source/PROM Comparator](HistoryOfDecompilation2#TopicSourcePROM){.twikiAnchorLink}
  1994        [The dcc decompiler](HistoryOfDecompilation2#TopicDCC){.twikiAnchorLink}
  1995        [DECLER Decompiler](HistoryOfDecompilation2#TopicDECLER){.twikiAnchorLink}
  1997-2001   [University of Queensland Binary Translator](HistoryOfDecompilation2#TopicUQBT){.twikiAnchorLink}
  1999        [A. Mycroft\'s Type Reconstruction for Decompilation](HistoryOfDecompilation2#TopicMycroft){.twikiAnchorLink}
  ----------- ---------------------------------------------------------------------------------------------------------------

Part 3

  ------------ -----------------------------------------------------------------------------------------------------------------------------------------
  2000         [University of London\'s Asm21toc reverse compiler](HistoryOfDecompilation3#TopicAsm21toc){.twikiAnchorLink}
  2001         [Proof-Directed De-compilation of Low-Level Code](HistoryOfDecompilation3#TopicProofDirected){.twikiAnchorLink}
  2001         [Computer Security Analysis through Decompilation and High-Level Debugging](HistoryOfDecompilation3#TopicSecurityHLD){.twikiAnchorLink}
  2001         [Type Propagation in IDA Pro Disassembler](HistoryOfDecompilation3#TopicIDATypeProp){.twikiAnchorLink}
  2001         [DisC, by Satish Kumar](HistoryOfDecompilation3#TopicDisC){.twikiAnchorLink}
  2002         [ndcc decompiler](HistoryOfDecompilation3#TopicNdcc){.twikiAnchorLink}
  circa 2002   [The Anatomizer Decompiler](HistoryOfDecompilation3#TopicAnatomizer){.twikiAnchorLink}
  2002         [Analysis of Virtual Method Invocation for Binary Translation](HistoryOfDecompilation3#TopicAnalysisVT){.twikiAnchorLink}
  2002         [Boomerang](HistoryOfDecompilation3#TopicBoomerang){.twikiAnchorLink}
  2002         [Desquirr](HistoryOfDecompilation3#TopicDesquirr){.twikiAnchorLink}
  2004         [Analyzing Memory Accesses in x86 Executables](HistoryOfDecompilation3#TopicAnalysingMem){.twikiAnchorLink}
  2004         [R. Falke\'s Type Analysis for Decompilers](HistoryOfDecompilation3#TopicFalkeDiploma){.twikiAnchorLink}
  ------------ -----------------------------------------------------------------------------------------------------------------------------------------

[]{#TopicDNeliac}

### []{#D_Neliac_decompiler_1960} D-Neliac decompiler, 1960

As reported by Halstead in \[
[Hals62](HistoryOfDecompilation1#RefHals62){.twikiAnchorLink} \], the
Donnelly-Neliac (D-Neliac) decompiler was produced by J.K.Donnelly and
H.Englander at the Navy Electronics Laboratory (NEL) in 1960. Neliac is
an Algol-type language developed at the NEL in 1955. The D-Neliac
decompiler produced Neliac code from machine code programs; different
versions were written for the Remington Rand Univac M-460 Countess
computer and the Control Data Corporation 1604 computer. See also
[NeliacDecompiler](NeliacDecompiler){.twikiLink}.

*D-Neliac proved useful for converting non-Neliac compiled programs into
Neliac, and for detecting logic errors in the original high-level
program. This decompiler proved the feasibility of writing decompilers.*

[]{#TopicLockheed}

### []{#The_Lockheed_Neliac_Decompiler_1} The Lockheed Neliac Decompiler, 1963-7

The Lockheed decompiler, also known as the IBM 7094 to Univac 1108
Neliac Decompiler helped in the migration of scientific applications
from the IBM 7094 to the newer Univac 1108 at Lockheed Missiles and
Space. Binary card images were translated to Univac 1108 Neliac, as well
as assembly code (if available). Binary code was produced from Fortran
applications. As reported in \[Hals70\].

*Halstead analyzed the implementation effort required to raise the
percentage of correctly decompiled instructions half way to 100%, and
found that it was approximately equal to the effort already spent \[
[Hals70](HistoryOfDecompilation1#RefHals70){.twikiAnchorLink} \].* *This
was because decompilers from that time handled straightforward cases,
but the harder cases were left for the programmer to consider. In order
to handle more cases, more time was required to code these special cases
into the decompiler, and this time was proportionately greater than the
time required to code simple cases.*

[]{#TopicSassaman}

### []{#W_Sassaman_1966} W.Sassaman, 1966

Sassaman developed a decompiler at TRW Inc., to aid in the conversion
process of programs from 2nd to 3rd generation computers. This
decompiler took as input symbolic assembler programs for the IBM 7000
series and produced Fortran programs. Binary code was not chosen as
input language because the information in the symbolic assembler was
more useful. Fortran was a standard language in the 1960s and ran on
both 2nd and 3rd generation computers. Engineering applications which
involved algebraic algorithms were the type of programs decompiled. The
user was required to define rules for the recognition of subroutines.
The decompiler was 90% accurate, and some manual intervention was
required \[
[Sass66](HistoryOfDecompilation1#RefSass66){.twikiAnchorLink} \].

*This decompiler makes use of assembler input programs rather than pure
binary code. Assembler programs contain useful information in the form
of names, macros, data and instructions, which are not available in
binary or executable programs, and therefore eliminate the problem of
separating data from instructions in the parsing phase of a decompiler.*

[]{#TopicAutocoder}

### []{#Autocoder_to_Cobol_Conversion_Ai} Autocoder to Cobol Conversion Aid Program, 1967

Housel reported on a set of commercial decompilers developed by IBM to
translate Autocoder programs, which were business data processing
oriented, to Cobol. The translation was a one-to-one mapping and
therefore manual optimization was required. The size of the final
programs occupied 2.1 times the core storage of the original program \[
[Hous73](HistoryOfDecompilation1#RefHous73){.twikiAnchorLink} \].

*This decompiler is really a translation tool of one language to
another. No attempt is made to analyze the program and reduce the number
of instructions generated. Inefficient code was produced in general.*

[]{#TopicInverse}

### []{#The_Inverse_Compiler_1972_6} The Inverse Compiler, 1972-6

The Inverse compiler, also known as the Sperry\*Univac 494 to 1100
inverse compiler, was developed at Univac to aid in the migration to
newer machines, including business applications (i.e. decompilation to
[COBOL](COBOL){.twikiLink}). This decompiler was based on the Lockheed
Neliac decompiler.

[]{#TopicHollander}

### []{#C_R_Hollander_1973} C.R.Hollander, 1973

Hollander\'s PhD dissertation \[
[Holl73](HistoryOfDecompilation1#RefHoll73){.twikiAnchorLink} \]
describes a decompiler designed around a formal syntax-oriented
metalanguage, and consisting of 5 cooperating sequential processes;
initializer, scanner, parser, constructor, and generator; each
implemented as an interpreter of sets of metarules. The decompiler was a
metasystem that defined its operations by implementing interpreters.

The initializer loads the program and converts it into an internal
representation. The scanner interacts with the initializer when finding
the fields of an instruction, and interacts with the parser when
matching source code templates against instructions. The parser
establishes the correspondence between syntactic phrases in the source
language and their semantic equivalents in the target language. Finally,
the constructor and generator generate code for the final program.

An experimental decompiler was implemented to translate a subset of
IBM\'s System/360 assembler into an Algol-like target language. This
decompiler was written in Algol-W, a compiler developed at Stanford
University, and worked correctly on the 10 programs it was tested
against.

*This work presents a novel approach to decompilation, by means of a
formal syntax-oriented metalanguage, but its main drawback is precisely
this methodology, which is equivalent to a pattern-matching operation of
assembler instructions into high-level instructions. This limits the
amount of assembler instructions that can be decompiled, as instructions
that belong to a pattern need to be in a particular order to be
recognized; intermediate instructions, different control flow patterns,
or optimized code is not allowed. In order for syntax-oriented
decompilers to work, the set of all possible patterns would need to be
enumerated for each high-level instruction of each different compiler.
Another approach would be to write a decompiler for a specific compiler,
and make use of the specifications of that compiler; this approach is
only possible if the compiler writer is willing to reveal the
specifications of his compiler. It appears that Hollander\'s decompiler
worked because the compiler specifications for the Algol-W compiler that
he was using were known, as this compiler was written at the University
where he was doing this research. The set of assembler instructions
generated for a particular Algol-W instruction were known in this case.*

[]{#TopicHousel}

### []{#B_C_Housel_1973} B.C.Housel, 1973

Housel\'s PhD dissertation \[
[Hous73](HistoryOfDecompilation1#RefHous73){.twikiAnchorLink} \]
describes a clear approach to decompilation by borrowing concepts from
compiler, graph, and optimization theory. His decompiler involves 3
major phases: partial assembly, analyzer, and code generation.

The partial assembly phase separates data from instructions, builds a
control flow graph, and generates an intermediate representation of the
program. The analyzer analyzes the program in order to detect program
loops and eliminate unnecessary intermediate instructions. Finally, the
code generator optimizes the translation of arithmetic expressions, and
generates code for the target language.

An experimental decompiler was written for Knuth\'s MIX assembler
(MIXAL), producing PL/1 code for the IBM 370 machines. 6 programs were
tested, 88% of the generated statements were correct, and the remaining
12% required manual intervention \[
[Hous73b](HistoryOfDecompilation1#RefHous73b){.twikiAnchorLink}
[HH74](HistoryOfDecompilation1#RefHH74){.twikiAnchorLink} \].

Housel made a real attempt at a general decompiler design, although his
experimental decompiler was time constrained (completed in about 5
person-months). He describes a series of mappings (transformations) to a
\"Final Abstract Representation\" and back again \[
[HH74](HistoryOfDecompilation1#RefHH74){.twikiAnchorLink} \]. The
experimental decompiler was extended in [Friedman\'s
work](HistoryOfDecompilation1#TopicFriedman){.twikiAnchorLink}.

*This decompiler proved that by using known compiler and graph methods,
a decompiler could be written that produced good high-level code. The
use of an intermediate representation made the analysis completely
machine independent. The main objection to this methodology is the
choice of source language, MIX assembler, not only for the greater
amount of information available in these programs, but for being a
simplified non-real-life assembler language.*

[]{#TopicPiler}

### []{#The_Piler_System_1974} The Piler System, 1974

Barbe\'s Piler system attempts to be a general decompiler that
translates a large class of source\--target language pairs to help in
the automatic translation of computer programs. The Piler system was
composed of three phases: interpretation, analysis, and conversion. In
this way, different interpreters could be written for different source
machine languages, and different converters could be written for
different target high-level languages, making it simple to write
decompilers for different source\--target language pairs. Other uses for
this decompiler included documentation, debugging aid, and evaluation of
the code generated by a compiler.

During interpretation, the source machine program was loaded into
memory, parsed and converted into a 3-address microform representation.
This meant that each machine instruction required one or more microform
instructions. The analyzer determined the logical structure of the
program by means of data flow analysis, and modified the microform
representation to an intermediate representation. A flowchart of the
program after this analysis was made available to users, and they could
even modify the flowchart, if there were any errors, on behalf of the
decompiler. Finally, the converter generated code for the target
high-level language \[
[Barb74](HistoryOfDecompilation1#RefBarb74){.twikiAnchorLink} \].

Although the Piler system attempted to be a general decompiler, only an
interpreter for machine language of the GE/Honeywell 600 computer was
written, and skeletal converters for Univac 1108\'s Fortran and Cobol
were developed. The main effort of this project concentrated on the
analyzer. See also [PilerSystem](PilerSystem){.twikiLink}.

*The Piler system was a first attempt at a general decompiler for a
large class of source and target languages. Its main problem was to
attempt to be general enough with the use of a microform representation,
which was even lower-level than an assembler-type representation.*

[]{#TopicFriedman}

### []{#F_L_Friedman_1974} F.L.Friedman, 1974

Friedman\'s PhD dissertation describes a decompiler used for the
transfer of mini-computer operating systems within the same
architectural class \[
[Frie74](HistoryOfDecompilation1#RefFrie74){.twikiAnchorLink} \]. Four
main phases are described: pre-processor, decompiler, code generator,
and compiler.

The pre-processor converts assembler code into a standard form
(descriptive assembler language). The decompiler takes the standard
assembler form, analyses it, and decompiles it into an internal
representation, from which FRECL code is then generated by the code
generator. Finally, a FRECL compiler compiles this program into machine
code for another machine. FRECL is a high-level language for program
transport and development; it was developed by Friedman, who also wrote
a compiler for it. The decompiler used in this project was an adaptation
of Housel\'s decompiler \[
[Hous73](HistoryOfDecompilation1#RefHous73){.twikiAnchorLink} \].

Two experiments were performed; the first one involved the transport of
a small but self-contained portion of the IBM 1130 Disk Monitor System
to Microdata 1600/21; up to 33% manual intervention was required on the
input assembler programs. Overall, the amount of effort required to
prepare the code for input to the transport system was too great to be
completed in a reasonable amount of time; therefore, a second experiment
was conducted. The second experiment decompiled Microdata 1621 operating
system programs into FRECL and compiled them back again into Microdata
1621 machine code. Some of the resultant programs were re-inserted into
the operating system and tested. On average, only 2% of the input
assembler instructions required manual intervention, but the final
machine program had a 194% increase in the number of machine
instructions. See also \[
[FS73](HistoryOfDecompilation1#RefFS73){.twikiAnchorLink} \].

*This dissertation is a first attempt at decompiling operating system
code, and it illustrates the difficulties faced by the decompiler when
decompiling machine-dependent code. Input programs to this transport
system require a large amount of effort to be presented in the format
required by the system, and the final produced programs appear to be
inefficient; both in the size of the program and the time to execute
many more machine instructions.*

[]{#TopicUltrasystems}

### []{#Ultrasystems_1974} Ultrasystems, 1974

Hopwood reported on a decompilation project at Ultrasystems, Inc., in
which he was a consultant for the design of the system \[
[Hopw78](HistoryOfDecompilation1#RefHopw78){.twikiAnchorLink} \]. This
decompiler was to be used as a documentation tool for the Trident
submarine fire control software system. It took as input Trident
assembler programs, and produced programs in the Trident High-Level
Language (THLL) that was being developed at this company. Four main
stages were distinguished: normalization, analysis, expression
condensation, and code generation.

The input assembler programs were normalized so that data areas were
distinguished with pseudo-instructions. An intermediate representation
was generated, and the data analyzed. Arithmetic and logical expressions
were built during a process of expression condensation, and finally, the
output high-level language program was generated by matching control
structures to those available in THLL.

*This project attempts to document assembler programs by converting them
into high-level language. The fact is, given the time constraints of the
project, the expression condensation phase was not coded, and therefore
the output programs were hard to read, as several instructions were
required for a single expression.*

[]{#TopicSchneider}

### []{#V_Schneider_and_G_Winiger_1974} V.Schneider and G.Winiger, 1974

Schneider and Winiger presented a notation for specifying the
compilation and decompilation of high-level languages. By defining a
context-free grammar for the compilation process (i.e. describe all
possible 2-address object code produced from expressions and
assignments), the paper shows how this grammar can be inverted to
decompile the object code into the original source program \[
[Schn74](HistoryOfDecompilation1#RefSchn74){.twikiAnchorLink} \]. Even
more, an ambiguous compilation grammar will produce optimal object code,
and will generate an unambiguous decompilation grammar. A case study
showed that the object code produced by the Algol 60 constructs could
not be decompiled deterministically. This work was part of a future
decompiler, but further references in the literature about this work
were not found.

*This work presents, in a different way, a syntax-oriented decompiler \[
[Holl73](HistoryOfDecompilation1#REefHoll73){.twikiAnchorLink} \]; that
is, a decompiler that uses pattern matching of a series of object
instructions to reconstruct the original source program. In this case,
the compilation grammar needs to be known in order to invert the grammar
and generate a decompilation grammar. Note that no optimization is
possible if it is not defined as part of the compilation grammar.*

[]{#TopicDeutsch}

### []{#L_Peter_Deutsch_1977_1979} L Peter Deutsch 1977-1979

L. Peter Deutsch, using technology derived from his Ph.D thesis (\"An
Interactive Program Verifier\", U.C. Berkeley, 1973), built a very
small-scale instruction-set-retargetable decompiler (RMICRO) in Lisp at
Xerox PARC. It was able to decompile binary code in 4 instruction sets
(two microcodes, one minicomputer, and one bytecoded) into a C-like
language, using Baker\'s algorithm (Journal of the
[ACM](ACM){.twikiLink}, January 1977) to convert flowgraphs into
if/while constructs. It never worked very well, and was not eveloped
further. Peter is known for work on Lisp systems in the \'70s, and later
work on Ghostscript and just-in-time compilation for Smalltalk.

[]{#TopicPolish}

### []{#Decompilation_of_Polish_code_197} Decompilation of Polish code, 1977, 1981, 1988

Two papers in the area of decompilation of Polish code into Basic code
are found in the literature. The problem arises in connection with
highly interactive systems, where a fast response is required to every
input from the user. The user\'s program is kept in an intermediate
form, and then \`\`decompiled\'\' each time a command is issued. An
algorithm for the translation of reverse Polish notation to expressions
is given in \[
[Balb79](HistoryOfDecompilation1#RefBalb79){.twikiAnchorLink} \].

The second paper presents the process of decompilation as a two step
problem: the need to convert machine code to Polish representation, and
the conversion of Polish code to source form. The paper concentrates on
the second step of the decompilation problem, but yet claims to be
decompiling Polish code to Basic code by means of a context-free grammar
for Polish notation and a left-to-right or right-to-left parsing scheme
\[ [Bert81](HistoryOfDecompilation1#RefBert81){.twikiAnchorLink} \].

This technique was recently used in a decompiler that converted reverse
Polish code into spreadsheet expressions \[
[May88](HistoryOfDecompilation1#RefMay88){.twikiAnchorLink} \]. In this
case, the programmers of a product that included a spreadsheet-like
component wanted to speed up the product by storing user\'s expressions
in a compiled form, reverse Polish notation in this case, and decompile
these expressions whenever the user wanted to see or modify them.
Parentheses were left as part of the reverse Polish notation to
reconstruct the exact same expression the user had input to the system.

*The use of the word decompilation in this sense is a misuse of the
term. All that is being presented in these papers is a method for
re-constructing or deparsing the original expression (written in Basic
or Spreadsheet expressions) given an intermediate Polish representation
of a program. In the case of the Polish to Basic translators, no
explanation is given as to how to arrive at such an intermediate
representation given a machine program.*

[]{#TopicHopwood}

### []{#G_L_Hopwood_1978} G.L.Hopwood, 1978

Hopwood\'s PhD dissertation \[
[Hopw78](HistoryOfDecompilation1#RefHopw78){.twikiAnchorLink} \]
describes a 7-step decompiler designed for the purposes of
transferability and documentation. It is stated that the decompilation
process can be aided by manual intervention or other external
information.

The input program to the decompiler is formatted by a preprocessor, then
loaded into memory, and a control flow graph of the program is built.
The nodes of this graph represent one instruction. After constructing
the graph, control patterns are recognized, and instructions that
generate a goto statement are eliminated by the use of either node
splitting or the introduction of synthetic variables. The source program
is then translated into an intermediate machine independent code, and
analysis of variable usage is performed on this representation in order
to find expressions and eliminate unnecessary variables by a method of
forward substitution. Finally, code is generated for each intermediate
instruction, functions are implemented to represent operations not
supported by the target language, and comments are provided. Manual
intervention was required to prepare the input data, provide additional
information that the decompiler needed during the translation process,
and to make modifications to the target program.

An experimental decompiler was written for the Varian Data machines
620/i. It decompiled assembler into MOL620, a machine-oriented language
developed at University of California at Irvine by M.D.Hopwood and the
author. The decompiler was tested with a large debugger program,
Isadora, which was written in assembler. The generated decompiled
program was manually modified to recompile it into machine code, as
there were calls to interrupt service routines, self-modifying code, and
extra registers used for subroutine calls. The final program was better
documented than the original assembler program.

*The main drawbacks of this research are the granularity of the control
flow graph and the use of registers in the final target program. In the
former case, Hopwood chose to build control flow graphs that had one
node per instruction; this means that the size of the control flow graph
is quite large for large programs, and there is no benefit gained as
opposed to using nodes that are basic blocks (i.e. the size of the nodes
is dependent on the number of changes of flow of control). In the latter
case, the MOL620 language allows for the use of machine registers, and
sample code illustrated in Hopwood\'s dissertation shows that registers
were used as part of expressions and arguments to subroutine calls. The
concept of registers is not a high-level concept available in high-level
languages, and it should not be used if wanting to generate high-level
code.*

[]{#TopicWorkman}

### []{#D_A_Workman_1978} D.A.Workman, 1978

This work describes the use of decompilation in the design of a
high-level language suitable for real time training device systems, in
particular the F4 trainer aircraft \[
[Work78](HistoryOfDecompilation1#RefWork78){.twikiAnchorLink} \]. The
operating system of the F4 was written in assembler, and it was
therefore the input language to this decompiler. The output language was
not determined as this project was to design one, thus code generation
was not implemented.

Two phases of the decompiler were implemented: the first phase, which
mapped the assembler to an intermediate language and gathered statistics
about the source program, and the second phase, which generated a
control flow graph of basic blocks, classified the instructions
according to their probable type, and analyzed the flow of control in
order to determine high-level control structures. The results indicated
the need of a high-level language that handled bit strings, supported
looping and conditional control structures, and did not require dynamic
data structures or recursion.

*This work presents a novel use of decompilation techniques, although
the input language was not machine code but assembler. A simple data
analysis was done by classifying instructions, but did not attempt to
analyze them completely as there was no need to generate high-level
code. The analysis of the control flow is complete and considers 8
different categories of loops and 2-way conditional statements.*

[History Of Decompilation 2](HistoryOfDecompilation2){.twikiLink}
(1980-1999)\
[History Of Decompilation 3](HistoryOfDecompilation3){.twikiLink}
(2000-present)

------------------------------------------------------------------------

#### []{#References} References

[]{#RefHals62}

 Hals62
:   M.H. Halstead. Machine-independent computer programming, Chapter 11,
    pages 143-150. Spartan Books, 1962.

[]{#RefHals67}

 Hals67
:   M.H. Halstead. Machine independence and third generation computers.
    In Proceedings SJCC (Sprint Joint Computer Conference), pages
    587-592, 1967.

[]{#RefHals70}

 Hals70
:   M.H. Halstead. Using the computer for program conversion.
    Datamation, pages 125-129, May 1970.

[]{#RefSass66}

 Sass66
:   W.A. Sassaman. A computer program to translate machine language into
    Fortran. In Proceedings SJCC, pages 235-239, 1966.

[]{#RefHous73}

 Hous73
:   B.C. Housel. A Study of Decompiling Machine Languages into
    High-Level Machine Independent Languages. PhD dissertation, Purdue
    University, Computer Science, August 1973.

[]{#RefHous73b}

 Hous73b
:   B.C. Housel and M.H. Halstead. A methodology for machine language
    decompilation. Technical Report RJ 1316 (\#20557), Purdue
    University, Department of Computer Science, December 1973. Also
    published as \[
    [HH74](HistoryOfDecompilation1#RefHH74){.twikiAnchorLink} \].

[]{#RefHoll73}

 Holl73
:   C.R. Hollander. Decompilation of Object Programs. PhD dissertation,
    Stanford University, Computer Science, January 1973.

[]{#RefFS73}

 FS73
:   F.L. Friedman and V.B.Schneider. A Systems Implementation Language.
    [ACM](ACM){.twikiLink} [SIGPLAN](SIGPLAN){.twikiLink} Notices 8(9),
    pages 60-63, September 1973.

[]{#RefHH74}

 HH74
:   B.C. Housel and M.H. Halstead. A methodology for machine language
    decompilation. In Proceedings of the 27th [ACM](ACM){.twikiLink}
    Annual Conference, [ACM](ACM){.twikiLink} Press, pages
    254-260, 1974.

[]{#RefBarb74}

 Barb74
:   P. Barbe. The Piler system of computer program translation.
    Technical report PLR-020, Probe Consultants Inc., September 1974.
    Prepared for the Office of Naval Research, distributed by National
    Technical Information Service, USA. ADA000294. Contract
    N00014-67-C-0472.

[]{#RefFrie74}

 Frie74
:   F.L. Friedman. Decompilation and the Transfer of Mini-Computer
    Operating Systems. PhD dissertation, Purdue University, Computer
    Science, August 1974.

[]{#RefSchn74}

 Schn74
:   V. Schneider and G. Winiger. Translation grammars for compilation
    and decompilation. BIT, 14:78-86, 1974.

[]{#RefBake77}

 Bake77
:   B.S. Baker. An algorithm for structuring flowgraphs. Journal of the
    [ACM](ACM){.twikiLink}, 24(1):98-120, January 1977.

[]{#RefHopw78}

 Hopw78
:   G.L. Hopwood. Decompilation. PhD dissertation, University of
    California, Irvine, Computer Science, 1978.

[]{#RefWork78}

 Work78
:   D.A. Workman. Language design using decompilation. Technical report,
    University of Central Florida, December 1978.

[]{#RefBalb79}

 Balb79
:   D. Balbinot and L. Petrone. Decompilation of Polish code in Basic.
    Rivista di Informatica, 9(4):329-335, October 1979.

[]{#RefBert81}

 Bert81
:   M.N. Bert and L. Petrone. Decompiling context-free languages from
    their Polish-like representations. pages 35-57, 1981.

[]{#RefMay88}

 May88
:   W. May. A simple decompiler. Dr.Dobb\'s Journal, pages 50-52,
    June 1988.

[]{#RefCifu94}

 Cifu94
:   C. Cifuentes. Reverse Compilation Techniques. PhD Dissertation.
    Queensland University of Technology, Department of Computing
    Science, 1994. Also as [compressed
    postscript](http://www.program-transformation.org/twiki/bin/viewfile/Transform/CristinaCifuentes?rev=/sw/bin/rlog%20%20-h%20/users/www/staff/research/projects/stratego/twiki/pub/Transform/CristinaCifuentes/decompilation_thesis.ps.gz,v&filename=decompilation_thesis.ps.gz).

------------------------------------------------------------------------

Portions Copyright 1998 Cristina Cifuentes, All Rights Reserved.\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.HistoryOfDecompilation1 moved from
Transform.HistoryOfDecompilation on 21 Nov 2001 - 12:53 by
[MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/HistoryOfDecompilation1?newweb=Transform&newtopic=HistoryOfDecompilation&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
