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
    Page](http://www.program-transformation.org/edit/Stratego/SeparationOfRulesAndStrategies?t=1536825668)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SeparationOfRulesAndStrategies)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SeparationOfRulesAndStrategies)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SeparationOfRulesAndStrategies?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SeparationOfRulesAndStrategies?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/SeparationOfRulesAndStrategies?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SeparationOfRulesAndStrategies)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SeparationOfRulesAndStrategies?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/SeparationOfRulesAndStrategies?template=oopsmore&param1=1.1&param2=1.1)
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
Separation Of Rules And Strategies {#separation-of-rules-and-strategies .twikiTopicTitle}
==================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

You insist on the importance of separation of concerns, in particular in
separation between rules and strategies, so that rules become basic
strategies on top of which you build more complex transformation
strategies. However, when you introduce match and build strategies and
\"break\" the rules, these disappear completely and everything becomes
just strategies. How do you explain or justify this?

\-- Narcisco Marti Oliet

This seems indeed paradoxical, but it is not, in fact.

The \'separation of rules and strategies\' is a programming idiom that
is not the same as the \'linguistic distinction between rules and
strategies\'.

According to the principle of separation of rules and strategies, it
should be possible to define transformation rules separately from the
strategy in which they are applied. Thus, a rule

      PlusZero : Plus(x, Zero) -> x

defines a single transformation step regardless of the strategy. It can
be used in an innermost normalization of terms

      innermost(PlusZero + ...)

or in single bottomup traversal

      bottomup(try(PlusZero + ...)

To support this separation you need a language in which rules can be
defined as first-class citizens, i.e., it should be possible to combine
rules in different strategies.

In the entire discussion above we regarded a \'rule\' as a \`basic
transformation step\'. Nothing in the separation principle requires that
rules are defined in as specific way. In Stratego rules are implemented
by the atomic transformation operatations match and build. Thus, the
rule above is nothing but syntactic sugar for

      PlusZero  = ?Plus(x, Zero); !x

So, linguistically speaking, there is no distinction between rules and
strategies.

The important point is that we can distinguish rule-like entities such
as `PlusZero` from strategy-like entities such as innermost, and that
rule-like things are *first-class*.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 23 May 2002\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
