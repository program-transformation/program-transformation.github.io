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
    Page](http://www.program-transformation.org/edit/Stratego/ScopedDynamicRewriteRules?t=1536825425)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ScopedDynamicRewriteRules)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ScopedDynamicRewriteRules)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ScopedDynamicRewriteRules?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ScopedDynamicRewriteRules?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ScopedDynamicRewriteRules?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ScopedDynamicRewriteRules?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ScopedDynamicRewriteRules?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ScopedDynamicRewriteRules?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ScopedDynamicRewriteRules?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ScopedDynamicRewriteRules)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ScopedDynamicRewriteRules?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/ScopedDynamicRewriteRules?template=oopsmore&param1=1.3&param2=1.3)
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
[E. Visser](EelcoVisser){.twikiLink}. **Scoped dynamic rewrite rules.**
In [M. van den Brand](../Transform/MarkVanDenBrand){.twikiLink}and [R.
Verma](../Transform/RakeshVerma){.twikiLink}, editors, Rule Based
Programming (RULE\'01), volume 59/4 of *Electronic Notes in Theoretical
Computer Science*. Elsevier Science Publishers, September 2001.
([pdf](http://www.cs.uu.nl/people/visser/ftp/Vis01-rule.pdf),[psgz](http://www.cs.uu.nl/people/visser/ftp/Vis01-rule.ps.gz))

### []{#Abstract} Abstract

The applicability of term rewriting to program transformation is limited
by the lack of control over rule application and by the context-free
nature of rewrite rules. The first problem is addressed by languages
supporting user-definable rewriting strategies. This paper addresses the
second problem by extending rewriting strategies with scoped dynamic
rewrite rules. Dynamic rules are generated at run-time and can access
variables available from their definition context. Rules generated
within a rule scope are automatically retracted at the end of that
scope. The technique is illustrated by means of several program
tranformations: bound variable renaming, function inlining, and dead
function elimination.

### []{#Links} Links

-   [Dynamic rule](DynamicRule){.twikiLink}
-   [Dynamic rule semantics](DynamicRuleSemantics){.twikiLink}
-   [Dynamic rules rethought](DynamicRulesRethought){.twikiLink}
-   [Dynamic rules related](DynamicRulesRelated){.twikiLink}

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
