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
    Page](http://www.program-transformation.org/edit/Transform/AnatomizerDecompiler?t=1536826425)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/AnatomizerDecompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/AnatomizerDecompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/AnatomizerDecompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/AnatomizerDecompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/AnatomizerDecompiler?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/AnatomizerDecompiler?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/AnatomizerDecompiler?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/AnatomizerDecompiler?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/AnatomizerDecompiler?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/AnatomizerDecompiler?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/AnatomizerDecompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/AnatomizerDecompiler?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/AnatomizerDecompiler?template=oopsmore&param1=1.4&param2=1.4)
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
Anatomizer Decompiler {#anatomizer-decompiler .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Web sites (all in Japanese):

-   <http://jdi.at.infoseek.co.jp/> \"Anatomizer entrance\" with legal
    matter
-   <http://jdi.at.infoseek.co.jp/japanese/index.plg> Main page
-   <http://jdi.tripod.co.jp/japanese/> Alternative address for the main
    page
-   <http://jdi.at.infoseek.co.jp/japanese/download.plg> Download page
-   Try the [Babel Fish
    Translation](http://babelfish.altavista.com/babelfish/trurl_pagecontent?lp=ja_en&trurl=http%3a%2f%2fjdi.at.infoseek.co.jp)
    for the entrance page. Something about the page makes it better to
    view it in Internet Explorer.

This binary decompiler for Win32 executables seems to have been in
existance at least since early 2002. It is still at a quite early stage.
There are a few parts that are surprisingly good, but these are probably
the result of low level pattern matching, rather than general principes
that would work for all code from all compilers.

The web pages are entirely in Japanese, which I cannot read. I have
found a few clues from the fragments of English interspersed with
Japanese, along with a
[Babelfish](http://babelfish.altavista.com/babelfish/tr) translation.
There seem to be three binaries available for download:

-   <http://jdi.at.infoseek.co.jp/japanese/anatomizer1605.zip> (June
    2004; version 1.06.0005; written in Visual Basic)
-   <http://jdi.at.infoseek.co.jp/japanese/anatomizer150b3.zip> (Dec
    2003; version 1.5B3; written in C++)
-   <http://jdi.at.infoseek.co.jp/japanese/anatomizer150a.zip> (Nov
    2003; version 1.5 alpha; written in C++)

The C++ versions require MFC71.DLL, MSVCR71.DLL and MSVCP71.DLL. I could
not get the alpha version to decompile anything, not even the [sample
program](http://jdi.at.infoseek.co.jp/japanese/sample.lzh) from the web
site. The VB version seems to take a very long time intitialising after
loading larger program files. The 1.5B3 version seems to have severe
output windows clipping problems. So the VB program would appear to be
the best one to use, despite being a bit slow to start (and sometimes
seems to just crash silently immediately after loading.)

The way to get a decompilation seems to be to open an executable
(control-O on the 2004 version), choose an entry point (the upper option
seems to work so far, (E) on some versions), then from the (R) menu
choose (D) (control-D on the 2004 version) to get a list of procedures,
select one, and from the (R) menu, choose (A) (control-A on the 2004
version) to see a decompilation. You can highlight the decompiled output
and copy to the clipboard with control-C, or use the right mouse menu to
select all, copy, etc. There is an option in the decompilation window to
print the address of each basic block as a comment (left of 2 check
boxes). The right hand checkbox seems to add the hex address of a call
as a comment (e.g. // 01003740 in front of call proc\_0019). Once you
have done one decompilation, you can double click on a procedure in the
procedure window to decompile it, replacing the existing decompilation.

Here is a small sample of output, from Boomerang\'s
test/windows/lpq.exe. The disassembly is from objdump; I can\'t figure
out how to copy the disassembly output to the clipboard as yet.

     18c11f7:       8b 44 24 08             mov    0x8(%esp),%eax
     18c11fb:       23 44 24 04             and    0x4(%esp),%eax
     18c11ff:       2b 44 24 08             sub    0x8(%esp),%eax
     18c1203:       83 f8 01                cmp    $0x1,%eax
     18c1206:       1b c0                   sbb    %eax,%eax
     18c1208:       f7 d8                   neg    %eax
     18c120a:       c2 08 00                ret    $0x8

    long proc_0002(void arg1, void arg2)
    /* 018C11F7 - 018C120C
     * Size : 22 ( 0x00000016 )
     * Takes 8 Bytes parameters.
     * Pascal calling convention.
     * Call from proc_0001.
     */
    {
        register long loc1; /* EAX */

        loc1 = (arg2 & arg1) - arg2;
        /* Unsupported operation. */
        _asm{018C1206 1BC0                SBB        EAX,EAX};
        return (!loc1);
    }

The register variable is declared, and the AND and SUB instructions are
combined into a suitable expression. Unfortunately, the SBB idiom is not
recognised, and the NEG instruction is dubiously translated into a ! (C
not) operator. Parameters are declared but not typed, so this code would
not compile. The return value is typed, and the return value is used
sensibly in proc\_0001 (with `if (proc_0002() = 0) {`).

For larger examples, see [Anatomizer Decompiler
Test](AnatomizerDecompilerTest){.twikiLink}.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 01 Aug 2005\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
