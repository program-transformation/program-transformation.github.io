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
    Page](http://www.program-transformation.org/edit/Stratego/EvaluationOrder?t=1536825579)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/EvaluationOrder)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/EvaluationOrder)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/EvaluationOrder?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/EvaluationOrder?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/EvaluationOrder?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/EvaluationOrder?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/EvaluationOrder?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/EvaluationOrder)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/EvaluationOrder?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/EvaluationOrder?template=oopsmore&param1=1.2&param2=1.2)
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
Evaluation Order {#evaluation-order .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The evaluation order of the alternatives of the
[NonDeterministicChoice](NonDeterministicChoice){.twikiLink} operator
`+` is **undefined**.

------------------------------------------------------------------------

Improved efficiency of needed definition extraction by using dynamic
rules instead of a list of definitions to look up definitions in. The
effect of this change is that the order of evaluation of definitions for
the same label is reversed. This is fine since the order of evaluation
of rules/definitions with the same name is undefined, but it might break
some specifications. It might be a good idea to change the evaluation
order with every distribution in order to force programmers to use left
choice when the order is relevant.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Dec 2001\

To assist users in detecting problems it would be useful to
[DetectOverlappingRules](DetectOverlappingRules){.twikiLink} in the
alternatives of a
[NonDeterministicChoice](NonDeterministicChoice){.twikiLink}.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Mar 2002

------------------------------------------------------------------------

[CategoryGlossary](CategoryGlossary){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
