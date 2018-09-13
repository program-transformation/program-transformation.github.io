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
    Page](http://www.program-transformation.org/edit/Stratego/HSX?t=1536825371)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/HSX)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/HSX)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/HSX?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/HSX?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/HSX?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/HSX?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/HSX?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/HSX?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/HSX?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/HSX)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/HSX?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/HSX?template=oopsmore&param1=1.3&param2=1.3)
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
HSX {#hsx .twikiTopicTitle}
===

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

**HSX: A Framework for Haskell Transformation**

**Note that this was the second Stratego project and probably not
up-to-date with modern Stratego programming practices**

[HSX](HSX){.twikiLink} is the byproduct of the work on the
implementation of the
[WarmFusionTransformation](WarmFusionTransformation){.twikiLink} in
Stratego. Apart from the warm fusion transformation itself, it contains
a whole range of standard utilities (such as simplification, variable
renaming, substitution, \...) that can be used to transform Haskell
programs.

**Limitations**

The current version only supports a subset of the complete language. The
syntax definition is complete, but does not support the offside rule.
The framework contains a very simple typechecker that is used to
distribute types over expressions; it assumes type declarations for all
functions.

**Requirements**

The framework is implemented on top of the XT bundle of transformation
tools and requires XT version 0.3 with Stratego version 0.4.17.

**Source**

-   <https://svn.strategoxt.org/repos/StrategoXT/hsx/trunk/>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
