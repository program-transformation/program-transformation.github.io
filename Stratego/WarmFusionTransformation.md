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
    Page](http://www.program-transformation.org/edit/Stratego/WarmFusionTransformation?t=1536825562)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/WarmFusionTransformation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/WarmFusionTransformation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/WarmFusionTransformation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/WarmFusionTransformation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/WarmFusionTransformation?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/WarmFusionTransformation?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/WarmFusionTransformation?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/WarmFusionTransformation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/WarmFusionTransformation?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/WarmFusionTransformation?template=oopsmore&param1=1.2&param2=1.2)
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
Warm Fusion Transformation {#warm-fusion-transformation .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Warm fusion is a program transformation technique for deforesting
functional programs developed by John Launchbury and Tim Sheard. Warm
fusion works by the cata/build fusion rule:

       cata(f1,...,fn)(build(g)) = g f1 ... fn

Here g is a function that produces a \`virtual\` data structure that is
parameterized with data constructors. The build function
instantiantiates such a virtual data structure with actual constructors.
Since cata replaces constructors with functions, application of a cata
to a build can as well be replaced with the instantation of the virtual
data structure with those functions.

Application of warm fusion is trivial once functions use cata and build
to deal with data structures; instead of explicitly recursive functions
to destruct and construct such data structures. Since programming with
these operators is rather involved, it is nicer to derive the build/cata
forms of functions automatically. That is what the warm fusion
transformation of Launchbury and Sheard is about.

The warm fusion algorithm has been implemented in
[StrategoLanguage](StrategoLanguage){.twikiLink} by
[PatriciaJohann](PatriciaJohann){.twikiLink} and
[EelcoVisser](EelcoVisser){.twikiLink}. The implementation is described
in a journal article and a technical report
([WarmFusionInStratego](WarmFusionInStratego){.twikiLink}). The Stratego
implementation of warm fusion is distributed in the
[HSX](HSX){.twikiLink} package.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
