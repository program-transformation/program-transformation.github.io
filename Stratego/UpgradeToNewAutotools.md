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
    Page](http://www.program-transformation.org/edit/Stratego/UpgradeToNewAutotools?t=1536825716)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/UpgradeToNewAutotools)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/UpgradeToNewAutotools)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/UpgradeToNewAutotools?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/UpgradeToNewAutotools?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/UpgradeToNewAutotools?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/UpgradeToNewAutotools)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/UpgradeToNewAutotools?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/UpgradeToNewAutotools?template=oopsmore&param1=1.1&param2=1.1)
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
Upgrade To New Autotools {#upgrade-to-new-autotools .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Akim Demaille pointed out that the use of autoconf and automake in
Stratego and XT is antiquated, and badly needs to be updated to more
modern versions of these tools. I had already encountered this problem
when trying to build on a
[FreeBSD[^?^](http://www.program-transformation.org/edit/Stratego/FreeBSD?topicparent=Stratego.UpgradeToNewAutotools)]{.twikiNewLink
style="background : #FFFFCE;"} machine. The first fix is to renovate the
current scripts and makefiles such that they will pass through newer
versions of the autotools.

This turned out not to be such a problem. The issues were:

Automake enforces consistent usage of `= and =+`

The `AC_OUTPUT_SUBDIRS` macro used in the Autobundle macro
`AB_CONFIG_PKG` is no longer used. I found a simple fix for this problem
using google. The fix defines the old style macro in terms of the new
one, if it was not defined yet:

      ifdef([AC_OUTPUT_SUBDIRS],[],
        [AC_DEFUN([AC_OUTPUT_SUBDIRS],[subdirs=$1; _AC_OUTPUT_SUBDIRS])])

[StrategoRelease09](StrategoRelease09){.twikiLink} is generated using
autoconf 2.53 and automake 1.5

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 16 Nov 2002\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
