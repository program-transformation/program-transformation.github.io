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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoSimplifier?t=1536825682)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoSimplifier)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoSimplifier)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoSimplifier?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoSimplifier?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoSimplifier?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoSimplifier)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoSimplifier?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoSimplifier?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego Simplifier {#stratego-simplifier .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The Stratego simplifier is applied at several times by the [Stratego
optimizer](StrategoOptimizer){.twikiLink}. The simplifier reduces
strategy expressions by means of a large number of simple rewrite rules
using innermost rewriting.

Simplifier

-   [simplify1](https://svn.strategoxt.org/repos/StrategoXT/trunk/StrategoXT/sc/spec/opt/simplify1.str)

Rules

-   [stratego-laws](https://svn.strategoxt.org/repos/StrategoXT/trunk/StrategoXT/sc/spec/opt/stratego-laws.str)
-   [idfail-laws](https://svn.strategoxt.org/repos/StrategoXT/trunk/StrategoXT/sc/spec/opt/idfail-laws.str)
-   [congruence-laws](https://svn.strategoxt.org/repos/StrategoXT/trunk/StrategoXT/sc/spec/opt/congruence-laws.str)
-   [build-match-laws](https://svn.strategoxt.org/repos/StrategoXT/trunk/StrategoXT/sc/spec/opt/build-match-laws.str)
-   [traversal-laws](https://svn.strategoxt.org/repos/StrategoXT/trunk/StrategoXT/sc/spec/opt/traversal-laws.str)
-   [bind-laws](https://svn.strategoxt.org/repos/StrategoXT/trunk/StrategoXT/sc/spec/opt/bind-laws.str)
-   [scope-laws](https://svn.strategoxt.org/repos/StrategoXT/trunk/StrategoXT/sc/spec/opt/scope-laws.str)

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 18 Aug 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
