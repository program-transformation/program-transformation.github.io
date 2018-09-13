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
    Page](http://www.program-transformation.org/edit/Stratego/UserDefinableDesugaring?t=1536825717)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/UserDefinableDesugaring)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/UserDefinableDesugaring)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/UserDefinableDesugaring?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/UserDefinableDesugaring?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/UserDefinableDesugaring?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/UserDefinableDesugaring)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/UserDefinableDesugaring?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/UserDefinableDesugaring?template=oopsmore&param1=1.1&param2=1.1)
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
User Definable Desugaring {#user-definable-desugaring .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

-   Allow some specification of a desugaring tool in a meta file to
    apply to concrete syntax
-   Make it easier to add custom desugarings (use [meta
    file](ModuleMetaFile){.twikiLink}?), maybe implement extra
    desugaring for concat\*string (use &?)
-   Let the Stratego compiler not desugar the AST of a concrete syntax
    section with the Stratego desugaring rules.
-   Depending on the desugaring solution and the location of
    [MetaExplode](MetaExplode){.twikiLink} in the pipeline,
    [MetaExplode](MetaExplode){.twikiLink} should double quote strings.
    Also lists should be represented in the same way as they are
    represented after parsing.

------------------------------------------------------------------------

[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.UserDefinableDesugaring)]{.twikiNewLink
style="background : #FFFFCE;"}
[CategoryConcreteObjectSyntax](CategoryConcreteObjectSyntax){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
