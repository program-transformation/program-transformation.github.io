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
    Page](http://www.program-transformation.org/edit/Stratego/ContinuousDistribution?t=1536825573)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ContinuousDistribution)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ContinuousDistribution)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ContinuousDistribution?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ContinuousDistribution?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    24](http://www.program-transformation.org/view/Stratego/ContinuousDistribution?rev=1.24)
    [(diff 23)](http://www.program-transformation.org/rdiff/Stratego/ContinuousDistribution?rev1=1.24&rev2=1.23)
-   [Rev
    23](http://www.program-transformation.org/view/Stratego/ContinuousDistribution?rev=1.23)
    [(diff 22)](http://www.program-transformation.org/rdiff/Stratego/ContinuousDistribution?rev1=1.23&rev2=1.22)
-   [Rev
    22](http://www.program-transformation.org/view/Stratego/ContinuousDistribution?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Stratego/ContinuousDistribution?rev1=1.22&rev2=1.21)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ContinuousDistribution)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ContinuousDistribution?template=oopsmore&param1=1.24&param2=1.24)
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
    \...](http://www.program-transformation.org/oops/Stratego/ContinuousDistribution?template=oopsmore&param1=1.24&param2=1.24)
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
Continuous Distribution {#continuous-distribution .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

------------------------------------------------------------------------

[Note that Stratego is now part of the [Spoofax Language
Workbench](http://metaborg.org/spoofax), which provides an Eclipse
plugin for developing SDF and Stratego, and creating Eclipse IDE plugins
for your own language. See the Spoofax website for information and
downloads: <http://metaborg.org>. This website is still available for
historical purposes. Refer the new site for up-to-date documentation.
]{style="color:red;font-size:24px"}

------------------------------------------------------------------------

The [buildfarm](http://releases.strategoxt.org) continuously builds
Stratego/XT and related packages. The distributions contain the latest
of the latest developments. Although the distributions are thoroughly
tested by the buildfarm, such an installation is not guaranteed to be
stable.

Continuous builds are available at:

-   <http://hydra.nixos.org/job/strategoxt/strategoxt-packages/strategoxt>

To get strategoxt and the dependencies using nix, please use the
follwoing commands:

     nix-channel --add http://hydra.nixos.org/jobset/strategoxt/strategoxt-packages/channel/latest
     nix-channel --update
     nix-env -i aterm-2.5 sdf2-bundle strategoxt

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.ContinuousDistribution moved from Stratego.DailyDistribution
on 10 Nov 2004 - 17:31 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Stratego/ContinuousDistribution?newweb=Stratego&newtopic=DailyDistribution&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
