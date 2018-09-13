::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![Stratego
logo](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)

------------------------------------------------------------------------

***Tiger in Stratego***

------------------------------------------------------------------------

**[WebHome](WebHome){.twikiLink}**\
[Tiger Compiler](TigerCompiler){.twikiLink}\
[Architecture](CompilerArchitecture){.twikiLink}\
[Packages](CompilerPackages){.twikiLink}\
[Components](CompilerComponent){.twikiLink}\
[Glossary](WebGlossary){.twikiLink}

[Download](DownloadAndInstallation){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tiger/HighPerformanceCompilersCourse?t=1536826692)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HighPerformanceCompilersCourse)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HighPerformanceCompilersCourse)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HighPerformanceCompilersCourse?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HighPerformanceCompilersCourse?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Tiger/HighPerformanceCompilersCourse?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tiger/HighPerformanceCompilersCourse?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tiger/HighPerformanceCompilersCourse?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/HighPerformanceCompilersCourse?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tiger/HighPerformanceCompilersCourse?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HighPerformanceCompilersCourse)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HighPerformanceCompilersCourse?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Tiger/HighPerformanceCompilersCourse?template=oopsmore&param1=1.3&param2=1.3)
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
High Performance Compilers Course {#high-performance-compilers-course .twikiTopicTitle}
=================================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

This is the Wiki entry for the course on High-Performance Compilers
given at Utrecht University in the Fall of 2000.

The official website of the course is
<http://www.cs.uu.nl/~visser/teaching/hpc/>

------------------------------------------------------------------------

**Administrativa**

Meetings are on Tuesdays and Fridays from 11 to 14 in Room Stratego.CGZ
Stratego.F216 (Tuesday) and Room Stratego.Trans1 116 (Friday).

During some of the meetings there will be a lab session in Room
Stratego.CGN Stratego.C009.

------------------------------------------------------------------------

**Course Resources**

-   [HpcAnnouncements[^?^](http://www.program-transformation.org/edit/Stratego/HpcAnnouncements?topicparent=Tiger.HighPerformanceCompilersCourse)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [HpcSchedule[^?^](http://www.program-transformation.org/edit/Stratego/HpcSchedule?topicparent=Tiger.HighPerformanceCompilersCourse)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [HpcProject[^?^](http://www.program-transformation.org/edit/Trash/HpcProject?topicparent=Tiger.HighPerformanceCompilersCourse)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [HpcExercises[^?^](http://www.program-transformation.org/edit/Stratego/HpcExercises?topicparent=Tiger.HighPerformanceCompilersCourse)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [StrategoAtCSUUNL[^?^](http://www.program-transformation.org/edit/Stratego/StrategoAtCSUUNL?topicparent=Tiger.HighPerformanceCompilersCourse)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [TigerInStratego[^?^](http://www.program-transformation.org/edit/Hpc/TigerInStratego?topicparent=Tiger.HighPerformanceCompilersCourse)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [HpcBooks[^?^](http://www.program-transformation.org/edit/Stratego/HpcBooks?topicparent=Tiger.HighPerformanceCompilersCourse)]{.twikiNewLink
    style="background : #FFFFCE;"}

------------------------------------------------------------------------

**Tools**

-   [StrategoLanguage](../Stratego/StrategoLanguage){.twikiLink}:
    <http://www.stratego-language.org/>
-   Transformation Tools (Stratego.XT):
    <http://www.program-transformation.org/xt>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Hpc.HighPerformanceCompilersCourse moved from
Stratego.HighPerformanceCompilersCourse on 01 Dec 2001 - 17:01 by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}*
:::
:::
:::
:::
