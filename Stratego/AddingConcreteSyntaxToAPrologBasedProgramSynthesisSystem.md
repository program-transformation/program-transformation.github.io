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
    Page](http://www.program-transformation.org/edit/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?t=1536825431)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/AddingConcreteSyntaxToAPrologBasedProgramSynthesisSystem?template=oopsmore&param1=1.3&param2=1.3)
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
B. Fischer and E. Visser. **Adding concrete syntax to a Prolog-based
program synthesis system** (extended abstract). In M. Bruynooghe,
editor, Preliminary proceedings of the International Symposium on
Logic-based Program Synthesis and Transformation (LOPSTR\'03), Uppsala,
Sweden, August 2003. ([pdf](http://www.cs.uu.nl/~visser/ftp/FV03.pdf))

This paper is subsumed by the paper \'[Retrofitting the AutoBayes
program synthesis system with concrete
syntax](RetrofittingTheAutoBayesProgramSynthesisSystemWithConcreteSyntax){.twikiLink}\'

### []{#Abstract} Abstract

Program generation and transformation systems manipulate large,
parameterized object language fragments. Support for user-definable
concrete syntax makes this easier but is typically restricted to certain
object and meta languages. We show how Prolog can be retrofitted with
concrete syntax and describe how a seamless interaction of concrete
syntax fragments with an existing \`\`legacy\'\' meta-programming system
based on abstract syntax is achieved. We apply the approach to gradually
migrate the schemas of the [AutoBayes](AutoBayes){.twikiLink} program
synthesis system to concrete syntax. First experiences show that this
can result in a considerable reduction of the code size and an improved
readability of the code. In particular, abstracting out fresh-variable
generation and second-order term construction allows the formulation of
larger continuous fragments and improves the \`\`locality\'\' in the
schemas.

### []{#Links} Links

-   [PrologTools](PrologTools){.twikiLink} \-- extension of Prolog with
    concrete syntax
-   [CategoryConcreteObjectSyntax](CategoryConcreteObjectSyntax){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
