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
    Page](http://www.program-transformation.org/edit/Stratego/ImplementationOfFailure?t=1536825588)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ImplementationOfFailure)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ImplementationOfFailure)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ImplementationOfFailure?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ImplementationOfFailure?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ImplementationOfFailure?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ImplementationOfFailure?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ImplementationOfFailure?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ImplementationOfFailure?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ImplementationOfFailure?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ImplementationOfFailure)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ImplementationOfFailure?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/ImplementationOfFailure?template=oopsmore&param1=1.3&param2=1.3)
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
Implementation Of Failure {#implementation-of-failure .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Before [StrategoRelease06](StrategoRelease06){.twikiLink} failure was
implemented in the [StrategoCompiler](StrategoCompiler){.twikiLink} by
using GCC\'s computed labels feature.

Starting with [StrategoRelease06](StrategoRelease06){.twikiLink} failure
handling is implemented using setjmp and longjmp.

Starting with [StrategoRelease07](StrategoRelease07){.twikiLink} failure
can optionally be handled using
[PierreEtienneMoreau[^?^](http://www.program-transformation.org/edit/Transform/PierreEtienneMoreau?topicparent=Stratego.ImplementationOfFailure)]{.twikiNewLink
style="background : #FFFFCE;"}\'s
[ChoicePointLibrary[^?^](http://www.program-transformation.org/edit/Stratego/ChoicePointLibrary?topicparent=Stratego.ImplementationOfFailure)]{.twikiNewLink
style="background : #FFFFCE;"}. If this option is chosen (when
configuring the [StrategoCompiler](StrategoCompiler){.twikiLink}
distribution) support for
[GlobalBacktracking[^?^](http://www.program-transformation.org/edit/Stratego/GlobalBacktracking?topicparent=Stratego.ImplementationOfFailure)]{.twikiNewLink
style="background : #FFFFCE;"} is provided as well.

[ToDo](ToDo){.twikiLink}

-   [Unbind variables on
    backtracking](UnbindVariablesOnBacktracking){.twikiLink} (solved
    with
    [ChoicePointLibrary[^?^](http://www.program-transformation.org/edit/Stratego/ChoicePointLibrary?topicparent=Stratego.ImplementationOfFailure)]{.twikiNewLink
    style="background : #FFFFCE;"}?)

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Dec 2001\

------------------------------------------------------------------------

[ImplementationScheme](ImplementationScheme){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
