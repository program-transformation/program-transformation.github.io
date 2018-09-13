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
    Page](http://www.program-transformation.org/edit/Transform/WhyDecompilation?t=1536826287)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/WhyDecompilation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/WhyDecompilation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/WhyDecompilation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/WhyDecompilation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    17](http://www.program-transformation.org/view/Transform/WhyDecompilation?rev=1.17)
    [(diff 16)](http://www.program-transformation.org/rdiff/Transform/WhyDecompilation?rev1=1.17&rev2=1.16)
-   [Rev
    16](http://www.program-transformation.org/view/Transform/WhyDecompilation?rev=1.16)
    [(diff 15)](http://www.program-transformation.org/rdiff/Transform/WhyDecompilation?rev1=1.16&rev2=1.15)
-   [Rev
    15](http://www.program-transformation.org/view/Transform/WhyDecompilation?rev=1.15)
    [(diff 14)](http://www.program-transformation.org/rdiff/Transform/WhyDecompilation?rev1=1.15&rev2=1.14)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/WhyDecompilation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/WhyDecompilation?template=oopsmore&param1=1.17&param2=1.17)
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
    \...](http://www.program-transformation.org/oops/Transform/WhyDecompilation?template=oopsmore&param1=1.17&param2=1.17)
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
Why Decompilation {#why-decompilation .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Why_decompilation}[]{#Why_decompilation_} Why decompilation?
================================================================

[]{#Why_not_just_disassemble}[]{#Why_not_just_disassemble_} Why not just disassemble?
-------------------------------------------------------------------------------------

Consider the Java world, where there are simple disassemblers and
sophisticated decompilers that often work well and with little user
intervention. Would you use a Java disassembler to try to understand
some Java bytecode program? Most likely not. If there is a good
decompiler available, you don\'t need to see the individual
instructions. If and when a good decompiler for executable programs
becomes available, it will be a better choice than a disassembler in
most circumstances.

[]{#Applications} Applications
------------------------------

There are many reasons why you might want to decompile a program. Here
are some of them, based on this diagram:

![Decompilation
applications](../pub/Transform/WhyDecompilation/tree120.png)

If the output is considered\...

-   A comprehension aid. You don\'t have the resources to create
    compilable code. Even so, you can do these things:
    -   You can perform code checking of various kinds:
        -   Find bugs. You focus on the area of the program that you are
            interested in. looking for bugs.
        -   Find vulnerabilities. You scan the whole program, looking
            for code that could be exploited.
        -   Find malware. Again you scan the whole program, this time
            looking for code that has already been exploited. It may be
            easier and quicker to find malware in 1000 lines of C than
            in 10,000 lines of assembler.
        -   Verification. You want to make sure that the binary code
            that you have corresponds to the source code that you also
            have. This is important in safety critical applications.
        -   Comparison. Suppose you are accused of violating a software
            patent, or suspect that someone has violated your patent.
            You can show how different or similar two programs are by
            comparing decompiled source code. To some extent, a
            decompiler can make two different implementations of the
            same program reveal their similarities. As an example of
            this, using different optimisations with the same compiler
            somtimes results in similar decompiled code.
    -   Learn Algorithm. To the extent that is allowable by law, you
        might want to discover how a particular feature of a piece of
        software is implemented. It\'s a little bit like browsing
        patents online; you can\'t use what you see directly in a
        commercial setting, unless you have an arrangement with the
        author.
    -   Interoperability. It may be legal and necessary to reverse
        engineer some binary code for the purposes of interoperability.
        There are the famous cases of Sega vs Accolade and Atari v
        Nintendo, where small games companies successfully argued their
        right to reverse engineer some existing games, so that they
        could manufacture competing games for that platform. I don\'t
        know if they used decompilation for this (probably not), but
        it\'s a good example of iwhere decompilation might make a
        difficult job much easier.
-   If you have compilable code, then you can do more:
    -   With little user input:
        -   Optimise for platform. Example: you have an old program
            written for the 80286 processor, but you have a Pentium 4.
            You can recompile the code with optimisations appropriate
            for your actual hardware.
        -   Port cross platform (where the same libraries are
            available). For example, you have an Intel Windows version
            of a program, but you have an Alpha (running Windows NT).
            You can recompile the decompiled output with an Alpha
            compiler. Or recompile it with
            [Winelib](http://www.winehq.com/site/winelib) (to provide
            Windows libraries) and run the \"Windows\" program natively
            on your PPC laptop under Linux. Or compile it under
            [Darwine](http://darwine.opendarwin.org) on your Mac running
            OS/X. If the vendor doesn\'t provide one, a 64-bit driver
            (required for 64-bit Windows XP) might be rewritten from the
            decompilation of a 32-bit driver. Decompiling or
            disassembling an existing driver binary may be the only way
            to find interoperability information, e.g. to write a Linux
            driver.
    -   If you put enough effort into the decompilation to produce
        maintainable code, you can also:
        -   Fix bugs (without the tediom of patching the binary file).
        -   You can also add new features that were not in the original
            program.
        -   You can recover lost or unusable source code. It is
            estimated that 5% of all software in the world has at least
            some source files missing. You can use the decompiled code
            to replace the missing source file(s). You can also maintain
            code that was written in assembler, or in a language for
            which the compilers no longer exist.

Some more decompilation applications that don\'t fit very well into the
above classification:

-   Defeating copy protection, where the company who wrote the software
    (that you paid for) is out of business, and you can\'t transfer it
    to a new machine. It does happen!
-   Support for programs that ship without debugging information, often
    linking with third party code, and one day it just stops working.
    Recompiling with debugging support turned on may or may not show the
    fault. People experience this problem in the field all the time, and
    at present the tools they have to work with are inadequate.
    Decompilation may be able to ease the support burden, even for
    companies that have the source code (except perhaps to some third
    party code).

[]{#Software_Freedoms} Software Freedoms
----------------------------------------

On a [SlashDot](http://www.slashdot.org) articled called [\"BitKeeper
Love Triangle: McVoy, Linus and
Tridge\"](http://linux.slashdot.org/linux/05/04/11/1413232.shtml?tid=99&tid=106)
11/Apr/2005), it was posted:

Copyrights on binaries (Score:4, Insightful)\
by Peaker (72084) on Monday April 11, \@01:51PM (\#12202730)
(<http://slashdot.org/>)

*\"The purpose of copyrights is to advance science and useful arts, not
to reward authors.*

*If rewarding authors for that purpose is required, then they will be
rewarded.*

*Copyrights on binaries however, reward authors while stifling the
progress of science and useful arts.*

*It encourages people to create secretly-operating software that helps
them get revenue but does not inspire new works, does not enter the
public* *domain and does not help anyone else in the long run.*

So what if publishing your binary was almost as useful as publishing
source code? Decompilation is not yet at a stage where this is true, but
in 5-10 years, it may well be. Decompilation could then become a tool
for software freedom.

Here is another quote, this time from [\"Breaking into Locked Rooms to
Access Computer Source Code: Does the DMCA Violate a Constitutional
Mandate When Technological Barriers of Access Are Applied to
Software?\"](http://www.vjolt.net/vol8/issue1/v8i1_a02-Dixon.pdf) by Rod
Dixon of Virginia Journal of Law and Technology:

*\"27. For non-software literary works, once the work is published, the*
*ideas contained in the work become apparent and conspicuous. In this*
*manner, the work\'s basic ideas may provide a basis for further*
*development of additional works by any member of the public with*
*access to the work. This is a critical function of the public domain*
*because it serves the primary purpose of copyright. \... The
enrichment* *of the public domain of ideas increases the public\'s
access to works,* *which further enriches the public domain. Software,
however, presents* *a slight conundrum that disrupts the flow of the
recursive enrichment* *of the public domain served by copyright law.\"*

Again, decompilation may (if the laws are written correctly) allow the
ideas contained in programs not released with source code to become
available to the public domain, as they were always intended to. The
novel ideas can be patented (unless you believe that all software
patents are bad); this does at least disclose the ideas (they are freely
readable by all) and can freely be used by all once the patent expires.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
