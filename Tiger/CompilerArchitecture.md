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
    Page](http://www.program-transformation.org/edit/Tiger/CompilerArchitecture?t=1536825753)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/CompilerArchitecture)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/CompilerArchitecture)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/CompilerArchitecture?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/CompilerArchitecture?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Tiger/CompilerArchitecture?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tiger/CompilerArchitecture?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tiger/CompilerArchitecture?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/CompilerArchitecture?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tiger/CompilerArchitecture?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/CompilerArchitecture)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/CompilerArchitecture?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Tiger/CompilerArchitecture?template=oopsmore&param1=1.3&param2=1.3)
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
Compiler Architecture {#compiler-architecture .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

The diagram below depicts the data flow in the
[TigerCompiler](TigerCompiler){.twikiLink} for the
[HpcProject](HpcProject){.twikiLink}. Red edges denote the data flow of
the compiler. Green edges denote data flow in the interpreter. The idea
is that a compiled program should produce the same output as the same
program interpreted. Black edges denote utilities such as
[PrettyPrinters[^?^](http://www.program-transformation.org/edit/Tiger/PrettyPrinters?topicparent=Tiger.CompilerArchitecture)]{.twikiNewLink
style="background : #FFFFCE;"} and
[FormatCheckers[^?^](http://www.program-transformation.org/edit/Tiger/FormatCheckers?topicparent=Tiger.CompilerArchitecture)]{.twikiNewLink
style="background : #FFFFCE;"}. Edges are labeled with the name of the
[CompilerComponent](CompilerComponent){.twikiLink}. The boxes correspond
to the [CompilerPackages](CompilerPackages){.twikiLink} in which the
compiler is divided. The names in the ellipses show the name of the
program (`f`) and the file extension. The file extension can be used
with the make targets in the
[TigerMakeRules[^?^](http://www.program-transformation.org/edit/Tiger/TigerMakeRules?topicparent=Tiger.CompilerArchitecture)]{.twikiNewLink
style="background : #FFFFCE;"} to create the corresponding intermediate
result.

There is also an abbreviated
[CompilerOverview](CompilerOverview){.twikiLink} and extracts of this
diagram depicting the
[FrontEndArchitecture](FrontEndArchitecture){.twikiLink},
[OptimizerArchitecture](OptimizerArchitecture){.twikiLink}, and
[BackEndArchitecture](BackEndArchitecture){.twikiLink}.

![architecture.gif](http://www.cs.uu.nl/~visser/teach/hpc/architecture.gif)\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
