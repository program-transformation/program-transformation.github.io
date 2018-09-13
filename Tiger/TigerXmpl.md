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
    Page](http://www.program-transformation.org/edit/Tiger/TigerXmpl?t=1536826648)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/TigerXmpl)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/TigerXmpl)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/TigerXmpl?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/TigerXmpl?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Tiger/TigerXmpl?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tiger/TigerXmpl?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tiger/TigerXmpl?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/TigerXmpl?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tiger/TigerXmpl?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/TigerXmpl)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/TigerXmpl?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Tiger/TigerXmpl?template=oopsmore&param1=1.3&param2=1.3)
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
Tiger Xmpl {#tiger-xmpl .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

The [TigerXmpl](TigerXmpl){.twikiLink} package provides a directory with
example Tiger programs and a makefile for testing the various
[TigerCompiler](TigerCompiler){.twikiLink} components. The makefile
imports make-rules files installed by the other
[CompilerPackages](CompilerPackages){.twikiLink}.

**Download**

-   <http://www.stratego-language.org/ftp/tiger-xmpl-0.2.tar.gz>

**Installation**

    > gtar zxf tiger-xmpl-0.2.tar.gz
    > cd tiger-xmpl-0.2
    > ./configure --with-xt=/projects/stratego/xt --with-tiger=/tiger/install/dir
    > gmake

Note: `--with-xt` is necessary even if you add the directory
`/projects/stratego/xt/bin` to your `$PATH`, since the Tools.XT
components are addressed using variables in the makerules, e.g.,
`$(SGLR)/bin/sglr`.

Configuration with `--with-tiger` assumes that all the
[CompilerPackages](CompilerPackages){.twikiLink} are configured with the
same prefix.

**Testing**

You can now test (components of) the compiler; see
[HowToTestTheTigerCompiler](HowToTestTheTigerCompiler){.twikiLink}.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
