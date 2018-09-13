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
    Page](http://www.program-transformation.org/edit/Stratego/StrategyRule?t=1536825558)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategyRule)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategyRule)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategyRule?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategyRule?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategyRule?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategyRule?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategyRule?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategyRule)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategyRule?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategyRule?template=oopsmore&param1=1.2&param2=1.2)
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
Strategy Rule {#strategy-rule .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A [StrategyRule](StrategyRule){.twikiLink} of the form

      Lab :: s1 --> s2 where s3

is syntactic sugar for a
[StrategyDefinition](StrategyDefinition){.twikiLink} of the form

      Lab = s1; where(s3); s2

------------------------------------------------------------------------

[StrategoRelease06](StrategoRelease06){.twikiLink} introduced a bug in
the translation of strategy rules. The condition of a rule should be
wrapped in a Where. In normal rules that perform a build it can be left
out, but in \`strategy rules\' (:: \--\>) that might do a congruence,
this is essential. Bug report by Hedzer Westra. The bug is solved in
[StrategoRelease064](StrategoRelease064){.twikiLink}.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 03 Jan 2002\

------------------------------------------------------------------------

[CategorySolvedBugs[^?^](http://www.program-transformation.org/edit/Stratego/CategorySolvedBugs?topicparent=Stratego.StrategyRule)]{.twikiNewLink
style="background : #FFFFCE;"}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.StrategyRule moved from Stratego.StrategyRuleTranslation on 03
Jan 2002 - 21:36 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Stratego/StrategyRule?newweb=Stratego&newtopic=StrategyRuleTranslation&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
