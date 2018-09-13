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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoXT?t=1536825461)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoXT)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoXT)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoXT?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoXT?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Stratego/StrategoXT?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/StrategoXT?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/StrategoXT?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/StrategoXT?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/StrategoXT?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/StrategoXT?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoXT)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoXT?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoXT?template=oopsmore&param1=1.7&param2=1.7)
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
About Stratego/XT {#about-strategoxt .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Stratego/XT is the combination of the [Stratego
language](StrategoLanguage){.twikiLink} for strategic programming with
the XT bundle of transformation tools.

### []{#XT} XT

XT is a bundle of transformation tools that combines Stratego, a
language for transformation of abstract syntax trees, with tools for
other aspects of program transformation. Stratego only deals with
transformation of programs represented by means of terms. Parsing and
pretty-printing is provided by the XT bundle of transformation tools,
which combines Stratego with the Syntax Definition Formalism
[SDF](../Sdf/WebHome){.twikiLink} and the Generic Pretty-Printing
Package [GPP](../Tools/GenericPrettyPrinter){.twikiLink}.

### []{#ATerm_Exchange_Format} ATerm Exchange Format

The foundation of XT is the ATerm format for exchange of structured data
such as abstract syntax trees. The format essentially consists of
first-order prefix terms. The format is supported by libraries for C,
Java, and Haskell, which support reading and writing of ATerms.

### []{#SDF} [SDF](SDF){.twikiLink}

The Syntax Definition Formalism [SDF](../Sdf/WebHome){.twikiLink}
supports high-level, declarative, and modular definition of the syntax
of programming languages and data formats. The formalism integrates the
definition of lexical and context-free syntax. The modularity of the
formalism implies that it is possible to easily *combine* two languages
or to *embed* one language into another.

#### []{#Grammar_Base} Grammar Base

The SDF Grammar Base is a collection of syntax definitions for various
languages, including Java, C, SQL, COBOL, BibTex, Stratego, and SDF. The
Grammar Base will be distributed separately.

#### []{#Parser_Generation} Parser Generation

The parser generator PGEN Generates parse tables from SDF definitions.

#### []{#Scannerless_Generalized_LR_Parse} Scannerless Generalized-LR Parser

The scannerless generalized-LR parser [SGLR](SGLR){.twikiLink}
interprets parse tables generated from SDF definitions. The parser does
not use a separate scanner; lexical analysis is included in the parsing
process. The parser can deal with arbitrary context-free grammars.
Disambiguation is based on filters in different stages of the parsing
process.

### []{#Parse_Tree_Manipulation} Parse Tree Manipulation

XT provides several generic tools for parse tree manipulation such as
implosion of parse trees to abstract syntax trees.

### []{#Grammar_Engineering} Grammar Engineering

XT provides several tools for derivation of [SDF](SDF){.twikiLink}
syntax definitions from
[YACC](../Transform/YetAnotherCompilerCompiler){.twikiLink}-like
formalisms, which allows reusing existing grammars to a large extent,
and tools for improving syntax definitions.

### []{#Generic_Pretty_Printing_Package} Generic Pretty-Printing Package

Generic pretty-printing package
([GPP](../Tools/GenericPrettyPrinter){.twikiLink}) is based on the
device-independent Box format and allows pretty-printing to different
targets; now supported are text, html and latex. Pretty-printers are
driven by pretty-print tables, which can be generated automatically from
syntax definitions.

### []{#Application_Areas} Application Areas

XT is applicable in a many instances of program transformation including

-   Meta-programming
-   Generative programming
-   Compilation
-   Implementation of domain-specific languages
-   Language extensions
-   Documentation generation
-   Software visualization

### []{#Brochure} Brochure

This two page brochure

-   <http://www.stratego-language.org/ftp/StrategoXT.pdf>

summarizes the main features of Stratego and XT. Useful for distribution
at conferences and such.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Nov 2002\
\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 04 Jun 2002\

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
