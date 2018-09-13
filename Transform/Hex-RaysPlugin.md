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
    Page](http://www.program-transformation.org/edit/Transform/Hex-RaysPlugin?t=1536826495)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/Hex-RaysPlugin)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/Hex-RaysPlugin)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/Hex-RaysPlugin?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/Hex-RaysPlugin?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/Hex-RaysPlugin?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/Hex-RaysPlugin?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/Hex-RaysPlugin?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/Hex-RaysPlugin?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/Hex-RaysPlugin?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/Hex-RaysPlugin?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/Hex-RaysPlugin)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/Hex-RaysPlugin?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/Hex-RaysPlugin?template=oopsmore&param1=1.4&param2=1.4)
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
Hex-RaysPlugin {#hex-raysplugin .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

<http://www.hex-rays.com>\
<http://hexblog.com/2007/04/decompilation_gets_real.html>\
<http://www.hexblog.com/hexrays/manual>

Hex-Rays is a decompiler plug-in for the IDA Pro disassembler. As of Sep
2007, version 1 has been released. It currently supports 32-bit x86 only
(32-bit versions of Windows, Linux, and presumably Intel OS/X), and
relies on the intermediate representation of a program as interactively
created in IDA Pro. Version 5.1 of IDA Pro is required. Floating point
is not supported at present. The output is not designed to be
recompiled. Output is quite C-like, and affords an overview of a binary
program.

Procedures can be viewed one at a time, or there is an option to
translate all procedures to C, or just a selected range of code. Some
procedures fail to be decompiled for various reasons. Compound
conditionals, arrays, and structures are supported, and functions are
inlined into expressions. Parameters and returns are handled as per the
disassembly view. While in the decompiler view, you can perform a
(currently) very limited set of commands, including following calls,
returning to the caller, and renaming functions and variables.

The first version of the decompiler SDK was released in November 2007;
this allows the decompiler to be extended in various ways by users. The
author states that user interface improvements and provision for
decompiling other platforms are the next areas of focus.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
