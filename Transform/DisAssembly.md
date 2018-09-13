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
    Page](http://www.program-transformation.org/edit/Transform/DisAssembly?t=1536826295)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DisAssembly)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DisAssembly)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DisAssembly?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DisAssembly?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Transform/DisAssembly?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Transform/DisAssembly?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Transform/DisAssembly?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/DisAssembly?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/DisAssembly?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/DisAssembly?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DisAssembly)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DisAssembly?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Transform/DisAssembly?template=oopsmore&param1=1.8&param2=1.8)
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
Dis Assembly {#dis-assembly .twikiTopicTitle}
============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Disassembly} Disassembly
----------------------------

Disassembly is the process of translating an executable program into its
equivalent assembly representation. The greatest problem with
disassembling is determining what is code (instructions) and what is
data, as both are represented in the same way in current machines.
Further, disassembly is equivalent to the Halting Problem and hence
cannot be fully automated for all input programs.

This page contains information about various commercial, shareware and
freeware disassemblers, and tools for building disassemblers.

Because of the relative immaturity of machine code
[decompilation](DeCompilation){.twikiLink}, it is presently the case
that for large, commercial reverse engineering projects, a good
disassembler is probably a better option than a decompiler.

-   IDA Pro. Generally agreed as the most powerful disassembler. See
    [IDAPro](IDAPro){.twikiLink}.

<!-- -->

-   Sourcer by [V Communications](http://www.v-com.com). Also a very
    powerful disassembler. See
    [SourcerDisassembler](SourcerDisassembler){.twikiLink}.

<!-- -->

-   BDASM by Manuel Jiménez. A relatively new disassembler. See
    [BdasmDisassembler](BdasmDisassembler){.twikiLink}.

<!-- -->

-   Borg is a freeware disassembler for Windows 32-bit binaries. See
    [BorgDisassembler](BorgDisassembler){.twikiLink}.

<!-- -->

-   [Object file converter](http://www.agner.org/optimize/#objconv) is
    an open source tool which can disassemble COFF, PE, ELF, OMF and
    Mach-O files for x86 and x86-64 systems. Supports SSE4 instruction
    set. Reports syntax errors and suboptimal instruction codes. Source
    code is portable to all systems. It can also be used for converting
    object files between different formats and as a cross-platform
    library manager.

<!-- -->

-   DSM Studio was earlier known as the Phoenix disassembler. See
    [DsmStudioDisassembler](DsmStudioDisassembler){.twikiLink}.

<!-- -->

-   ProView (formerly PVDasm). See
    [ProViewDisassembler](ProViewDisassembler){.twikiLink}.

<!-- -->

-   [MacNosy](http://www.jasik.com/nosy.html) is a disassembler for Mac
    (68K and PowerPC) applications, resource files or ROM.

<!-- -->

-   [Lida (Linux Interactive
    DisAssembler)](http://lida.reverse-engineering.net/) is a 6 pass
    disassembler with some cryptanalysis and resistance against corrupt
    ELF sections and the like. Features include cross references, string
    references, add/rename labels and pointers, search, syntax
    highlighting, high speed.

<!-- -->

-   [XDASM](http://www.datasynceng.com/xdasmdoc.htm): Universal Cross
    Disassembler. This is a commercial disassembler for a large number
    of 8/16 bit processors (except anything higher than 386). This
    disassembler uses processor description to do its work, which means
    you can add your own processor descriptions. Was US\$249, now US\$99
    if you print your own manual.

<!-- -->

-   [Win32 Program Disassembler](Win32ProgramDisassembler){.twikiLink}

<!-- -->

-   [PE Explorer Disassembler](http://www.heaventools.com/) achieves
    most of the power of IDA Pro, while requiring less skill or
    knowledge, by automating more of the disassembly process. The PE
    Explorer disassembler assumes that some manual editing of the
    reproduced code will be needed. A 30 day free trial is available.
    See [PEExplorer](PEExplorer){.twikiLink}.

<!-- -->

-   [MFVDasm](http://redirect.to/MFVDasm) is commercial software
    (US\$100 as of December 2001) for Windows. It disassembles many PC
    format files, and uses a web-browser like GUI interface. A 7 day
    free trial is available.

<!-- -->

-   [disasm32 Visual Symbolic
    Disassembler](Disasm32VisualSymbolicDisassembler){.twikiLink}

<!-- -->

-   [VXDasm](http://www.chez.com/jls/vxdasm.html) is a visual
    relocatable disassembler for Windows device drivers. A demo version
    is downloadable from the VXDasm home page.

<!-- -->

-   [Bastard](http://bastard.sourceforge.net/) is an open source
    disassembler hosted on [Sourceforge](http://www.sourceforge.net).
    From the web page: \"The bastard currently runs on x86 Linux and
    FreeBSD \[CVS version\]. It can disassemble x86 ELF, a.out, and PE
    files as well as flat binary files \[.com, .bin\]. Future releases
    will support additional file formats and CPU architectures.\" The
    [libdisasm](http://bastard.sourceforge.net/libdisasm.html) library
    is available separately (X86 only).

<!-- -->

-   [TC source for 486 code stream
    disassembler](http://www.simtel.net/pub/simtelnet/msdos/disasm/486dis_c.zip):
    These Turbo C sources are written by Robin Hilliard and are under
    the [GNU](GNU){.twikiLink} license. As far as we know, no automatic
    detection system for code and data is included. (Dated: 4-20-93.)

<!-- -->

-   [obj2asm](http://www.simtel.net/pub/simtelnet/msdos/disasm/obj2asm.zip)
    TC Source for intelligent .OBJ disassembler. This is not a
    disassembler of EXE or COM files, but of OBJ files, which are
    sometimes distributed in LIB files, without the original code.
    Because of the nature of the OBJ files, a far more accurate
    disassembling can be done, with even some of the original names of
    procedures and (global) variables. Sources are provided under the
    [GNU](GNU){.twikiLink} license. This is also from Robin Hilliard.
    (Dated: 4-20-93.)

<!-- -->

-   Duncan Murdoch maintains a
    [page](http://www8.pair.com/dmurdoch/programs/index.htm) with
    programs for dumping the various Turbo Pascal Unit (TPU) files, as
    well as various other disassembly related programs.

<!-- -->

-   AMSGEN is a disassembler written by J. Gersbach and J. Damke.
    (Appears to be freeware.) It is automatic detection of code and
    data, but extra information can be provided in a .SEQ file. ASMGSQ
    is a .SEQ file generator. The program has been throughly tested on
    correctness. A test procedure is included in the distribution.
    (Dated: 11-23-90.) Download from
    [SimTel](http://www.simtel.net/pub/simtelnet/msdos/disasm).

<!-- -->

-   Bubble is a disassembler program with automatic detection of code
    and data fragments, but can also be used interactively. (Dated:
    3-12-92.) Download from
    [SimTel](http://www.simtel.net/pub/pd/44039.html). (Address updated
    07 Jun 2004 by Trash.BG1)

<!-- -->

-   DIS86 is more like a step-by-step debugger, with built in
    disassembler. You can walk through the code, call subroutines, and
    return. It keeps some track of the contents of the registers, but
    not much. You can add your own labels. Does not have an automatic
    detection of code and data. Written by James R. van Zandt. (Dated:
    1-1-79.) Download from
    [SimTel](http://www.simtel.net/pub/simtelnet/msdos/disasm).

<!-- -->

-   nm - print symbol name list (Unix command). nm prints the name list
    (symbol table) of each object filename in the argument list. If an
    argument is an archive, a listing for each object file in the
    archive will be produced. If no filename is given, the symbols in
    a.out are listed.

<!-- -->

-   [RosAsm](http://betov.free.fr/RosAsm.html) is primarily an
    assembler, but it claims to have a \"two click disassembly\"
    feature. I haven\'t tried it, but it sounds interesting. The claim
    is that most small and some medium sized programs can be modified.

<!-- -->

-   [Dispe](http://kmkz.jp/mtm/?load=dispe) is a Japanese disassembler
    for Windows PE programs. It attempts to structure the output
    slightly, giving it a slight decompiler flavour. I find that
    [Babelfish](http://babelfish.altavista.com) translates the page
    better than
    [Google](http://translate.google.com/translate?u=http%3A%2F%2Fkmkz.jp%2Fmtm%2F%3Fload%3Ddispe&langpair=ja%7Cen&hl=en&ie=UTF-8&oe=UTF-8&prev=%2Flanguage_tools).
    There appears to be a freely downloadable Windows binary on the web
    page.

<!-- -->

-   See also
    -   [The New Jersey Machine Code Toolkit](NjmcTk){.twikiLink}
    -   [Hacker Disassembling
        Uncovered](HackerDisassemblingUncovered){.twikiLink}: a book by
        Kris Kaspersky.
    -   See also [the Data Rescue
        Bookstore](http://www.datarescue.com/bookstore/index.htm) for
        more book suggestions.
    -   <http://www.shareware.com> archive search on
        [disassembler](http://shareware.search.com/search?cat=247l&q=disassembler)
        or
        [disassemble](http://shareware.search.com/search?cat=247l&q=disassemble).
    -   [dmoz.org](http://dmoz.org)\'s
        [Computers/Programming/Disassemblers](http://dmoz.org/Computers/Programming/Disassemblers)
        directory entry. Similar pages are available from
        [Google](http://directory.google.com/Top/Computers/Programming/Disassemblers),
        [Netscape](http://search-intl.netscape.com/Computers/Programming/Disassemblers),
        [interactiva.org](http://www.interactiva.org/Dir/I/English/Computers/Programming/Disassemblers/),
        and many others.
    -   <http://www.simtel.net> under
        [Programming](http://www.simtel.net/category.sub.php?id=346)
        then [Disassemblers](http://www.simtel.net/category.php?id=73).
    -   [DecompilationResources](DecompilationResources){.twikiLink}.

### []{#Possibly_obsolete_products} Possibly obsolete products

-   WDASM 1.7b: Windows Disassembler Program. This is a shareware
    Windows program for disassembling Windows 3.1 programs, written by
    Eric Grass. It also includes a program called hilevel, which can
    transform the assembler output in a structured assembler format,
    including definition of procedures, local variables, and if-macro
    sections (it is also mentioned in the Free Compilers list.) Was at
    <http://www.leo.org/pub/comp/os/windows/win3.11/programming/asm/index.html>
    .

<!-- -->

-   ASM Trace is the disassembler by Tels of ASM Edit. The author wrote
    it because he was not happy with Sourcer. He has discontinued work
    on ASM Trace a while ago. Was at <http://www.bloodgate.com> .

<!-- -->

-   Unasource. The current release of Unasource is v0.3d which is
    described by its author, Francisco Javier Felix, as a little
    disassembler for .com and .sys pentium binaries. Unasource is a
    straight line disassembler for DOS binaries. The long term goal for
    unasource is to be a full decompiler that generates C, Cobol, Visual
    Basic and other source codes. At present, it is a disassembler. Was
    at <http://www.ctv.es/USERS/fflix/> .

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
