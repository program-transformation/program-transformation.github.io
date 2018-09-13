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
    Page](http://www.program-transformation.org/edit/Stratego/FusionOfStrategoAndXT?t=1536825556)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/FusionOfStrategoAndXT)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/FusionOfStrategoAndXT)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/FusionOfStrategoAndXT?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/FusionOfStrategoAndXT?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/FusionOfStrategoAndXT?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/FusionOfStrategoAndXT?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/FusionOfStrategoAndXT?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/FusionOfStrategoAndXT)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/FusionOfStrategoAndXT?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/FusionOfStrategoAndXT?template=oopsmore&param1=1.2&param2=1.2)
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
Fusion Of Stratego And XT {#fusion-of-stratego-and-xt .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

In [StrategoRelease08](StrategoRelease08){.twikiLink} an extension of
Stratego with [concrete syntax](ConcreteSyntax){.twikiLink} is provided.
This extension requires a tighter integration with
[SDF](SDF){.twikiLink} and several of the XT tools. In effect, this has
resulted in the dependency of Stratego on a large part of the XT
packages. Therefore, a Stratego distribution can no longer be built
without these packages.

Starting with [StrategoRelease09](StrategoRelease09){.twikiLink}, the
Stratego and XT source trees (and CVS repositories) have been merged
into [StrategoXT](StrategoXT){.twikiLink}.

The distribution of the [ATermLibrary](ATermLibrary){.twikiLink} and the
[SDF](SDF){.twikiLink} tools (parser generator and sglr) have been
factored out of the [StrategoXT](StrategoXT){.twikiLink} distribution,
because (1) these packages are produced by the CWI group, (2) the
development is independent, (3) the functionality of
[ATermLibrary](ATermLibrary){.twikiLink} and [SDF](SDF){.twikiLink} is
quite stable from the perspective of Stratego, i.e., not every Stratego
distribution needs a new ATerm and [SDF](SDF){.twikiLink} distribution.

A first beta release ([StrategoXT](StrategoXT){.twikiLink}-0.9beta1) is
available from

<http://www.stratego-language.org/Stratego/StrategoRelease09>

along with distributions of the [ATermLibrary](ATermLibrary){.twikiLink}
and [SDF](SDF){.twikiLink}.

The integration of Stratego and XT was also needed because development
was stagnating. Now the combined CVS repository is available to all
Stratego developers, so badly needed improvements and extensions of XT
packages can be undertaken.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 14 Nov 2002\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
