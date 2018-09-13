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
    Page](http://www.program-transformation.org/edit/Stratego/InnermostFusion?t=1536825589)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/InnermostFusion)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/InnermostFusion)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/InnermostFusion?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/InnermostFusion?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/InnermostFusion?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/InnermostFusion?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/InnermostFusion?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/InnermostFusion)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/InnermostFusion?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/InnermostFusion?template=oopsmore&param1=1.2&param2=1.2)
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
Innermost Fusion {#innermost-fusion .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

An experimental fusion transformation for fusing the generic
[InnermostStrategy[^?^](http://www.program-transformation.org/edit/Stratego/InnermostStrategy?topicparent=Stratego.InnermostFusion)]{.twikiNewLink
style="background : #FFFFCE;"} with the rules it is instantiated with
was implemented in [StrategoRelease05](StrategoRelease05){.twikiLink}.
The transformation is described in the paper \'[Fusing Logic and
Control](FusingLogicAndControl){.twikiLink}\'.

The transformation is not as useful after
[StrategoRelease06](StrategoRelease06){.twikiLink}, since
[InliningDefinitions[^?^](http://www.program-transformation.org/edit/Stratego/InliningDefinitions?topicparent=Stratego.InnermostFusion)]{.twikiNewLink
style="background : #FFFFCE;"} has been reduced. To get a better result
out of the transformation, the inlining heuristics need to be improved.
Probably it is a good idea to move the inliner from the front-end to the
optimizer.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Dec 2001\

The fusion transformation is fully integrated in the compiler since
[StrategoRelease08](StrategoRelease08){.twikiLink} using its own
inliner. The transformation is routinely used in the compiler itself and
produces very fast simplifiers. The optimization works best for
unconditional rules or rules with a condition not contributing to the
right-hand side.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Aug 2003

------------------------------------------------------------------------

[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.InnermostFusion)]{.twikiNewLink
style="background : #FFFFCE;"} \| [ToDo](ToDo){.twikiLink} \|
[StrategoOptimization](StrategoOptimization){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
