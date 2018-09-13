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
    Page](http://www.program-transformation.org/edit/Stratego/ConcreteSyntaxPackage?t=1536825571)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ConcreteSyntaxPackage)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ConcreteSyntaxPackage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ConcreteSyntaxPackage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ConcreteSyntaxPackage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ConcreteSyntaxPackage?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ConcreteSyntaxPackage?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ConcreteSyntaxPackage?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ConcreteSyntaxPackage?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ConcreteSyntaxPackage?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ConcreteSyntaxPackage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ConcreteSyntaxPackage?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/ConcreteSyntaxPackage?template=oopsmore&param1=1.3&param2=1.3)
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
Concrete Syntax Package {#concrete-syntax-package .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Description](ConcreteSyntaxPackage#Description)
-   [Concrete Syntax Tools](ConcreteSyntaxPackage#Concrete_Syntax_Tools)
-   [Implementation](ConcreteSyntaxPackage#Implementation)
:::

### []{#Description} Description

The `concrete-syntax` package provides =parse-cs, a generic program for
parsing programs with embedded [concrete
syntax](ConcreteSyntax){.twikiLink}. The program is parameterized with
meta-data indicating components for various aspects such as parsing,
exploding, desugaring, and pretty-printing. The meta data can be
specified in a .meta file specific for a program to be parsed, or it can
be associated with an extension and registered in an
[XTC](XTC){.twikiLink} repository.

For example, the following is the contents of pl.meta, the meta-data for
Prolog programs with embedded syntax. The assumption (in this example)
is that syntax embeddings use a standard
([ToTerm[^?^](http://www.program-transformation.org/edit/Stratego/ToTerm?topicparent=Stratego.ConcreteSyntaxPackage)]{.twikiNewLink
style="background : #FFFFCE;"}) convention for indicating the boundary
between meta- and object-syntax.

      Meta([
        Syntax("Prolog"),
        ParseTable("Prolog.tbl"),
        Explode("prolog-explode"),
        PrettyPrintTable("Prolog-pretty.pp.af")
      ])

This information can be overridden in a file specific .meta file with
the same extension. For example, the following indicates an embedding of
ABIR in Prolog and a specific desugaring tool for this format:

      Meta([
        Syntax("PrologABIR"),
        PostExplodeDesugar("abir-in-prolog-implode")
      ])

It overrides the syntax component, and adds a desugaring component.

In order to define such meta-data for a whole class of programs, it can
be defined in a meta file associated with a new extension. For example,
the following is the contents plabir.meta, which defines all meta-data
for preprocessing Prolog with embedded ABIR in files with extension
.plabir.

      Meta([
        Syntax("PrologABIR"),
        Explode("prolog-explode"),
        PostExplodeDesugar("abir-in-prolog-implode"),
        PrettyPrintTable("Prolog-pretty.pp.af")
      ])

### []{#Concrete_Syntax_Tools} Concrete Syntax Tools

Parse-cs is the only tool provided by the package at the moment. Other
tools that might be provided in the future include:

-   embed-syntax : combines two syntax definitions embedding one in the
    other by generating quotation productions and variable schemas
    according to a standard schema which might be adapted.

<!-- -->

-   gen-explode : a generic explosion transformation for embeddings that
    can be expressed locally (term-like API in host language) and
    generically

### []{#Implementation} Implementation

Browse the implementation in the subversion repository:

-   <https://svn.cs.uu.nl:12443/repos/StrategoXT/trunk/StrategoXT/concrete-syntax/>

The package is available in the [daily
distribution](ContinuousDistribution){.twikiLink} of
[StrategoXT](StrategoXT){.twikiLink} and will be available in
[StrategoRelease094](StrategoRelease094){.twikiLink}.

The instantiation of the tool for Prolog is available in the
[PrologTools](PrologTools){.twikiLink} package.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
