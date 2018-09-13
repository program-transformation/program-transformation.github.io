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
    Page](http://www.program-transformation.org/edit/Stratego/EffectsAnalysis?t=1536825578)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/EffectsAnalysis)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/EffectsAnalysis)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/EffectsAnalysis?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/EffectsAnalysis?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/EffectsAnalysis?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/EffectsAnalysis?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/EffectsAnalysis?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/EffectsAnalysis?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/EffectsAnalysis?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/EffectsAnalysis)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/EffectsAnalysis?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/EffectsAnalysis?template=oopsmore&param1=1.3&param2=1.3)
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
Effects Analysis {#effects-analysis .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Effects analysis can further enhance the optimizations performed by the
[Stratego optimizer](StrategoOptimizer){.twikiLink}. The following
questions should be answered by effects analysis:

-   Does the strategy inspect the current term?
-   Does the strategy change the current term?
-   Does the strategy have a side-effect (io, table)?
-   Does the strategy bind variables?
-   Can the strategy fail, or is it guaranteed to succeed?

If the answers to all these questions is no, then the strateg is
equivalent to the identity strategy `id`. In case some answers are no,
optimizations may still be possible.

For instance, a sequence `(t; s)` can be reduced to `s` if `s` does not
inspect the current term. A generalization of one of the [build match
fusion](BuildMatchFusion){.twikiLink} laws.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Aug 2003

------------------------------------------------------------------------

[ToDo](ToDo){.twikiLink},
[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.EffectsAnalysis)]{.twikiNewLink
style="background : #FFFFCE;"},
[StrategoOptimization](StrategoOptimization){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
