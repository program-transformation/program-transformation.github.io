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
    Page](http://www.program-transformation.org/edit/Transform/DccDecompiler?t=1536826453)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DccDecompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DccDecompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DccDecompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DccDecompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Transform/DccDecompiler?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/DccDecompiler?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/DccDecompiler?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DccDecompiler?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/DccDecompiler?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DccDecompiler?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DccDecompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DccDecompiler?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Transform/DccDecompiler?template=oopsmore&param1=1.5&param2=1.5)
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
Dcc Decompiler {#dcc-decompiler .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

dcc is a research decompiler, written as a proof of concept for
[Cristina Cifuentes](CristinaCifuentes){.twikiLink}\' [PhD
thesis](http://www.program-transformation.org/twiki/bin/viewfile/Transform/CristinaCifuentes?rev=/sw/bin/rlog%20%20-h%20/users/www/staff/research/projects/stratego/twiki/pub/Transform/CristinaCifuentes/decompilation_thesis.ps.gz,v&filename=decompilation_thesis.ps.gz).

A complete
[distribution](http://www.itee.uq.edu.au/~cristina/dcc.html#distrib) of
dcc (executable, source, tools to generate signatures, etc) is
available. The authors ask users to first read the [readme
file](http://www.itee.uq.edu.au/~cristina/dcc/dcc_readme.html), before
downloading the archive. It may also be worth visiting the [dcc home
page](http://www.itee.uq.edu.au/~cristina/dcc.html). Please note that
the authors are not currently working on this project so they cannot
support any changes to the distribution. The distribution contains known
bugs. Only small 80286 DOS programs can be decompiled, and only to C
(not C++).

The research done by this group has focused on reconstructing the
original control-flow from the assembly instructions. They also have a
hash-based recognizing tool for libraries. The program lacks a complete
coverage of all instructions (e.g., the floating point instructions are
missing), and does not do anything in the area of data type
reconstruction.

For tests, see [Dcc decompiler tests](DccDecompilerTests){.twikiLink}.

In 2002, André Janz wrote a diploma thesis entitled [\"Experimente mit
einem Decompiler im Hinblick auf die forensische
Informatik\"](http://agn-www.informatik.uni-hamburg.de/papers/doc/diparb_andre_janz.pdf)
(\"Experiments with a Decompiler regarding forensic Computer Science\").
He modified the source code for dcc to read Win32 Portable Executable
(PE) files. With the help of web translation tools, it seems to me that
the conclusion was that while a rewrite would be needed to properly
represent programs in the 80386 instruction set, reasonable results were
obtained. It seems the author even added Win32 signature recognition. I
could not find a [URL](URL){.twikiLink} to download the source code.

------------------------------------------------------------------------

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.DccDecompiler moved from Transform.DecompilationDcc on 02 Mar
2005 - 07:24 by [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Transform/DccDecompiler?newweb=Transform&newtopic=DecompilationDcc&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
