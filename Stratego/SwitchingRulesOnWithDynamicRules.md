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
    Page](http://www.program-transformation.org/edit/Stratego/SwitchingRulesOnWithDynamicRules?t=1536825711)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SwitchingRulesOnWithDynamicRules)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SwitchingRulesOnWithDynamicRules)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SwitchingRulesOnWithDynamicRules?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SwitchingRulesOnWithDynamicRules?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/SwitchingRulesOnWithDynamicRules?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SwitchingRulesOnWithDynamicRules)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SwitchingRulesOnWithDynamicRules?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/SwitchingRulesOnWithDynamicRules?template=oopsmore&param1=1.1&param2=1.1)
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
Switching Rules On With Dynamic Rules {#switching-rules-on-with-dynamic-rules .twikiTopicTitle}
=====================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The [dynamic rules](DynamicRule){.twikiLink} mechanism can be used to
enable a set of rules.

      TriggerRules = 
         ?Context(Bla, _);
          rules( A : ... -> ...   B : ... -> ... )

      traverse =
         rec x({| A, B : try(TriggerRules + A + B); all(x) |})

Rules `A` and `B` are only applied after a `Context(Bla,...)` has been
encountered.

This is not always appropriate. Often the applicability of rules can be
determined by the position in the tree.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} & Lennart Swart - 22
May 2002\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
