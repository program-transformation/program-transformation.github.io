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
    Page](http://www.program-transformation.org/edit/Transform/DotNetDecompilers?t=1536826292)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DotNetDecompilers)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DotNetDecompilers)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DotNetDecompilers?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DotNetDecompilers?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    14](http://www.program-transformation.org/view/Transform/DotNetDecompilers?rev=1.14)
    [(diff 13)](http://www.program-transformation.org/rdiff/Transform/DotNetDecompilers?rev1=1.14&rev2=1.13)
-   [Rev
    13](http://www.program-transformation.org/view/Transform/DotNetDecompilers?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Transform/DotNetDecompilers?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Transform/DotNetDecompilers?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Transform/DotNetDecompilers?rev1=1.12&rev2=1.11)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DotNetDecompilers)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DotNetDecompilers?template=oopsmore&param1=1.14&param2=1.14)
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
    \...](http://www.program-transformation.org/oops/Transform/DotNetDecompilers?template=oopsmore&param1=1.14&param2=1.14)
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
Dot Net Decompilers {#dot-net-decompilers .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#NET_Decompiler_Comparison}[]{#_NET_Decompiler_Comparison} .NET Decompiler Comparison
----------------------------------------------------------------------------------------

-   See [Dot Net Decompiler Tests](DotNetDecompilerTests){.twikiLink}

[]{#NET_Decompilers}[]{#_NET_Decompilers} .NET Decompilers
----------------------------------------------------------

-   [Salamander](http://www.remotesoft.com/salamander) is a commercial
    decompiler for .NET. The web page allows decompiling of moderately
    sized programs online. It seems to recognise the source language,
    and automatically generates source code in C\#, managed C++, Visual
    Basic.NET, JScript.NET etc. First release was 1st Feb 2002. There
    are several examples online. For some tests see
    [DecompilationSalamanderTest](DecompilationSalamanderTest){.twikiLink}.

<!-- -->

-   [Anakrino](http://www.saurik.com/net/exemplar/) is a .NET (more
    correctly CIL, sometimes called MSIL, i.e. CLR executable files) to
    C\# decompiler. The web page is a little difficult to get an
    overview of, since the latest news is at the top. Source code is
    available online. The command line version seems to be called
    **Exemplar**. See also [this
    article](http://www.dotnetcoders.com/web/Articles/ShowArticle.aspx?article=40)
    from [dotnetcoders.com](http://www.dotnetcoders.com). For some tests
    see
    [DecompilationAnakrinoTest](DecompilationAnakrinoTest){.twikiLink}.

<!-- -->

-   [LSW
    DotNet-Reflection-Browser](http://www.lesser-software.com/lswdnrb.htm)
    is a commercial .NET object browser, disassembler, and decompiler.
    It is a native Windows application. Downloads are free, but it is
    not capable of any decompilation without registration (starts at
    US\$99 as of March 2003). They do have an extended example, which
    does not recompile with Mono. For example, there are calls to
    `point..ctor()` (presumably, a constructor for the `point` object),
    variable `m` is declared as both a `Message` and later as an `int` ,
    local variables are declared at the start of the function, not where
    they come into scope, and so on. There are many `goto` s in the
    example decompilation.

<!-- -->

-   [Lutz Roeder\'s
    Programming.NET](http://www.aisto.com/roeder/dotnet/) page has
    released Reflector for .NET. From the web page: *Reflector is a
    class browser for .NET components and assemblies. It features
    hierarchical assembly and namespace views, type and member
    dictionary index search, type reference search, custom attributes
    view, IL disassembler, C\# decompiler, VB decompiler, viewers for
    C\# XML docs and MSDN help. Assembly dependency trees,
    supertype/subtype hierarchies and resources can be inspected as
    well.* Function prototypes are displayed in C\# and VB syntax. Full
    source code is available. Also decompiles in Delphi-like and Visual
    Basic flavours. See also
    [DecompilationReflectorTest](DecompilationReflectorTest){.twikiLink}.

<!-- -->

-   [Dis\#](http://www.netdecompiler.com/). *The main problem of
    decompilation is the absence of full source information in the
    executable file. Dis\# allows the editing of local variables and
    other names and these changes persist in project file. Generated
    source code becomes more similar to the original source.*
    Proprietary software; a trial version is available.

<!-- -->

-   [9rays.net](http://9rays.net) sells a product called
    [spices.net](http://www.9rays.net/cgi-bin/components.cgi?act=1&cid=86),
    which can include a plugin called
    [spices.decompiler](http://www.9rays.net/cgi-bin/components.cgi?act=2&cid=86).
    This decompiles to IL (disassembles the .NET bytecodes), C\#, Visual
    Basic, C++, J\#, Delphi.

<!-- -->

-   [Decompiler.net](http://www.junglecreatures.com/DesktopDefault.aspx?tabindex=3&tabid=3)
    is a *combination decompiler, obfuscator, language translator, and
    refactoring tool for Microsoft .NET managed applications and
    libraries*. Commercial decompiler from
    [www.junglecreatures.com](http://www.junglecreatures.com). A
    restricted trial version is available. Decompiler.net received a
    good review from [.NET Developer\'s
    Journal](http://dotnet.sys-con.com)\'s article \"[Decompiler
    Round-Up, Regenerating Your
    Code](http://dotnet.sys-con.com/read/45917.htm)\".

<!-- -->

-   Microsoft provides a **CIL** (Common Intermediate Language)
    **disassembler** called **ILDASM** with all its compilers. A
    disassembler is certainly not a decompiler, but ILDASM has the
    **\"round tripping\"** ability. This means that is it possible to
    take a CIL binary file to which you don\'t have the source code,
    disassemble it (to ILAsm format, not pretty), make some changes, and
    then reassemble it. Most disassembler / assembler pairs are not
    capable of this round tripping, because of a host of issues.
    However, the CIL format avoids all these problems. So without the
    source code to a program, you can achieve some of the things that
    normally you would want a decompiler for (e.g. making small
    changes). It is, presumably, part of the .NET framework SDK
    [download
    page](http://msdn.microsoft.com/library/default.asp?url=/downloads/list/netdevframework.asp)).
    See also this [C\# Intermediate Language Disassembler
    (ILDASM)](http://www.csharphelp.com/archives/archive23.html) page.

[]{#DotNetLinks}

[]{#NET_Links}[]{#_NET_Links} .NET Links
----------------------------------------

-   <http://www.dotnet-collective.com>, a comprehensive collection of
    .NET resources by Tony O\'Hagan.

<!-- -->

-   <http://www.ikvm.net>, an implementation of the Java VM in .NET.
    There is also a tool called
    [ikvmc](http://www.ikvm.net/userguide/ikvmc.html) which translates
    Java bytecode (compiled) programs to .NET in various forms.

<!-- -->

-   <http://dotnet.wikis.com>, a wiki site denoted to .NET

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
