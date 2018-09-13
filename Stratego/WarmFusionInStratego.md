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
    Page](http://www.program-transformation.org/edit/Stratego/WarmFusionInStratego?t=1536825427)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/WarmFusionInStratego)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/WarmFusionInStratego)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/WarmFusionInStratego?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/WarmFusionInStratego?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/WarmFusionInStratego?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/WarmFusionInStratego?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/WarmFusionInStratego?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/WarmFusionInStratego?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/WarmFusionInStratego?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/WarmFusionInStratego)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/WarmFusionInStratego?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/WarmFusionInStratego?template=oopsmore&param1=1.3&param2=1.3)
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
Warm Fusion In Stratego {#warm-fusion-in-stratego .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[PatriciaJohann](PatriciaJohann){.twikiLink} and
[EelcoVisser](EelcoVisser){.twikiLink}. Warm fusion in Stratego: A case
study in the generation of program transformation systems. *Annals of
Mathematics and Artificial Intelligence*, **29**(1\--4):1\--34, 2000.

The technical report version of the paper contains the complete Stratego
specification of the implementation

-   <http://www.cs.uu.nl/~visser/ftp/JV2000-TR.ps.gz>
-   <http://www.cs.uu.nl/~visser/ftp/JV2000-TR.ps.zip>

**Abstract**

Stratego is a domain-specific language for the specification of program
transformation systems. The design of Stratego is based on the paradigm
of rewriting strategies: user-definable programs in a little language of
strategy operators determine where and in what order transformation
rules are (automatically) applied to a program. The separation of rules
and strategies supports modularity of specifications. Stratego also
provides generic features for specification of program traversals.

In this paper we present a case study of Stratego as applied to a
non-trivial problem in program transformation. We demonstrate the use of
Stratego in eliminating intermediate data structures from (also known as
\'deforesting\') functional programs via the \'warm fusion\' algorithm
of Launchbury and Sheard. This algorithm has been specified in Stratego
and embedded in a fully automatic transformation system for kernel
Haskell. The entire system consists of about 2600 lines of specification
code, which breaks down into 1850 lines for a general framework for
Haskell transformation and 750 lines devoted to a highly modular, easily
extensible specification of the warm fusion transformer itself. Its
successful design and construction provides further evidence that
programs generated from Stratego specifications are suitable for
integration into real systems, and that rewriting strategies are a good
paradigm for the implementation of such systems.

**See Also**

-   [WarmFusionTransformation](WarmFusionTransformation){.twikiLink}
-   [HSX](HSX){.twikiLink}: a Haskell Transformation Framework

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink} \|
[StrategoPublications](StrategoPublications){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
