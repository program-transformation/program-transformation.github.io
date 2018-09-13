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
    Page](http://www.program-transformation.org/edit/Tiger/UsingTheComponents?t=1536826687)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/UsingTheComponents)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/UsingTheComponents)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/UsingTheComponents?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/UsingTheComponents?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/UsingTheComponents?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/UsingTheComponents)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/UsingTheComponents?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/UsingTheComponents?template=oopsmore&param1=1.1&param2=1.1)
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
Using The Components {#using-the-components .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

The `xmpl/` directory in the [TigerXmpl](TigerXmpl){.twikiLink} package
contains a number of example Tiger programs (partly copied from the
[ModernCompilerImplementation[^?^](http://www.program-transformation.org/edit/Stratego/ModernCompilerImplementation?topicparent=Tiger.UsingTheComponents)]{.twikiNewLink
style="background : #FFFFCE;"} site) and a Makefile for applying
components to the examples.

Examples of usage are

-   `gmake prog.tas`: to make Tiger abstract syntax from `prog.tig`

<!-- -->

-   `gmake prog.txt`: to \`pretty-print\' `prog.tig`

<!-- -->

-   `gmake prog.ir`: to translate `prog.tig` to
    [IntermediateRepresentation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}

<!-- -->

-   `gmake prog.s`: to make the
    [MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}
    assembly language implementation of `prog.tig`

See the `Makefile.pkg` ffiles for all the available targets.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 14 Sep 2002\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
