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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationProcess?t=1536826290)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationProcess)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationProcess)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationProcess?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationProcess?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilationProcess?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilationProcess?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompilationProcess?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationProcess)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationProcess?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationProcess?template=oopsmore&param1=1.2&param2=1.2)
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
Decompilation Process {#decompilation-process .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#The_Decompilation_Process} The Decompilation Process
========================================================

The main problems with decompilation are the separation of data and code
(i.e. obtaining a complete disassembly of the program), the
reconstruction of control structures, and the recovery of high-level
data types. In order to achieve a greater percentage of the disassembly
automatically, decompilers can make use of knowledge about certain
compilers and libraries used in the compilation of the file to be
decompiled. Identification of library code has been made possible
through signatures, and examples of their usage are dcc\'s dccSign (see
[postscript paper](http://www.csee.uq.edu.au/~cristina/tr-2-94-qut.ps))
and IDA\'s [FLIRT](http://www.datarescue.com/idabase/flirt.htm) library
support.

The following are the main steps in converting executable programs into
a procedural-based high-level language (HLL):

-   Decode the binary-file format.
-   Decode the machine instructions into assembly code for that machine.
    Extra smarts are needed to handle indirect transfers of control such
    as indirect calls and indexed jumps. If the targets of these are not
    all known, the decompilation will be incomplete for that procedure.
    Alternatively, human intervention may be required.
-   Perform semantic analysis to recover some low-level data types such
    as long variables, and to simplify the decoded instructions based on
    their semantics.
-   Store the information in a suitable intermediate representation If a
    suitable intermediate language is used, the next 2 steps can be used
    with any assembly language to generate any procedural HLL code.
-   Perform data flow analysis to remove low-level aspects of the
    intermediate representation that do not exist in HLLs, e.g.
    registers, condition codes, stack references.
-   Perform control flow analysis to recover the control structures
    available in each procedure (i.e. loops, conditionals and their
    nesting level)
-   Perform type analysis to recover HLL data types such as arrays and
    structures. Recovery of classes requires extra analysis. Note: this
    is one of the hardest steps and may need human intervention.
-   Generate HLL code from the transformed intermediate code.

------------------------------------------------------------------------

At a high level, decompilation is a transformation from one program
representation form, which happens to be binary (or assembly language),
to a high level language source code. Loking at the individual
components of a decompiler, perhaps roughly half of these may be viewed
as transformations from one IR to another, or rewritings (same IR).
Specifically:

1.  Decoder/disassembler: machine code instructions to assembly
    language. Note that a stand alone disassembler like objdump can\'t
    really replace this transformation step if (as there should be) here
    is feedback from other parts of the decompiler. However, something
    like the opcodes library which can disassemble one instruction could
    do it.
2.  Semantic transformer. Equivalent to the current SSL parser in
    [Boomerang](DecompilationBoomerang){.twikiLink}. Assembly language
    in, RTL (or some other IR) out.
3.  Possibly the CFG generator. Lists of statements in, CF graph out.
    You could have rules about how branches split up basic blocks, tail
    call restoration, etc. Possibly removing delayed branches could be a
    machine dependent transformation of this kind.
4.  Expression simplifying (and canonicalisation). Used at various
    points.
5.  Possibly switch and virtual function table and/or indirect function
    pointer analysis, or at least application of the results.
6.  Structurer. RTL with CFG in, perhaps machine independent AST out.
    Handle short circuit switches, loops, for/while, etc.
7.  Back end: machine independent AST in, HLL out. May be split into two
    transformations, with a machine dependent AST as the IR between
    these two.
8.  Possibly applying the results of type analysis. For example,
    inserting casts, moving an element of a union to a surrounding
    struct.
9.  VERY speculative: Type Analysis itself? Especially where you meet
    this type with that, result is that type\... Needs more thought.
10. Finding main or a suitable starting point (or points; there could be
    several or many) to start recursive decoding from.
11. Function separator. For example, programs compiled by the MLton
    compiler do not have normal calls and returns, instead moves to and
    from offsets from the stack pointer, and branches. CFG is rewritten,
    list of functions created.

No doubt there are several more. \--
[MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 21 Feb 2005

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
