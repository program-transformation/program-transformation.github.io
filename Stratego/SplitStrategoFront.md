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
    Page](http://www.program-transformation.org/edit/Stratego/SplitStrategoFront?t=1536825670)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SplitStrategoFront)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SplitStrategoFront)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SplitStrategoFront?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SplitStrategoFront?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/SplitStrategoFront?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SplitStrategoFront)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SplitStrategoFront?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/SplitStrategoFront?template=oopsmore&param1=1.1&param2=1.1)
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
Split Stratego Front {#split-stratego-front .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The [StrategoFront](StrategoFront){.twikiLink} package contains the
[SDF](SDF){.twikiLink} syntax definition of Stratego, the signatures and
pretty-print tables generated from that syntax definition and additional
code for desugaring and meta-exploding Stratego abstract syntax trees.
The parse and pretty-print tables are needed by other packages for
building signatures. The signature generation in
[StrategoFront](StrategoFront){.twikiLink} has a circular dependency
with the stratego-tools package.

This can be solved by splitting the package into a package with only the
syntax and pretty-print tables.

This seems to be an instance of the \'[bootstrapped packages containing
generated
sources[^?^](http://www.program-transformation.org/edit/Stratego/BootstrappedPackagesContainingGeneratedSources?topicparent=Stratego.SplitStrategoFront)]{.twikiNewLink
style="background : #FFFFCE;"}\' problem.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 14 Nov 2002\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
