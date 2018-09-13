::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/StrategoCompiler?t=1536825372)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Stratego/StrategoCompiler?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/StrategoCompiler?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/StrategoCompiler?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/StrategoCompiler?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/StrategoCompiler?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/StrategoCompiler?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoCompiler?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoCompiler?template=oopsmore&param1=1.8&param2=1.8)
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
Stratego Compiler {#stratego-compiler .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Introduction} Introduction
------------------------------

The Stratego Compiler translates a Stratego specification to a C
program. The compiler is completely implemented in Stratego (except for
the parser, which is implemented in [SDF](SDF){.twikiLink}). The
Stratego Compiler is part of the Stratego/XT distribution. The main
components of the Stratego Compiler are part of the strc package. This
package is one of the core [packages of
Stratego/XT](StrategoXTPackages){.twikiLink}.

The entry point to the Stratego Compiler is the
[strc](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/ref-strc.html)
command.

[]{#Architecture} Architecture
------------------------------

The compiler components of the strc package compile an Stratego program
in abstract syntax to a C program. The components are separated in:

-   [Stratego FrontEnd](StrategoFrontEnd){.twikiLink}
-   [Stratego Optimizer](StrategoOptimizer){.twikiLink}
-   [Stratego BackEnd](StrategoBackEnd){.twikiLink}

The [stratego-front](StrategoFront){.twikiLink} packages defines the
concrete syntax of Stratego and provides tools for parsing and
desugaring Stratego programs.

[]{#Data_flow} Data flow
------------------------

A data flow diagram of components of the Stratego Compiler is
automatically generated by
[xdoc](ExtendibleDocumentationGenerator){.twikiLink}. The most recent
version is available [here](http://www.levellers.nl/strc.ps).

The following (out of date) data-flow diagram below depicts the
architecture of the compiler. Boxes depict data and ellipses depict
executable compiler components. Solid arrows depict data-flow. Dashed
arrows depict control-flow. The components are driven by the main
compiler component `sc`, which is not shown in the diagram.

![architecture.gif](http://www.stratego-language.org/sc/architecture.gif)

[CategoryCompiler](CategoryCompiler){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
