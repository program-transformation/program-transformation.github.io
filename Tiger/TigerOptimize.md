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
    Page](http://www.program-transformation.org/edit/Tiger/TigerOptimize?t=1536826655)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/TigerOptimize)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/TigerOptimize)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/TigerOptimize?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/TigerOptimize?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tiger/TigerOptimize?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/TigerOptimize?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tiger/TigerOptimize?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/TigerOptimize)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/TigerOptimize?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tiger/TigerOptimize?template=oopsmore&param1=1.2&param2=1.2)
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
Tiger Optimize {#tiger-optimize .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

[TigerOptimize](TigerOptimize){.twikiLink} is a component of the
[TigerCompiler](TigerCompiler){.twikiLink} in the
[TigerOpt](TigerOpt){.twikiLink} package. The component applies various
[ProgramOptimizations](../Transform/ProgramOptimization){.twikiLink} at
the level of
[TigerAbstractSyntax](http://www.program-transformation.org/Tiger/TigerAbstractSyntax){.twikiLink}
expressions.

Examples of optimizations that can be applied:

-   [ConstantFolding[^?^](http://www.program-transformation.org/edit/Transform/ConstantFolding?topicparent=Tiger.TigerOptimize)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ConstantPropagation[^?^](http://www.program-transformation.org/edit/Transform/ConstantPropagation?topicparent=Tiger.TigerOptimize)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [DeadCodeElimination[^?^](http://www.program-transformation.org/edit/Transform/DeadCodeElimination?topicparent=Tiger.TigerOptimize)]{.twikiNewLink
    style="background : #FFFFCE;"}

As distributed the implementation of the component defines the identity
transformation.

[DynamicRules](../Stratego/DynamicRule){.twikiLink} are very useful for
implementing source to source transformations.

------------------------------------------------------------------------

[CompilerComponent](CompilerComponent){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
