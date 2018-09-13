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
    Page](http://www.program-transformation.org/edit/Stratego/PitFalls?t=1536825607)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PitFalls)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PitFalls)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PitFalls?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PitFalls?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/PitFalls?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/PitFalls?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/PitFalls?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/PitFalls?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/PitFalls?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/PitFalls?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PitFalls)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PitFalls?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/PitFalls?template=oopsmore&param1=1.4&param2=1.4)
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
Pit Falls {#pit-falls .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

From time to time you write obvious code, but after several days of
intensive debugging, you discover that it cannot possibly work.
Beginners are espacially at risk for this, because they find it
difficult to distinguish between code that fails because they made a
mistake, or because they midunderstand the language semantics.

This page is a list of such [PitFalls](PitFalls){.twikiLink}.

-   You code topdown(s) to apply the strategy s wherever possible. It
    ends up being applied nowhere. You see, topdown(s) fails as soon as
    its argument s fails. To get s applied everywhere it can be applied
    without getting stuck where cannot be, use topdown(try(s)) instead.
    The same holds for other iterators. \--
    [HendrikBoom](../Main/HendrikBoom){.twikiLink} - 02 Jul 2001\

<!-- -->

-   Please add more war stories here; otherwise this page will itself be
    one of the [PitFalls](PitFalls){.twikiLink}.

\-- [HendrikBoom](../Main/HendrikBoom){.twikiLink} - 02 Jul 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.PitFalls moved from Stratego.PittFalls on 15 May 2003 - 10:39
by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Stratego/PitFalls?newweb=Stratego&newtopic=PittFalls&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
