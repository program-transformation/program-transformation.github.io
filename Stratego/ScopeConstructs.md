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
    Page](http://www.program-transformation.org/edit/Stratego/ScopeConstructs?t=1536825666)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ScopeConstructs)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ScopeConstructs)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ScopeConstructs?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ScopeConstructs?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ScopeConstructs?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ScopeConstructs)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ScopeConstructs?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/ScopeConstructs?template=oopsmore&param1=1.1&param2=1.1)
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
Scope Constructs {#scope-constructs .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Stratego provides scope constructs for several types of data.

The [term variable
scope[^?^](http://www.program-transformation.org/edit/Stratego/TermVariableScope?topicparent=Stratego.ScopeConstructs)]{.twikiNewLink
style="background : #FFFFCE;"} `{x1,...,xn:s}` delimits the scope of
bindings to the term variables `xi` to the strategy `s`. That is, at the
start of the scope fresh, unbound variables are allocated, and after the
scope ends, the variables are removed and any old variables with the
same name are restored. The binding of term variables by a match does
not have to coincide with the scope.

The [dynamic rule
scope[^?^](http://www.program-transformation.org/edit/Stratego/DynamicRuleScope?topicparent=Stratego.ScopeConstructs)]{.twikiNewLink
style="background : #FFFFCE;"} `{|L:s|}` delimits the scope of dynamic
rules with label `L` to the strategy `s`. Any rule generated during the
execution of `s` is removed after the scope ends, and any old rules are
restored.

The [anonymous file
scope[^?^](http://www.program-transformation.org/edit/Stratego/AnonymousFileScope?topicparent=Stratego.ScopeConstructs)]{.twikiNewLink
style="background : #FFFFCE;"} `xtc-temp-files(s)` is used in
[XTC](XTC){.twikiLink} to manage the intermediate files that are used to
store the terms exchanged by transformation tools. It mainly keeps track
of which anonymous files are generated, and makes sure these are removed
when exiting the scope.

Can the notion of scope be generalized and made into a first-class
construct in the language?

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 14 Jun 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
