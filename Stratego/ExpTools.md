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
    Page](http://www.program-transformation.org/edit/Stratego/ExpTools?t=1536825579)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ExpTools)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ExpTools)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ExpTools?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ExpTools?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ExpTools?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ExpTools?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ExpTools?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ExpTools?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ExpTools?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ExpTools)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ExpTools?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/ExpTools?template=oopsmore&param1=1.3&param2=1.3)
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
Exp Tools {#exp-tools .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[exp-tools](ExpTools){.twikiLink} is a transformation tool package
containing all basic features found in a package for a more complex
language than expressions (for example
[xml-tools](../Tools/XmlTools){.twikiLink}). It contains the grammar,
some transformations and a xtc library for parsing/pretty-printing.

The original [xt-applet](XtApplet){.twikiLink} was used as a basis for
this package (NB: the grammar in [exp-tools](ExpTools){.twikiLink} works
with digits instead of identifiers)

[]{#Resources} Resources
------------------------

-   [xt-applet](XtApplet){.twikiLink} : a small package to get you
    started when creating your own packages

[]{#Download_and_installation} Download and installation
--------------------------------------------------------

The source of [exp-tools](ExpTools){.twikiLink} can be checked out
using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/trunk/experimental/exp-tools

There\'s no distribution of [exp-tools](ExpTools){.twikiLink} available
(yet).

### []{#Configuration} Configuration

Configure the package:

-   `--with-xt` or if the packages are installed at different locations:
    -   `--with-aterm`
    -   `--with-sdf`
    -   `--with-strategoxt`

\-- [NielsJanssen](../Main/NielsJanssen){.twikiLink} - 11 Nov 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
