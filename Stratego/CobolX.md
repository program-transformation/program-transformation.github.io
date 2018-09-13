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
    Page](http://www.program-transformation.org/edit/Stratego/CobolX?t=1536825370)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/CobolX)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/CobolX)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/CobolX?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/CobolX?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Stratego/CobolX?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/CobolX?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/CobolX?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/CobolX?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/CobolX?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/CobolX?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/CobolX)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/CobolX?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Stratego/CobolX?template=oopsmore&param1=1.6&param2=1.6)
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
Cobol X {#cobol-x .twikiTopicTitle}
=======

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

**Homepage:** <http://losser.st-lab.cs.uu.nl/~pretzel/>

[CobolX](CobolX){.twikiLink} is a transformation system for
[COBOL](../Transform/COBOL){.twikiLink} developed by
[HedzerWestra](../Main/HedzerWestra){.twikiLink} based on
[StrategoLanguage](StrategoLanguage){.twikiLink} and the Tools.XT tool
set.

The project is done in collaboration with the
[SoftwareImprovementGroup](../Transform/SoftwareImprovementGroup){.twikiLink}.

[CobolX](CobolX){.twikiLink} is split up into a number of small
components:

-   [CobolGrammar[^?^](http://www.program-transformation.org/edit/Stratego/CobolGrammar?topicparent=Stratego.CobolX)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [LanguageX[^?^](http://www.program-transformation.org/edit/Stratego/LanguageX?topicparent=Stratego.CobolX)]{.twikiNewLink
    style="background : #FFFFCE;"}: generation of PP tables and Stratego
    signatures
-   [RuleX[^?^](http://www.program-transformation.org/edit/Stratego/RuleX?topicparent=Stratego.CobolX)]{.twikiNewLink
    style="background : #FFFFCE;"}: flexible and easy to adapt, extend
    and use transformation building system
-   [LayoutPreservationSystem[^?^](http://www.program-transformation.org/edit/Stratego/LayoutPreservationSystem?topicparent=Stratego.CobolX)]{.twikiNewLink
    style="background : #FFFFCE;"}: enabling transformations with
    Stratego while preserving layout
-   cobolX: generating reports about transformed files

With this system, two applications have been built:

-   [CobolX](CobolX){.twikiLink}-goto
-   [CobolX](CobolX){.twikiLink}-trafo

links:

-   <http://losser.st-lab.cs.uu.nl/~pretzel/dbs/>
-   <http://losser.st-lab.cs.uu.nl/~pretzel/releases/>
-   <http://losser.st-lab.cs.uu.nl/~pretzel/docs/>
-   Tools.XT
-   [GrammarBase](../Sdf/GrammarBase){.twikiLink}
-   [GrammarTools](../Tools/GrammarTools){.twikiLink}
-   <http://www.cs.uu.nl/~visser/>
-   <http://www.stratego-language.org>
-   <http://www.cwi.nl>
-   <http://www.software-improvers.com>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
