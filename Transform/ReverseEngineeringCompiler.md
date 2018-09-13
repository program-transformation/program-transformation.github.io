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
    Page](http://www.program-transformation.org/edit/Transform/ReverseEngineeringCompiler?t=1536826549)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ReverseEngineeringCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ReverseEngineeringCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ReverseEngineeringCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ReverseEngineeringCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/ReverseEngineeringCompiler?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/ReverseEngineeringCompiler?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/ReverseEngineeringCompiler?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/ReverseEngineeringCompiler?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/ReverseEngineeringCompiler?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/ReverseEngineeringCompiler?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ReverseEngineeringCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ReverseEngineeringCompiler?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/ReverseEngineeringCompiler?template=oopsmore&param1=1.4&param2=1.4)
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
Reverse Engineering Compiler {#reverse-engineering-compiler .twikiTopicTitle}
============================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

<http://www.backerstreet.com/rec/rec.htm>

REC, a Reverse Engineering Compiler by Giampiero Caprino
(<gcaprino@katamail.com>), is a portable decompiler which supports a
variety of different input binary files and produces a C-like
representation as output. Source processors supported at present
include: Intel 386, Motorola 68000, MIPS R3000 and Motorola PowerPC.
Version 1.6 also supports SPARC. Amongst the source binary file formats
accepted are: Unix Elf, Unix COFF, Windows PE, Linux and SunOS AOUT,
PlayStation PS-X, and raw binary data.

As of mid 2005, the author appears to be back working on this
decompiler, and has produced a Windows GUI called
[RecStudio](http://www.backerstreet.com/rec/rec2.htm). It will be
interesting to see where this leads.

REC started as a workbench to test compiler related algorithms. Its
author, Giampiero Caprino, has worked on this project on an on and off
basis for several years and uses the Linux platform for development. REC
source is *not* in the public domain, but binaries for several popular
operating systems are freely downloadable from the website at
<http://www.backerstreet.com/rec/rec.htm>.

Some of the features of REC include:

-   Recognizes dynamically and statically linked functions like printf,
-   Recovers control structure information correctly,
-   Gets arguments to variable length routines such as printf correct,
-   Supports the information provided by the -g option, hence recovering
    correct names for all variables and routines,
-   For each routine provides the name (if known), argument size, local
    variables size, and saved register size,
-   Generates good code.

As of version 1.4a there is [HTML](HTML){.twikiLink} support at its user
interface level, as well as a HTTP proxy server. Users can therefore
decompile programs remotely over the internet.

As of version 1.4a, minor bugs that could be easily fixed include:

-   Easily confused by nulls on Solaris; these are rarely used on Linux
-   Return types are not correct; returns to eax even when using void
    routines
-   Does not handle global static arrays of initialized strings
-   A pattern for gcc\'s signed divide by 2 is needed to avoid emiting
    an expression that includes an arithmetic right shift by 31 bits
    followed by a logical right shift of 31 bits
-   Arrays are left as expressions at present; they are not processed
    into array notation
-   Uses globals for register variables instead of allocating a local
    variable
-   Registers are still available on the output; in many cases they can
    be removed
-   Gets confused by call \$+8 instructions, which are common in
    position independent code

Overall, REC is a great attempt at a portable decompiler. It needs some
data flow and type recovery analyses to produce better code. Development
seems to have stopped in September 2000 with version 1.6, until 2005
when the author returned to REC development. For some tests of the older
version see [DecompilerRecTest](DecompilerRecTest){.twikiLink}.

Note also a serious problem: REC assumes that the stack pointer does not
change between the prologue and epilogue of a procedure. This is not
valid for programs using the \"omit frame pointer\" optimisation (or
equivalent), including many Windows programs compiled with MSVC. For
more details, see the paper [Using a Decompiler for Real-World Source
Recovery](http://www.itee.uq.edu.au/~emmerik/experience_long.pdf).

Readers attempting to evaluate REC should note that you need `-gstabs`
(not just `-g` as stated in the REC manual) for creating object files to
be used with the `files:` option of a `.cmd` file.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
