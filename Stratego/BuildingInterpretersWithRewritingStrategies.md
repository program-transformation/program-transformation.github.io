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
    Page](http://www.program-transformation.org/edit/Stratego/BuildingInterpretersWithRewritingStrategies?t=1536825430)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/BuildingInterpretersWithRewritingStrategies)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/BuildingInterpretersWithRewritingStrategies)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/BuildingInterpretersWithRewritingStrategies?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/BuildingInterpretersWithRewritingStrategies?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/BuildingInterpretersWithRewritingStrategies?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/BuildingInterpretersWithRewritingStrategies?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/BuildingInterpretersWithRewritingStrategies?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/BuildingInterpretersWithRewritingStrategies?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/BuildingInterpretersWithRewritingStrategies?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/BuildingInterpretersWithRewritingStrategies)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/BuildingInterpretersWithRewritingStrategies?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/BuildingInterpretersWithRewritingStrategies?template=oopsmore&param1=1.3&param2=1.3)
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
Building Interpreters With Rewriting Strategies {#building-interpreters-with-rewriting-strategies .twikiTopicTitle}
===============================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[EelcoDolstra](../Main/EelcoDolstra){.twikiLink} and
[EelcoVisser](../Main/EelcoVisser){.twikiLink}. Building Interpreters
With Rewriting Strategies In
[MarkVanDenBrand](../Transform/MarkVanDenBrand){.twikiLink} and
[RalfLaemmel](../Transform/RalfLaemmel){.twikiLink} (editors) *Workshop
on Language Descriptions, Tools and Applications
([LDTA](../Transform/LDTA){.twikiLink}\'02).* volume 65.3 of *Electronic
Notes in Theoretical Computer Science.* Elsevier Science Publishers,
April 2002. (To appear)

**Abstract**

Programming language semantics based on pure rewrite rules suffers from
the gap between rewriting strategy implemented in rewriting engines and
the intended evaluation strategy. This paper shows how programmable
rewriting strategies can be used to implement interpreters for
programming languages based on rewrite rules. The advantage of this
approach is that reduction rules are first class entities that can be
reused in different strategies, even in other kinds of program
transformations such as optimizers. The approach is illustrated with
several interpreters for the lambda calculus based on implicit and
explicit (parallel) substitution, different strategies including
normalization, eager evaluation, lazy evaluation, and lazy evaluation
with updates. An extension with pattern matching and choice shows that
such interpreters can easily be extended.

**Preprint**

-   <http://www.cs.uu.nl/people/visser/ftp/DV02.pdf>

**Related**

-   [RhoStratego](RhoStratego){.twikiLink}

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
