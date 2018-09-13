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
    Page](http://www.program-transformation.org/edit/Stratego/AvoidRunTimeChecksOnVariables?t=1536825564)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/AvoidRunTimeChecksOnVariables)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/AvoidRunTimeChecksOnVariables)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/AvoidRunTimeChecksOnVariables?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/AvoidRunTimeChecksOnVariables?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/AvoidRunTimeChecksOnVariables?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/AvoidRunTimeChecksOnVariables?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/AvoidRunTimeChecksOnVariables?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/AvoidRunTimeChecksOnVariables)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/AvoidRunTimeChecksOnVariables?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/AvoidRunTimeChecksOnVariables?template=oopsmore&param1=1.2&param2=1.2)
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
Avoid Run Time Checks On Variables {#avoid-run-time-checks-on-variables .twikiTopicTitle}
==================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The binding of a term variable does not coincide with its binding. That
is, in the strategy expresssion

      {x : ... ; ?Foo(x) ; ... ; !Bar(x) }

the variable `x` is first introduced in a new scope, some time later it
is bound in a match, and at the end its binding is used in a build.

This entails that a variable is not necessarily bound when it is used in
a build. Furthermore, a variable may be matched twice. The second match
only succeeds if it is against the same term that it was bound to the
first time.

For these reasons the [Stratego Compiler](StrategoCompiler){.twikiLink}
generates run-time checks on variable matches and builds. Often these
checks are superfluous since the variable is sure to be bound or unbound
at a certain position in the program. An optimization that avoids these
checks allows the compiler to generate simpler code, which may also be
better amenable to optimization by the C compiler.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 11 Jul 2003

The optimization is now included in the compiler and will be available
in [StrategoRelease093](StrategoRelease093){.twikiLink}.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Jul 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
