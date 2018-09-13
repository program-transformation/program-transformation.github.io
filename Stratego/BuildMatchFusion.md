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
    Page](http://www.program-transformation.org/edit/Stratego/BuildMatchFusion?t=1536825565)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/BuildMatchFusion)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/BuildMatchFusion)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/BuildMatchFusion?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/BuildMatchFusion?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/BuildMatchFusion?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/BuildMatchFusion)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/BuildMatchFusion?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/BuildMatchFusion?template=oopsmore&param1=1.1&param2=1.1)
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
Build Match Fusion {#build-match-fusion .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The composition of a match and a build (in either order) can often be
simplified. If the match following a build is incompatible, failure is
certain. For example,

      !Foo(Bar(x), y); ?FooBar(z)

can be replaced with `fail` since the match will never succeed.

If the build and match *are* compatible (i.e., if they can be unified),
the sequence can be simplified. For example,

      !Foo(Bar(x), y); ?Foo(z1, z2); ...

can be replaced with

      !Bar(x); ?z1; !y; ?z2; !Foo(Bar(x), y); ...

Subsequent transformations can get rid of the construction of the entire
term, if it is not needed.

These ideas are implemented by simple rewrite rules in module

-   [build-match-laws](https://svn.strategoxt.org/repos/StrategoXT/trunk/StrategoXT/sc/spec/opt/build-match-laws.str)

The rules are applied by the [Stratego
simplifier](StrategoSimplifier){.twikiLink}. Often these rules are
triggered by inlining (which brings matches and builds together). The
results are simplified by [constant and copy
propagation](ConstantAndCopyPropagation){.twikiLink} and [dead variable
elimination](DeadVariableElimination){.twikiLink}.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 18 Aug 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
