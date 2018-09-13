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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoFrontEnd?t=1536825675)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoFrontEnd)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoFrontEnd)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoFrontEnd?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoFrontEnd?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoFrontEnd?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoFrontEnd)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoFrontEnd?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoFrontEnd?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego Front End {#stratego-front-end .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The front-end of the [Stratego compiler](StrategoCompiler){.twikiLink}
parses the source modules, performs several checks on them, integrates
multiple definitions, and produces a
[CoreStratego[^?^](http://www.program-transformation.org/edit/Stratego/CoreStratego?topicparent=Stratego.StrategoFrontEnd)]{.twikiNewLink
style="background : #FFFFCE;"} program for further processing by the
[Stratego optimizer](StrategoOptimizer){.twikiLink} and the [Stratego
back end](StrategoBackEnd){.twikiLink}.

Components of the front-end include

-   [pack
    stratego[^?^](http://www.program-transformation.org/edit/Stratego/PackStratego?topicparent=Stratego.StrategoFrontEnd)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [use def
    analysis[^?^](http://www.program-transformation.org/edit/Stratego/UseDefAnalysis?topicparent=Stratego.StrategoFrontEnd)]{.twikiNewLink
    style="background : #FFFFCE;"}

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Aug 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
