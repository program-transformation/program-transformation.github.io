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
    Page](http://www.program-transformation.org/edit/Stratego/HsOpt?t=1536825467)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/HsOpt)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/HsOpt)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/HsOpt?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/HsOpt?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/HsOpt?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/HsOpt?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/HsOpt?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/HsOpt?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/HsOpt?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/HsOpt)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/HsOpt?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/HsOpt?template=oopsmore&param1=1.3&param2=1.3)
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
Hs Opt {#hs-opt .twikiTopicTitle}
======

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[HsOpt](HsOpt){.twikiLink} is an optimizer for the Helium compiler
implemented in the transformation language Stratego.
[Helium](http://www.cs.uu.nl/~afie/helium/) is a subset of Haskell
developed at Utrecht University. The optimizer works on the code
produced by the Helium front-end, which is code for Daan Leijen\'s Lazy
Virtual Machine (LVM). The goal of this project is to validate the
paradigm of transformation strategies for the implementation of an
optimizing compiler.

Alan van Dam has written the first version of the optimizer consisting
of a basic simplifier in the style of the GHC. The main target of this
simplifier has been the optimization of pattern matching code. The naive
translation of pattern matching by the Helium front-end keeps it simple,
but produces rather ugly code. Using a small set of transformation rules
and an appropriate strategy the code can be reduced to more sane code,
often similar to code that would be written by hand. This first
simplification step produces an optimization of about 10%.

Plans for the near future are to include an inliner (currently only
local let bindings are inlined, not global function definitions), and to
incorporate the earlier work on deforestation.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 05 May 2003

Alan\'s master thesis is now available: [Simplifying the
Simplifier](SimplifyingTheSimplifier){.twikiLink}

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Jul 2003

------------------------------------------------------------------------

[StrategoApplication](StrategoApplication){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
