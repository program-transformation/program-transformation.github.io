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
    Page](http://www.program-transformation.org/edit/Stratego/DesignOfTheCodeBoostTransformationSystem?t=1536825428)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/DesignOfTheCodeBoostTransformationSystem)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/DesignOfTheCodeBoostTransformationSystem)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/DesignOfTheCodeBoostTransformationSystem?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/DesignOfTheCodeBoostTransformationSystem?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/DesignOfTheCodeBoostTransformationSystem?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/DesignOfTheCodeBoostTransformationSystem?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/DesignOfTheCodeBoostTransformationSystem?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/DesignOfTheCodeBoostTransformationSystem?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/DesignOfTheCodeBoostTransformationSystem?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/DesignOfTheCodeBoostTransformationSystem)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/DesignOfTheCodeBoostTransformationSystem?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/DesignOfTheCodeBoostTransformationSystem?template=oopsmore&param1=1.3&param2=1.3)
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
O. S. Bagge, K. T. Kalleberg, M. Haveraaen and E. Visser. **Design of
the [CodeBoost](CodeBoost){.twikiLink} transformation system for
domain-specific optimisation of C++ programs.** In D. Binkley and P.
Tonella, editors, Third IEEE International Workshop on Source Code
Analysis and Manipulation (SCAM\'03), Amsterdam, September 2003. IEEE
Computer Society Press. To appear.

### []{#Abstract} Abstract

The use of a high-level, abstract coding style can greatly increase
developer productivity. For numerical software, this can result in
drastically reduced run-time performance. High-level, domain-specific
optimisations can eliminate much of the overhead caused by an abstract
coding style, but current compilers have poor support for
domain-specific optimisation.

In this paper we present [CodeBoost](CodeBoost){.twikiLink}, a
source-to-source transformation tool for domain-specific optimisation of
C++ programs. [CodeBoost](CodeBoost){.twikiLink} performs parsing,
semantic analysis and pretty-printing, and transformations can be
implemented either in the Stratego program transformation language, or
as user-defined rewrite rules embedded within the C++ program.
[CodeBoost](CodeBoost){.twikiLink} has been used with great success to
optimise numerical applications written in the Sophus high-level coding
style.

We discuss the overall design of the [CodeBoost](CodeBoost){.twikiLink}
transformation framework, and take a closer look at two important
features of [CodeBoost](CodeBoost){.twikiLink}: user-defined rules and
totem annotations. We also show briefly how
[CodeBoost](CodeBoost){.twikiLink} is used to optimise Sophus code,
resulting in applications that run twice as fast, or more.

### []{#Links} Links

-   [CodeBoost](CodeBoost){.twikiLink}
-   <http://www.codeboost.org>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
