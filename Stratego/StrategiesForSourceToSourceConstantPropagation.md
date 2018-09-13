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
    Page](http://www.program-transformation.org/edit/Stratego/StrategiesForSourceToSourceConstantPropagation?t=1536825428)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategiesForSourceToSourceConstantPropagation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategiesForSourceToSourceConstantPropagation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategiesForSourceToSourceConstantPropagation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategiesForSourceToSourceConstantPropagation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/StrategiesForSourceToSourceConstantPropagation?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/StrategiesForSourceToSourceConstantPropagation?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/StrategiesForSourceToSourceConstantPropagation?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/StrategiesForSourceToSourceConstantPropagation?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategiesForSourceToSourceConstantPropagation?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategiesForSourceToSourceConstantPropagation?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategiesForSourceToSourceConstantPropagation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategiesForSourceToSourceConstantPropagation?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategiesForSourceToSourceConstantPropagation?template=oopsmore&param1=1.4&param2=1.4)
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
Strategies For Source To Source Constant Propagation {#strategies-for-source-to-source-constant-propagation .twikiTopicTitle}
====================================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

K. Olmos and E. Visser. Strategies for Source-to-Source Constant
Propagation. In B. Gramlich and S. Lucas (editors) *Second International
Workshop on Reduction Strategies in Rewriting and Programming(WRS\'02).*
Electronic Notes in Theoretical Computer Science vol. 70 No. 6. Elsevier
Science Publishers, Copenhagen, Denmark. July 2002. URL:
<http://www.elsevier.nl/locate/entcs/volume70.html>

**Abstract**

Data-flow optimizations are usually implemented on low-level
intermediate representations. This is not appropriate for
source-to-source optimizations, which reconstruct a source level program
after transformation. In this paper we show how constant propagation, a
well known data-flow optimization problem, can be implemented on
abstract syntax trees in Stratego, a rewriting system extended with
programmable rewriting strategies for the control over the application
of rules and dynamic rewrite rules for the propagation of information.

**Technical report**

-   <http://www.cs.uu.nl/~visser/ftp/OV02.pdf>

**Resources**

-   [Stratego](WebHome){.twikiLink}
-   [Tiger in Stratego](../Tiger/WebHome){.twikiLink}
-   [Constant propagation](ConstantPropagation){.twikiLink}

**BibTeX**

    @InProceedings{OV02,
      author =    {Karina Olmos and Eelco Visser},
      title = {Strategies for Source-to-Source Constant Propagation},
      booktitle = {Workshop on Reduction Strategies (WRS'02)},
      pages = 20,
      year = 2002,
      editor =  {B. Gramlich and S. Lucas},
      volume =  70,
      number =  6,
      series =  {Electronic Notes in Theoretical Computer Science},
      address = {Copenhagen, Denmark},
      month = {July},
      publisher = {Elsevier Science Publishers},
      note = {\url{http://www.elsevier.nl/locate/entcs/volume70.html}}
    }

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
