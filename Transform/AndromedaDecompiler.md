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
    Page](http://www.program-transformation.org/edit/Transform/AndromedaDecompiler?t=1536826426)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/AndromedaDecompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/AndromedaDecompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/AndromedaDecompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/AndromedaDecompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/AndromedaDecompiler?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/AndromedaDecompiler?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/AndromedaDecompiler?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/AndromedaDecompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/AndromedaDecompiler?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/AndromedaDecompiler?template=oopsmore&param1=1.2&param2=1.2)
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
Andromeda Decompiler {#andromeda-decompiler .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

<http://shulgaaa.at.tut.by>

The Andromeda Decompiler is still in development. At present, it will
only run on Windows, and only decompile Windows-based programs to C/C++.
There is a demo that is downloadable; the demo is not the complete
decompiler. The loader is disabled, so it is only possible to browse the
provided project, a medium sized C++ program.

There are three main views: output code, assembly language (not every
instruction is visible), and hex dump. The output code can be
\"unfolded\" (where data flow is not performed, so condition codes etc
are still visible), and \"unblocked\" (where for example all
if/then/else are replaced by if/goto). Two views (code, with or without
blocking, with or without folding) or assembly can be open at once,
synchronised if desired.

Whole lines can be selected with a click, or a part of an expression can
be selected with a control-click. The right mouse button presents a menu
of options. There are also a dozen or so commands available from the
Edit menu. As an example, the eXpand command can be used to include a
default arm into a switch statement (if it isn\'t there already).

It seems quite sensible at determining types for variables, and seems to
determine parameters and returns correctly. It may have trouble with
indirect calls. However, there are commands for manually changing these
things.

Overall, this is very impressive. It may be rather compiler specific
(i.e. makes assumptions about the compiler that compiled the input
binary file).

The author hopes to provide some documentation on the above web site
soon (as of mid October).

See also the [Andromeda Decompiler
Test](DecompilerAndromedaTest){.twikiLink} page.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
