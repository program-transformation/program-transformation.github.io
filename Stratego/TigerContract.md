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
    Page](http://www.program-transformation.org/edit/Stratego/TigerContract?t=1536825714)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/TigerContract)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/TigerContract)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/TigerContract?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/TigerContract?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/TigerContract?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/TigerContract?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/TigerContract?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/TigerContract?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/TigerContract?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/TigerContract)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/TigerContract?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/TigerContract?template=oopsmore&param1=1.3&param2=1.3)
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
Tiger Contract {#tiger-contract .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](TigerContract#Introduction)
-   [Resources](TigerContract#Resources)
-   [Download and installation](TigerContract#Download_and_installation)
    -   [Configuration](TigerContract#Configuration)
-   [Known Bugs](TigerContract#Known_Bugs)
-   [TODO](TigerContract#TODO)
:::

[]{#Introduction} Introduction
------------------------------

[TigerContract](TigerContract){.twikiLink} is an experimental package
which implements a [TigerCompiler](../Tiger/TigerCompiler){.twikiLink}
with contract support. The main purpose is to understand what contracts
are and how to implements the checking and enforcing of these contracts
in Stratego.

First target is to implement support structural contracts for rewriting
(compiler) components. A next step may be to implement semantic
contracts; but this support will be limited, probably by implementing
your own checker component.

[]{#Resources} Resources
------------------------

-   [tiger](../Tiger/WebHome){.twikiLink} : Tiger in Stratego
-   [stratego-regular](StrategoRegular){.twikiLink} : Optional Stratego
    library providing Regular Hedge/Tree Grammar support
-   [XTC](XTC){.twikiLink} : Transformation Tool Composition

[]{#Download_and_installation} Download and installation
--------------------------------------------------------

The current source of [TigerContract](TigerContract){.twikiLink} can be
checked out using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/trunk/experimental/tiger-contract

There will never be a distribution, since contract support will
eventually be implemented in a new version of the [XTC](XTC){.twikiLink}
library as part of my thesis work. Thus, making this package obsolete.

### []{#Configuration} Configuration

Configure the package:

-   `--with-xt` or if the packages are installed at different locations:
    -   `--with-aterm`
    -   `--with-sdf`
    -   `--with-strategoxt`
-   `--with-tiger`

[]{#Known_Bugs} Known Bugs
--------------------------

List of Bugs will hopefully never appear here

[]{#TODO} TODO
--------------

-   Contract support
    -   Extend the existing
        [TigerCompiler](../Tiger/TigerCompiler){.twikiLink}
        (tiger/xtc/tigerc.str) to support the notion of contracts - done
-   Refactor to library for contract support
    -   Create helper library for contract support - done
    -   Incorporate this library into thesis project
-   Use the new [XTC](XTC){.twikiLink} library (with contract support)
    to add contracts to other packages like [XWeb](XWeb){.twikiLink}

\-- [NielsJanssen](../Main/NielsJanssen){.twikiLink} - 11 Dec 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
