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
    Page](http://www.program-transformation.org/edit/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?t=1536825431)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Stratego/RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax?template=oopsmore&param1=1.6&param2=1.6)
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
[B. Fischer](http://ase.arc.nasa.gov/people/fischer/) and E. Visser.
**Retrofitting the [AutoBayes](AutoBayes){.twikiLink} Program Synthesis
System with Concrete Object Syntax.** In C. Lengauer et al., editors,
Domain-Specific Program Generation, volume 3016 of Lecture Notes in
Computer Science, pages 239\--253. Spinger-Verlag, 2004.
([techrep](http://www.cs.uu.nl/research/techreps/UU-CS-2004-012.html))

### []{#Abstract} Abstract

[AutoBayes](AutoBayes){.twikiLink} is a fully automatic, schema-based
program synthesis system for statistical data analysis applications. Its
core component is a schema library, i.e., a collection of generic code
templates with associated applicability constraints which are
instantiated in a problem-specific way during synthesis. Currently,
[AutoBayes](AutoBayes){.twikiLink} is implemented in Prolog; the schemas
thus use abstract syntax (i.e., Prolog terms) to formulate the
templates. However, the conceptual distance between this abstract
representation and the concrete syntax of the generated programs makes
the schemas hard to create and maintain.

In this paper we describe how [AutoBayes](AutoBayes){.twikiLink} is
retrofitted with concrete syntax. We show how it is integrated into
Prolog and describe how the seamless interaction of concrete syntax
fragments with [AutoBayes](AutoBayes){.twikiLink}\'s remaining
\`\`legacy\'\' meta-programming kernel based on abstract syntax is
achieved. We apply the approach to gradually migrate individual schemas
without forcing a disruptive migration of the entire system to a
different meta-programming language. First experiences show that a
smooth migration can be achieved. Moreover, it can result in a
considerable reduction of the code size and improved readability of the
code. In particular, abstracting out fresh-variable generation and
second-order term construction allows the formulation of larger
continuous fragments.

### []{#Links} Links

-   [PrologTools](PrologTools){.twikiLink} : implementation
-   [AutoBayes](AutoBayes){.twikiLink}
-   [Concrete syntax](ConcreteSyntax){.twikiLink}
-   [Meta programming with concrete object
    syntax](MetaProgrammingWithConcreteObjectSyntax){.twikiLink}
-   [CategoryConcreteObjectSyntax](CategoryConcreteObjectSyntax){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
