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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoXTPackages?t=1536825460)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoXTPackages)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoXTPackages)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoXTPackages?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoXTPackages?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    20](http://www.program-transformation.org/view/Stratego/StrategoXTPackages?rev=1.20)
    [(diff 19)](http://www.program-transformation.org/rdiff/Stratego/StrategoXTPackages?rev1=1.20&rev2=1.19)
-   [Rev
    19](http://www.program-transformation.org/view/Stratego/StrategoXTPackages?rev=1.19)
    [(diff 18)](http://www.program-transformation.org/rdiff/Stratego/StrategoXTPackages?rev1=1.19&rev2=1.18)
-   [Rev
    18](http://www.program-transformation.org/view/Stratego/StrategoXTPackages?rev=1.18)
    [(diff 17)](http://www.program-transformation.org/rdiff/Stratego/StrategoXTPackages?rev1=1.18&rev2=1.17)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoXTPackages)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoXTPackages?template=oopsmore&param1=1.20&param2=1.20)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoXTPackages?template=oopsmore&param1=1.20&param2=1.20)
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
Stratego/XT Packages {#strategoxt-packages .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The Stratego/XT distribution consists of the following packages:

[]{#Stratego_XT} Stratego/XT
----------------------------

### []{#Core_Stratego_packages} Core Stratego packages

-   [stratego-front](StrategoFront){.twikiLink} \-- Stratego syntax and
    support for concrete object syntax
-   [srts](StrategoRunTimeSystem){.twikiLink} \-- Stratego run-time
    system
-   [strc](StrategoCompiler){.twikiLink} \-- Stratego compiler
-   stratego-lib \-- Stratego Standard Library

### []{#Tools_for_languages} Tools for languages

-   [GPP](../Tools/GenericPrettyPrinter){.twikiLink} \-- Pretty-printing
    tools based on the [BoxLanguage](../Tools/BoxLanguage){.twikiLink}
-   [aterm-tools](../Tools/ATermTools){.twikiLink} \-- Generic term
    operations
-   [asfix-tools](../Tools/AsFixTools){.twikiLink} \-- Operations on
    concrete syntax trees
-   [c-tools](CTools){.twikiLink} \-- Support for the generation of
    [C](../Transform/CProgrammingLanguage){.twikiLink} code
-   [xml-front](../Tools/XmlFront){.twikiLink} \-- Support for the
    generation and transformation of XML
-   [sdf-front](../Tools/SdfFront){.twikiLink} \--
    [SDF](SDF){.twikiLink} syntax definition, pretty printing, abstract
    syntax and (de)sugaring.
-   [sdf-tools](../Tools/SdfTools){.twikiLink} \-- Transformations on
    syntax definitions

### []{#Composition_and_package_tools} Composition and package tools

-   [autoxt](AutoXT){.twikiLink} \-- autoconf/make support for packages
    using XT
-   [xtc](XTC){.twikiLink} \-- Transformation tool composition
    (component model)

[]{#Stratego_XT_Utils} Stratego/XT Utils
----------------------------------------

-   [graph-tools](../Tools/GraphTools){.twikiLink}
-   [dot-tools[^?^](http://www.program-transformation.org/edit/Stratego/DotTools?topicparent=Stratego.StrategoXTPackages)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- Support for processing
    [DotLanguage](../Transform/DotLanguage){.twikiLink} graph
    representations
-   [stratego-tools](StrategoTools){.twikiLink} \-- Generation of
    Stratego code
-   boxenv \--
    [LaTeX[^?^](http://www.program-transformation.org/edit/Stratego/LaTeX?topicparent=Stratego.StrategoXTPackages)]{.twikiNewLink
    style="background : #FFFFCE;"} run-time system for Box
-   [stratego-util[^?^](http://www.program-transformation.org/edit/Stratego/StrategoUtil?topicparent=Stratego.StrategoXTPackages)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- utilities for a Stratego
    development environment.

[]{#Stratego_XT_Extensions} Stratego/XT Extensions
--------------------------------------------------

See [Extensions](AdditionalPackageDownload){.twikiLink}

[]{#See_also} See also
----------------------

-   [Stratego Applications](StrategoApplication){.twikiLink} for
    applications of Stratego (as opposed to packages that support the
    development of applications).

<!-- -->

-   [Reference Card](ReferenceCard){.twikiLink} with a data-flow diagram
    of the most important tools in [StrategoXT](StrategoXT){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
