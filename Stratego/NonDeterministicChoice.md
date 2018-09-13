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
    Page](http://www.program-transformation.org/edit/Stratego/NonDeterministicChoice?t=1536825602)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/NonDeterministicChoice)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/NonDeterministicChoice)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/NonDeterministicChoice?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/NonDeterministicChoice?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/NonDeterministicChoice?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/NonDeterministicChoice)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/NonDeterministicChoice?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/NonDeterministicChoice?template=oopsmore&param1=1.1&param2=1.1)
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
Non Deterministic Choice {#non-deterministic-choice .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The non-deterministic local choice operator `s1 + s2` chooses one of the
strategies `s1` or `s2` to apply. If the one chose fails, the other one
is tried.

The `+` operator is **local** because once one of the strategies has
succeeded the choice is committed, even if the continuation of the
choice fails on the result. If backtracking to the other strategy is
desired one should used the
[GlobalChoice[^?^](http://www.program-transformation.org/edit/Stratego/GlobalChoice?topicparent=Stratego.NonDeterministicChoice)]{.twikiNewLink
style="background : #FFFFCE;"} operator `++`.

The `+` operator is **non-determinstic** sine the
[EvaluationOrder](EvaluationOrder){.twikiLink} in which the strategies
are tried is **not defined**. The
[StrategoCompiler](StrategoCompiler){.twikiLink} is free to choose an
order. If complete control over the evaluation order is needed one
should use the [DeterministicChoice](DeterministicChoice){.twikiLink}
operator `<-`.

In Stratego it is permitted to define several
[RewriteRules](RewriteRule){.twikiLink} with the same label. This
interpreted as the composition with `+` of the rules.

It would be useful to
[DetectOverlappingRules](DetectOverlappingRules){.twikiLink} in a
non-deterministic choice.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Mar 2002\

------------------------------------------------------------------------

[CategoryGlossary](CategoryGlossary){.twikiLink} \|
[StrategoGlossary](StrategoGlossary){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
