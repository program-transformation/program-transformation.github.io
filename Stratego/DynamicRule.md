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
    Page](http://www.program-transformation.org/edit/Stratego/DynamicRule?t=1536825576)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/DynamicRule)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/DynamicRule)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/DynamicRule?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/DynamicRule?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Stratego/DynamicRule?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/DynamicRule?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/DynamicRule?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/DynamicRule?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/DynamicRule?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/DynamicRule?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/DynamicRule)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/DynamicRule?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Stratego/DynamicRule?template=oopsmore&param1=1.6&param2=1.6)
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
Dynamic Rule {#dynamic-rule .twikiTopicTitle}
============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A dynamic rule is an ordinary [RewriteRule](RewriteRule){.twikiLink}
that is generated at run-time. A dynamic rule can inherit bindings of
variables from its generation context. Dynamic rules solve the problem
caused by the context-free nature of normal rewrite rules.

### []{#Syntax} Syntax

A set of dynamic rules is introduced by the keyword `rules` as follows

    rules(
      Lab1 : l1 -> r1 where s1 
      ... 
      Labn : ln -> rn where sn
    )

This construct itself defines a
[RewritingStrategy](RewritingStrategy){.twikiLink} that can be applied.
All variables that are *statically* bound before the `rules` construct
is invoked are inherited by the dynamic rules.

### []{#Resources} Resources

Dynamic rules are useful in many transformation problems. Several
examples of dynamic rules are presented in the paper [Scoped Dynamic
Rewrite Rules](ScopedDynamicRewriteRules){.twikiLink}.

The [dynamic rule semantics](DynamicRuleSemantics){.twikiLink} has
undergone some changes over time. Hairy issues include overlapping
left-hand sides in dynamic rules with the same label and the application
of dynamic rules to terms with annotations.

### []{#Pragmatics} Pragmatics

In order to use dynamic rules in a module it is necessary to import the
module `dynamic-rules`.

### []{#Dynamic_Rules_Rethought} Dynamic Rules Rethought

We\'re currently rethinking the concept of dynamic rules. Quite some
changes are at stake. We maintain (some of) our thoughts at [Dynamic
Rules Rethought](DynamicRulesRethought){.twikiLink}.

### []{#Related_Constructs_in_Other_Lang} Related Constructs in Other Languages

Dynamic rules are an innovation of Stratego. Some other languages have
constructs that have commonalities with dynamic rules. See [Dynamic
Rules Related](DynamicRulesRelated){.twikiLink} for a discussion.

------------------------------------------------------------------------

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 06 Dec 2001\
\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 07 May 2002\
\-- [ArthurVanDam](../Main/ArthurVanDam){.twikiLink} - 25 Mar 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
