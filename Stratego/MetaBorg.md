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
    Page](http://www.program-transformation.org/edit/Stratego/MetaBorg?t=1536825457)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/MetaBorg)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/MetaBorg)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/MetaBorg?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/MetaBorg?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    11](http://www.program-transformation.org/view/Stratego/MetaBorg?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Stratego/MetaBorg?rev1=1.11&rev2=1.10)
-   [Rev
    10](http://www.program-transformation.org/view/Stratego/MetaBorg?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Stratego/MetaBorg?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Stratego/MetaBorg?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/MetaBorg?rev1=1.9&rev2=1.8)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/MetaBorg)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/MetaBorg?template=oopsmore&param1=1.11&param2=1.11)
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
    \...](http://www.program-transformation.org/oops/Stratego/MetaBorg?template=oopsmore&param1=1.11&param2=1.11)
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
Meta Borg {#meta-borg .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[MetaBorg](MetaBorg){.twikiLink} is a method for providing *concrete
syntax* for domain abstractions to application programmers. The method
consists of *embedding* domain-specific languages in a general purpose
host language and *assimilating* the embedded domain code into the
surrounding host code. Instead of extending the implementation of the
host language, the assimilation phase implements domain abstractions in
terms of existing APIs leaving the host language undisturbed. Indeed,
[MetaBorg](MetaBorg){.twikiLink} can be considered a method for
promoting APIs to the language level.

### []{#Publications} Publications

The [MetaBorg](MetaBorg){.twikiLink} approach is described in the
following papers:

-   [Concrete Syntax for
    Objects](http://www.program-transformation.org/Stratego/ConcreteSyntaxForObjects){.twikiLink}
    about [JavaBorg](JavaBorg){.twikiLink} (OOPSLA\'04)
-   [MetaBorg in
    Action](http://www.cs.uu.nl/wiki/Visser/MetaBorgInAction)
    (GTTSE\'05)
-   [Meta programming with concrete object
    syntax](MetaProgrammingWithConcreteObjectSyntax){.twikiLink} about
    concrete syntax in Stratego (GPCE\'02)
-   [Retrofitting the AutoBayes program synthesis system with concrete
    syntax](RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax){.twikiLink}
    about concrete syntax in Prolog
-   [Generalized type-based disambiguation of meta programs with
    concrete object
    syntax](http://www.cs.uu.nl/wiki/Visser/GeneralizedTypeBasedDisambiguationOfMetaProgramsWithConcreteObjectSyntax)
    (GPCE\'05)

### []{#Instantiations} Instantiations

The [MetaBorg](MetaBorg){.twikiLink} approach has been instantiated for
the following host and embedded languages:

-   Stratego
    -   Embedded languages: Stratego, Java, XML, Tiger, \...
    -   See: [Concrete syntax](ConcreteSyntax){.twikiLink} in Stratego
-   Java
    -   Embedded languages: Java, XML, Swul (Swing user interface
        language), regular expressions
    -   See: [JavaJava](JavaJava){.twikiLink} (Java in Java),
        [JavaBorg](JavaBorg){.twikiLink} (various small samples, e.g
        XML), [Java-Swul](Java-Swul){.twikiLink} (embedding of Swing
        user interface language)
-   Prolog
    -   Embedded languages: ABIR ([AutoBayes](AutoBayes){.twikiLink}
        Intermediate Representation)
    -   See: [PrologTools](PrologTools){.twikiLink}

### []{#Implementation} Implementation

A generic implementation for parsing with concrete syntax is provided in
the

-   [concrete syntax package](ConcreteSyntaxPackage){.twikiLink}

in the [StrategoXT](StrategoXT){.twikiLink} distribution. Concrete
syntax is support is built into the Stratego compiler. For Java and
Prolog we have built pre-processors that transform Java/Prolog programs
with concrete syntax into pure Java/Prolog programs.

-   [JavaBorg](JavaBorg){.twikiLink}
-   [PrologTools](PrologTools){.twikiLink}

### []{#Why_call_it_MetaBorg}[]{#Why_call_it_MetaBorg_} Why call it [MetaBorg](MetaBorg){.twikiLink}?

[MetaBorg](MetaBorg){.twikiLink} provides generic technology for
allowing a host language (collective) to incorporate and assimilate
external domains (cultures) in order to strengthen itself. The ease of
implementing embeddings makes resistance futile.

If you still don\'t get it you should probably [read
on](http://www.startrek.com/startrek/view/library/aliens/article/70558.html).

### []{#Authors} Authors

[MetaBorg](MetaBorg){.twikiLink} is being developed by

-   [Martin Bravenboer](../Main/MartinBravenboer){.twikiLink}
-   [Eelco Visser](../Main/EelcoVisser){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
