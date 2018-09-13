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
    Page](http://www.program-transformation.org/edit/Stratego/MetaExplode?t=1536825599)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/MetaExplode)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/MetaExplode)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/MetaExplode?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/MetaExplode?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/MetaExplode?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/MetaExplode?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/MetaExplode?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/MetaExplode?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/MetaExplode?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/MetaExplode)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/MetaExplode?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/MetaExplode?template=oopsmore&param1=1.3&param2=1.3)
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
Meta Explode {#meta-explode .twikiTopicTitle}
============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

When using [concrete syntax](ConcreteSyntax){.twikiLink} for the [object
language[^?^](http://www.program-transformation.org/edit/Stratego/ObjectLanguage?topicparent=Stratego.MetaExplode)]{.twikiNewLink
style="background : #FFFFCE;"} the input is parsed against the combined
syntax of the object language (for example Tiger, Java, XML or Stratego)
and the [meta
language[^?^](http://www.program-transformation.org/edit/Stratego/MetaLanguage?topicparent=Stratego.MetaExplode)]{.twikiNewLink
style="background : #FFFFCE;"} (in this case Stratego). This will result
in an [abstract syntax tree](AbstractSyntaxTree){.twikiLink} that
contains a mixture of meta- and object language abstract syntax. Since
the [meta
language[^?^](http://www.program-transformation.org/edit/Stratego/MetaLanguage?topicparent=Stratego.MetaExplode)]{.twikiNewLink
style="background : #FFFFCE;"} compiler only deals with the
meta-language abstract syntax, the embedded object language abstract
syntax needs to be expressed in terms of meta abstract syntax.

The transitions from the meta language to the object language and vice
versa are marked by special constructors: [meta transition
markers](MetaTransitionMarker){.twikiLink}. [meta
explode](MetaExplode){.twikiLink} uses these constructors to determine
the object fragments in the abstract syntax tree that have to be
exploded to the meta language.

For Stratego this transformation is indepedent of the object language
and is therefore generic. The [meta explode](MetaExplode){.twikiLink}
transformation component implements this explosion. It is used by the
[Stratego Compiler](StrategoCompiler){.twikiLink}

------------------------------------------------------------------------

[CategoryConcreteObjectSyntax](CategoryConcreteObjectSyntax){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
