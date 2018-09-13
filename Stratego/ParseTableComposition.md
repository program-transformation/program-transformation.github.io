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
    Page](http://www.program-transformation.org/edit/Stratego/ParseTableComposition?t=1536825604)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ParseTableComposition)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ParseTableComposition)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ParseTableComposition?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ParseTableComposition?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Stratego/ParseTableComposition?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/ParseTableComposition?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/ParseTableComposition?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/ParseTableComposition?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/ParseTableComposition?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/ParseTableComposition?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ParseTableComposition)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ParseTableComposition?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Stratego/ParseTableComposition?template=oopsmore&param1=1.8&param2=1.8)
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
Parse Table Composition {#parse-table-composition .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](ParseTableComposition#Introduction)
    -   [Documentation](ParseTableComposition#Documentation)
-   [Download](ParseTableComposition#Download)
    -   [Releases](ParseTableComposition#Releases)
    -   [Subversion](ParseTableComposition#Subversion)
    -   [Installation](ParseTableComposition#Installation)
-   [Project Info](ParseTableComposition#Project_Info)
    -   [Contact and Mailing
        List](ParseTableComposition#Contact_and_Mailing_List)
    -   [Source Repository](ParseTableComposition#Source_Repository)
    -   [Team](ParseTableComposition#Team)
:::

[]{#Introduction} Introduction
------------------------------

[ Extensible Compilers.]{.smallcaps} Many extensible compilers and
programming languages allow the syntax of a base language to be extended
to introduce new syntactic abstractions. For example, the extensible
compilers [ableJ](http://www.melt.cs.umn.edu/ablej14.html) (based on
Silver), the [JastAdd extensible Java
compiler](http://jastadd.cs.lth.se/web/extjava/),
[Polyglot](http://www.cs.cornell.edu/projects/polyglot/), and
[MetaBorg](MetaBorg){.twikiLink} support the development of language
extensions. The focus of these tools is on optimizing the work of the
compiler developer through *source-level extensibility*; that is, to
create an implementation of an extended compiler by touching as little
as possible the code of the base compiler. To some extent, some of the
existing extensible compilers also support the combination of
implementations of language extensions such that multiple, independent,
extensions can be used in the same source program (a form of independent
extensibility).

[ Binary Extensibility.]{.smallcaps} However, each extension (or
combination of extensions) results in a different compiler. If the user
of the compiler needs a new combination of extensions, then he needs to
build a new compiler. In these tools, syntactic extensibility is mostly
monolithic, i.e. the syntax extensions are compiled together with the
syntax of the base language into a single parse table. Not only does
this complicate the independent evolution of the extensions and the base
language, but it also make it difficult to let the *user* of the
compiler select a number of (third party) extensions that he wants to
use in a program.

To support scenarios which require more dynamic configurations of
language combinations, it is desirable to support *binary*
extensibility. That is, extensibility that does not require rebuilding
the compiler. This would make it possible to deploy a single version of
the compiler, which users can then extend by plugging in separately
deployed language components, where potentially each compilation unit
uses a different combination of extensions.

[ Parse Table Composition.]{.smallcaps} o solve the syntactic aspect of
this goal, we developed *parse table composition*, a mechanism for
combining parse tables, rather than grammars. At generation-time,
grammars are compiled separately into *parse table components*. At
run-time of a compiler, the parse table for the base language is
combined with a series of parse tables based on a user-selection of the
desired extensions. Online parse table composition results in a single
parse table that is used by the parser to parse a source program

Composing a series of parse table components can be performed very
efficiently, making the user of the compiler unaware of the parse table
composition. Soon, the user will be familiar with the idea of a parser
that parses a source file according to a series of parse table
components, rather than a single one. After the parser generator has
been applied to the individual components, linking the components
typically just requires a minimal reconstruction of the parse table.
This is a classical partial evaluation argument: as opposed to applying
the full parser generation to all the involved grammars, the parser
generation has already been partially applied.

The parse table composition algorithm is based on partial reapplication
of subset construction, which converts an NFA to a DFA. Subset
construction is the essence of the LR parse table generation algorithm,
hence the method is easy to understand and relate to basic, monolithic,
parse table generation algorithm.

[ Prototype.]{.smallcaps} The prototype you can download from this page
targets a scannerless, generalized-LR parser ([SGLR](SGLR){.twikiLink})
and takes (possibly incomplete) [SDF](http://www.syntax-definition.org)
grammars as input. The source code is available under the MIT license.

### []{#Documentation} Documentation

-   Martin Bravenboer and Eelco Visser. *Parse Table Composition:
    Separate Compilation and Binary Extensibility of Grammars*
    ([pdf](http://martin.bravenboer.name/docs/ptc-draft.pdf), draft)

Of course, feel free to [contact us](mailto:martin.bravenboer@gmail.com)
with questions.

[]{#Download} Download
----------------------

### []{#Releases} Releases

Distributions of the head revision are created continuously:

-   <http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt/parse-table-composition-unstable-latest/>

### []{#Subversion} Subversion

The distributions contain the latest of the latest developments, but if
you really want to, the latest sources can be checked out using:\

    $ svn checkout https://svn.cs.uu.nl:12443/repos/StrategoXT/parse-table-composition/trunk

Before you can configure the package as described below you have to run
the `./bootstrap` script. Also, pass `--enable-bootstrap` to the
configure script.

### []{#Installation} Installation

The parse-table-composition package is a prototype built on top of
Stratego/XT. The release page of the parse-table-composition lists a
number of source packages that you need to install first:

-   aterm
-   sdf2-bundle
-   strategoxt
-   strategoxt-utils

Install all the package with the usual sequence of commands:

    $ ./configure --prefix=/where/you/want/to/install/the/packages
    $ make
    $ make install

See the [Installation
Chapter](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/installation.html)
if you experience any problems with this. You might need to set your
`PKG_CONFIG_PATH` if you did not install the dependencies in a standard
location. Configure will tell you to do this if it cannot find aterm,
sdf, strategoxt or strategoxt-utils.

[]{#Project_Info} Project Info
------------------------------

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [stratego\@cs.uu.nl mailing
list](https://mail.cs.uu.nl/mailman/listinfo/stratego). Also, the
developers are usually available on IRC at
[irc.freenode.net/stratego](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Source_Repository} Source Repository

The sources are available from Subversion.

-   <https://svn.cs.uu.nl:12443/repos/StrategoXT/parse-table-composition/trunk>

### []{#Team} Team

Developers:

-   [Martin Bravenboer](http://martin.bravenboer.name)

Feedback:

-   [Eelco Visser](../Main/EelcoVisser){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
