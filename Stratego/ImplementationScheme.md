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
    Page](http://www.program-transformation.org/edit/Stratego/ImplementationScheme?t=1536825588)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ImplementationScheme)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ImplementationScheme)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ImplementationScheme?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ImplementationScheme?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ImplementationScheme?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ImplementationScheme?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ImplementationScheme?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ImplementationScheme)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ImplementationScheme?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/ImplementationScheme?template=oopsmore&param1=1.2&param2=1.2)
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
Implementation Scheme {#implementation-scheme .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Ideas for improving the implementation scheme of the
[StrategoCompiler](StrategoCompiler){.twikiLink}. Feel free to add
ideas.

-   [GlobalBacktracking[^?^](http://www.program-transformation.org/edit/Stratego/GlobalBacktracking?topicparent=Stratego.ImplementationScheme)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ImplementationOfFailure](ImplementationOfFailure){.twikiLink}
-   [Unbind variables on
    backtracking](UnbindVariablesOnBacktracking){.twikiLink}
-   [ForeignFunctions[^?^](http://www.program-transformation.org/edit/Stratego/ForeignFunctions?topicparent=Stratego.ImplementationScheme)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [SeparateCompilation](SeparateCompilation){.twikiLink}
-   [DynamicLinking[^?^](http://www.program-transformation.org/edit/Stratego/DynamicLinking?topicparent=Stratego.ImplementationScheme)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   Other target languages
    -   [TranslationToJVM[^?^](http://www.program-transformation.org/edit/Stratego/TranslationToJVM?topicparent=Stratego.ImplementationScheme)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [TranslationToJava[^?^](http://www.program-transformation.org/edit/Stratego/TranslationToJava?topicparent=Stratego.ImplementationScheme)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [TranslationToHaskell[^?^](http://www.program-transformation.org/edit/Stratego/TranslationToHaskell?topicparent=Stratego.ImplementationScheme)]{.twikiNewLink
        style="background : #FFFFCE;"}

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Dec 2001\

------------------------------------------------------------------------

[ToDo](ToDo){.twikiLink} \|
[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.ImplementationScheme)]{.twikiNewLink
style="background : #FFFFCE;"} \|
[CompilerImprovements](CompilerImprovements){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
