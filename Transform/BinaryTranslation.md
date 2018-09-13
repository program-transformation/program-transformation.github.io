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
    Page](http://www.program-transformation.org/edit/Transform/BinaryTranslation?t=1536826295)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/BinaryTranslation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/BinaryTranslation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/BinaryTranslation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/BinaryTranslation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    22](http://www.program-transformation.org/view/Transform/BinaryTranslation?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Transform/BinaryTranslation?rev1=1.22&rev2=1.21)
-   [Rev
    21](http://www.program-transformation.org/view/Transform/BinaryTranslation?rev=1.21)
    [(diff 20)](http://www.program-transformation.org/rdiff/Transform/BinaryTranslation?rev1=1.21&rev2=1.20)
-   [Rev
    20](http://www.program-transformation.org/view/Transform/BinaryTranslation?rev=1.20)
    [(diff 19)](http://www.program-transformation.org/rdiff/Transform/BinaryTranslation?rev1=1.20&rev2=1.19)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/BinaryTranslation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/BinaryTranslation?template=oopsmore&param1=1.22&param2=1.22)
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
    \...](http://www.program-transformation.org/oops/Transform/BinaryTranslation?template=oopsmore&param1=1.22&param2=1.22)
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
Binary Translation {#binary-translation .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Binary_Translation} Binary Translation
------------------------------------------

### []{#What_is_binary_translation} What is binary translation

Binary tanslation is the process of automatically translating binary
object code from one machine Mi to another. The machines are normally
different. Binary translation either takes place at software or hardware
level.

There are three ways, which binary translation may take place, ranging
from the most difficult to more easy translation:

Translation of applications by software:

\- If the machines and the operating systems are different. In this case
we are interested in both translating the applications from the source
machine, but also in trapping or translating the operating system calls
from the source machine to the operating system supported on the target
machine. Often, the solution to this problem is to have an virtual
machine supporting the source machine. No research projects are known at
this time.

\- If the machines are different, but supports the same operating
system. In this case we are interested in translating the applications,
like SIND, UBQT, UBDQT and Walkabout frameworks.

Translation of operating systems by software: - If the machines are
different and we want the object code for the source machine to run on
the target machine. In this case we want to translate object code from
the source machine to the target, like LLVA-emu project.

In the latter case, we also meet translation of operating systems by
hardware, like DAISY and BOA.

Another area, which is mistakenly supposed to be binary translation is,
if the machines are the same and support different operating systems. In
this case this is not really binary translation, rather we are
interested in trapping operating system calls from the application
compiled for the source machine to use the operating system
[API](API){.twikiLink} on the target machine, like Wine on Linux x86
machines.

### []{#Why_use_binary_translation} Why use binary translation

As new and faster processor architectures are becoming available there
exists a growing number of appliactions written for old architectures
where recompilation are more difficult than translating the object code,
due to the lack of source code or difficulties with upgrading the
application (Diamond and japanese project).

Another reason to use software binary translation, is the ability to use
different machines to support the same operating system. Moreover, it
gets more interesting, if the operating system has distributed
capabilities, like the older TAOS operating system, which used a virtual
instruction set.

The future may hopefully show a hybrid between the LLVA-emu project and
<http://www.openmosix.org> or something similar.

### []{#Links} Links

The following links are to works directly or indirectly related to
binary translation.

-   [BinaryTranslationResearch](BinaryTranslationResearch){.twikiLink}
-   [BinaryOptimisers](BinaryOptimisers){.twikiLink}
-   [BinaryTranslationProducts](BinaryTranslationProducts){.twikiLink}
-   [JavaDynamicCompilers](JavaDynamicCompilers){.twikiLink}
-   [JavaNativeCompilers](JavaNativeCompilers){.twikiLink}
-   [BinaryTranslationProcessors](BinaryTranslationProcessors){.twikiLink}
    -   [HardwareAssistance](BinaryTranslationProcessors#HardwareAssistance){.twikiAnchorLink}
-   [BinaryTranslationWorkshops](BinaryTranslationWorkshops){.twikiLink}
-   [BinaryTranslationLinks](BinaryTranslationLinks){.twikiLink}

[CategoryDecompilation](CategoryDecompilation){.twikiLink}
[CategoryBinaryTranslation](CategoryBinaryTranslation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
