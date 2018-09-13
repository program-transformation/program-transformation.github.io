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
    Page](http://www.program-transformation.org/edit/Transform/HistoryOfDecompilation3?t=1536826290)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/HistoryOfDecompilation3)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/HistoryOfDecompilation3)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation3?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation3?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation3?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation3?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation3?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation3?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/HistoryOfDecompilation3?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation3?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/HistoryOfDecompilation3)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/HistoryOfDecompilation3?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Transform/HistoryOfDecompilation3?template=oopsmore&param1=1.6&param2=1.6)
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
History Of Decompilation 3 {#history-of-decompilation-3 .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#History_of_Decompilation_2000_pr} History of Decompilation (2000-present)
=============================================================================

[]{#TopicAsm21toc}

### []{#University_of_London_s_Asm21toc}[]{#University_of_London_s_Asm21toc_} University of London\'s Asm21toc reverse compiler, 2000.

This assembly language decompiler for Digital Signal Processing (DSP)
code was written in a compiler-compiler called rdp \[
[JSW00](HistoryOfDecompilation3#RefJSW00){.twikiAnchorLink} \]. The
authors note that DSP is one of the last areas where assembly language
is still commonly used. As usual, the decompilation from assembly
language is considerably easier than from executable code; in fact the
authors \"doubt the usefulness\" of decompiling from binary files.

[]{#TopicProofDirected}

### []{#Proof_Directed_De_compilation_of} Proof-Directed De-compilation of Low-Level Code, 2001.

Katsumata and Ohori published a paper \[
[KO01](HistoryOfDecompilation3#RefKO01){.twikiAnchorLink} \] on
decompilation based on proof theoretical methods. The input is Jasmin,
essentially Java assembly language. The output is an ML-like simply
typed functional language. Their example shows an iterative
implementation of the factorial function transformed into two functions
(an equivalent recursive implementation). Their approach is to treat
each instruction as a constructive proof representing its computation.
While not immediately applicable to a general decompiler, their work may
have application where proof of correctness (usually of a compilation)
is required.

In \[ [Myc01](HistoryOfDecompilation3#RefMyc01){.twikiAnchorLink} \],
Mycroft compares his Type-Based decompilation with this work.
Structuring to loops and conditionals is not attempted by either system.
He concludes that the two systems produce very similar results in the
areas where they overlap, but that they have different strengths and
weaknesses.

[]{#TopicSecurityHLD}

### []{#Computer_Security_Analysis_throu} Computer Security Analysis through Decompilation and High-Level Debugging, 2001.

Cifuentes et al suggested dynamic decompilation as a way to provide a
powerful tool for security work. The main idea is that the security
analyst is only interested in one small piece of code at one time, and
so high level code could be generated \"on the fly\". One problem with
traditional (static) decompilation is that it is difficult to determine
the range of possible values of variables; by contrast, a dynamic
decompiler can provide at least one value (the current value) with no
effort \[ [CWVE01](HistoryOfDecompilation3#RefCWVE01){.twikiAnchorLink}
\].

[]{#TopicIDATypeProp}

### []{#Type_Propagation_in_IDA_Pro_Disa} Type Propagation in IDA Pro Disassembler, 2001.

Guilfanov describes the type propagation system in the popular
disassembler IDA Pro [Ida Pro](http://www.datarescue.com/idabase/). The
types of parameters to library calls are captured from system header
files. The parameter types for commonly used libraries are saved in
files called type libraries. Assignments to parameter locations are
annotated with comments with the name and type of the parameter. This
type information is propagated to other parts of the disassembly,
including all known callers. At present, no attempt is made to find the
types for other variables not associated with the parameters of any
library calls \[
[Gui01](HistoryOfDecompilation3#RefGui01){.twikiAnchorLink} \].

[]{#TopicDisC}

### []{#DisC_by_Satish_Kumar_2001}[]{#DisC_by_Satish_Kumar_2001_} [DisC](DisC){.twikiLink}, by Satish Kumar, 2001.

This decompiler is designed to read only programs written in Turbo C
version 2.0 or 2.01; it is an example of a compiler specific decompiler.
There is no significant advantage to this approach, since general
techniques are not much more difficult to implement. It is an
interesting observation that since most aspects of decompilation are
ultimately pattern matching in some sense, the difference between
pattern matching decompilers and general ones is essentially one of the
generality of the patterns.
<http://www.debugmode.com/dcompile/disc.htm>.

[]{#TopicNdcc}

### []{#ndcc_decompiler_2002}[]{#ndcc_decompiler_2002_} ndcc decompiler, 2002.

André Janz modified the dcc decompiler to read 32-bit Windows Portable
Executable (PE) files. The intent was to use the modified decompiler to
analyse malware. The author states that a rewrite would be needed to
fully implement the 80386 instruction set. Even so, reasonable results
were obtained, while retaining dcc\'s severe limitations \[
[Jan02](HistoryOfDecompilation3#RefJan02){.twikiAnchorLink} \].

[]{#TopicAnatomizer}

### []{#The_Anatomizer_Decompiler_circa}[]{#The_Anatomizer_Decompiler_circa_} The Anatomizer Decompiler, circa 2002.

K. Morisada released a decompiler for Windows 32-bit programs, which
appears to be comparable in capability to the REC compiler for that
platform. See also
[AnatomizerDecompiler](AnatomizerDecompiler){.twikiLink} and
<http://jdi.at.infoseek.co.jp>.

[]{#TopicAnalysisVT}

### []{#Analysis_of_Virtual_Method_Invoc} Analysis of Virtual Method Invocation for Binary Translation, 2002.

Tröger and Cifuentes show a method of analysing indirect call
instructions. If such a call implements a virtual method call and is
correctly identified, various important aspects of the call are
extracted. The technique as presented is limited to one basic block; as
a result, it fails for some less common cases. \[
[TC02](HistoryOfDecompilation3#RefTC02){.twikiAnchorLink} \].

[]{#TopicBoomerang}

### []{#Boomerang_2002}[]{#Boomerang_2002_} Boomerang, 2002.

This is an open source decompiler, with several front ends (two are well
developed) and a C back end. It uses an internal representation based on
the Static Single Assignment form, and pioneers dataflow-based type
analysis. At the time of writing, it is still limited to quite small
(toy) binary programs. <http://boomerang.sourceforge.net>.

[]{#TopicDesquirr}

### []{#Desquirr_2002}[]{#Desquirr_2002_} Desquirr, 2002.

This is an IDA Pro Plugin, written by David Eriksson as part of his
Master\'s thesis. It decompiles one function at a time to the IDA output
window. While not intended to be a serious decompiler, it illustrates
what can be done with the help of a powerful disassembler and about 5000
lines of C++ code. Because a disassembler does not carry semantics for
machine instructions, each supported processor requires a module to
decode instruction semantics and addressing modes. The X86 and ARM
processors are supported. Conditionals and loops are emitted as gotos,
there is some simple switch analysis, and some recovery of parameters
and returns is implemented. <http://desquirr.sourceforge.net/desquirr>.

[]{#TopicAnalysingMem}

### []{#Analyzing_Memory_Accesses_in_x86} Analyzing Memory Accesses in x86 Executables, 2004.

Balakrishnan and Reps from the University of Wisconsin have developed a
framework for analysing binary programs that they call Codesurfer/x86.
The aim is to produce intermediate representations that are similar to
those that can be created for a program written in a high-level
language. The binary is first disassembled with the IDA Pro
disassembler. A plug-in for IDA Pro called Connector, provided by
[Grammatech Inc](http://www.grammatech.com), interfaces to the rest of
the tool. Value-set Analysis (VSA) is used to produce an intermediate
representation, which is presented in a source code analysis tool called
[CodeSurfer](http://www.grammatech.com/products/codesurfer/overview.html)
(sold separately by Grammatech Inc for C/C++ source code analysis) \[
[BR04](HistoryOfDecompilation3#RefBR04){.twikiAnchorLink},
[RBLT05](HistoryOfDecompilation3#RefRBLT05){.twikiAnchorLink} \].
Codesurfer/x86 may be [commercially available
soon](http://www.grammatech.com/research/cs-x86/).

[]{#TopicFalkeDiploma}

### []{#R_Falke_s_Type_Analysis_for_Deco} R. Falke\'s Type Analysis for Decompilers, 2004

Raimar Falke, in his Diploma Thesis \[
[Fal04](HistoryOfDecompilation3#RefFal04){.twikiAnchorLink} \] (German)
for the Technical University of Dresden, implemented an adaption of
Mycroft\'s type constraint theory in a decompiler called YaDeC. He
extended it to handle arrays. To keep the project manageable, he used
objdump for the front end, ignored floating point types, assumed only
stack parameters, and so on. An English translation of the paper\'s
summary can be found in
[FalkeDiplomaSummary](FalkeDiplomaSummary){.twikiLink}.

[]{#TopicAndromeda}

### []{#Andromeda_Decompiler_2004_2005}[]{#Andromeda_Decompiler_2004_2005_} Andromeda Decompiler, 2004-2005.

Andrey Shulga wrote a decompiler for Windows x86 and C. The decompiler
itself was never released, however a GUI program for manipulating the IR
generated by the compiler is available at the author\'s web site \[
[Shu04](HistoryOfDecompilation3#RefShu04){.twikiAnchorLink} \]. Only an
x86 front end is written at present, and only a C/C++ back end, although
the decompiler is claimed to be capable of other front and back ends.
The output for the provided demonstration IR is extremely impressive,
but it is not clear whether the IR is largely automatically generated by
the decompiler, or hand edited. The web page has been inactive since May
2005.

[]{#TopicHexRays}

### []{#Hex_Rays_Decompiler_Plugin_2007}[]{#Hex_Rays_Decompiler_Plugin_2007_} Hex Rays Decompiler Plugin, 2007.

Ilfak Guilfanov, author of the IDA Pro disassembler, released a
commercial decompiler plugin for IDA Pro \[
[Gui07a](HistoryOfDecompilation3#RefGui07a){.twikiAnchorLink},
[Gui07b](HistoryOfDecompilation3#RefGui07b){.twikiAnchorLink} \]. This
plugin adds a decompiler view to the other views available in the
interactive disassembler. One function is shown at a time; most
functions decompile in a fraction of a second to a quite C-like output.
The author stresses that output is not designed for re-compilation, only
for more rapid comprehension of what the function is doing. The output
includes compound conditionals (with \|\| and &&), loops (for, while,
break, etc), and function parameters and returns. There is also an
[API](API){.twikiLink} which gives access to the decompiler\'s IR,
allowing custom analyses if desired. At this stage, only the x86
architecture is supported. The decompiler relies on the disassembler
(and possibly manual intervention) to separate code from data and to
identify functions.

[]{#TopicSSAForDecomp}

### []{#Static_Single_Assignment_for_Dec} Static Single Assignment for Decompilation, 2007.

Mike Van Emmerik completed this PhD theses at the University of
Queensland in October 2007 \[
[VE07](HistoryOfDecompilation3#RefVE07){.twikiAnchorLink} \]. The main
theme is how the SSA form enables various aspects of decompilation to be
more readily analysed, although this leads to other topics such as type
analysis and the analysis of indirect jumps and calls. An industry case
study is discussed. Although considerable progress is made, many
problems still remain, particularly related to alias analysis. There is
a chapter of results, using the Boomerang open source decompiler. A new
algorithm for finding preserved locations in procedures in the presence
of recursion is given. There is a comprehensive glossary of terms,
history, comparison with Java decompilers, a survey of compiler
infrastructures that may be suitable for decompilation, and the problems
faced by decompilers are summarised in terms of separation problems
(code from data, pointers from constants, and original from offset
pointers).

[History Of Decompilation 1](HistoryOfDecompilation1){.twikiLink}
(1960-1979)\
[History Of Decompilation 2](HistoryOfDecompilation2){.twikiLink}
(1980-1999)\

------------------------------------------------------------------------

#### []{#References} References

[]{#RefJSW00}

 JSW00
:   A. Johnstone, E. Scott, and T. Womack. Reverse Compilation for
    Digital Signal Processors: a Working Example. In *Proceedings of the
    Hawaii International Conference on System Sciences*.
    [IEEE](IEEE){.twikiLink}-CS Press, January 2000.

[]{#RefKO01}

 KO01
:   S. Katumata and A. Ohori. Proof-directed de-compilation of low-level
    code. In *European Symposium on Programming*, volume 2028 of Lecture
    Notes in Computer Science, pages 352-366. Springer-Verlag 2001.

[]{#RefMyc01}

 Myc01
:   A. Mycroft. Comparing type-based and proof-directed decompilation.
    In *Proceedings of the Working Conference on Reverse Engineering*,
    pages 362-367, Stuttgart Germany. [IEEE](IEEE){.twikiLink}-CS
    Press 2001.

[]{#RefCWVE01}

 CWVE01
:   C. Cifuences, T. Waddington, and M. Van Emmerik. Computer Security
    Analysis through Decompilation and High Level Debugging. In
    *Proceedings of the Working Conference on Reverse Engineering*,
    pages 375-380, Stuttgart Germany. [IEEE](IEEE){.twikiLink}-CS
    Press 2001.

[]{#RefGui01}

 Gui01
:   I. Guilfanov. A simple type system for program reengineering. In
    *Proceedings of the Working Conference on Reverse Engineering*,
    pages 357-361, Stuttgart Germany. [IEEE](IEEE){.twikiLink}-CS
    Press 2001.

[]{#RefJan02}

 Jan02
:   André Janz. Experimente mit einem Decompiler im Hinblick auf die
    forensische Informatik, 2002.
    <http://agn-www.informatik.uni-hamburg.de/papers/doc/diparb_andre_janz.pdf>
    .

[]{#RefTC02}

 TC02
:   J. Tröger and C. Cifuentes. Analysis of virtual method invocation
    for binary translation. In *Proceedings of the Working Conference on
    Reverse Engineering*, Richmond, Virginia; pages 65-74.
    [IEEE](IEEE){.twikiLink}-CS Press, 2002.

[]{#RefBR04}

 BR04
:   G. Balakrishnan and T. Reps. Analyzing Memory Accesses in x86
    Executables. In *Proceedings of Compiler Construction*
    ([LNCS](LNCS){.twikiLink} 2985) pages 5-23. Springer-Verlag
    April 2004.

[]{#RefFal04}

 Fal04
:   R. Falke. Entwicklung eines Typeanalysesystem fü­­r einen Decompiler
    (Development of a type analysis system for a decompiler), 2004.
    Diploma thesis, German language. <http://risimo.net/diplom.ps> . No
    longer available, however archived
    [here](http://web.archive.org/web/*/http://risimo.net/diplom.ps)
    (archive.org, 491kB).

[]{#RefShu04}

 Shu04
:   Andrey Shulga. Andromeda Decompiler web page, 2004.
    <http://shulgaaa.at.tut.by> .

[]{#RefRBLT05}

 RBLT05
:   T. Reps, G. Balakrishnan, J. Lim and T. Teilelbaum. A
    Next-Generation Platform for Analysing Executables. To appear in
    *Proc. 3rd Asian Symposium on Programming Languages and Systems*,
    Springer-Verlag 2005.

[]{#RefGui07a}

 Gui07a
:   I. Guilfanov. Blog: Decompilation Gets Real, April 2007.
    <http://hexblog.com/2007/04/decompilation_gets_real.html> .

[]{#RefGui07b}

 Gui07b
:   I. Guilfanov. Hex-rays home page, 2007. <http://www.hex-rays.com> .

[]{#RefVE07}

 VE07
:   M. Van Emmerik. Static Single Assignment for Decompilation. PhD
    thesis, University of Queensland, 2007.
    <http://vanemmerikfamily.com/mike/master.pdf> or
    <http://vanemmerikfamily.com/mike/master.ps.gz> .

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
