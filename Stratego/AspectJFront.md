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
    Page](http://www.program-transformation.org/edit/Stratego/AspectJFront?t=1536825368)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/AspectJFront)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/AspectJFront)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/AspectJFront?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/AspectJFront?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    23](http://www.program-transformation.org/view/Stratego/AspectJFront?rev=1.23)
    [(diff 22)](http://www.program-transformation.org/rdiff/Stratego/AspectJFront?rev1=1.23&rev2=1.22)
-   [Rev
    22](http://www.program-transformation.org/view/Stratego/AspectJFront?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Stratego/AspectJFront?rev1=1.22&rev2=1.21)
-   [Rev
    21](http://www.program-transformation.org/view/Stratego/AspectJFront?rev=1.21)
    [(diff 20)](http://www.program-transformation.org/rdiff/Stratego/AspectJFront?rev1=1.21&rev2=1.20)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/AspectJFront)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/AspectJFront?template=oopsmore&param1=1.23&param2=1.23)
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
    \...](http://www.program-transformation.org/oops/Stratego/AspectJFront?template=oopsmore&param1=1.23&param2=1.23)
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
AspectJ-front {#aspectj-front .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](AspectJFront#Introduction)
    -   [Applications](AspectJFront#Applications)
    -   [Variations](AspectJFront#Variations)
    -   [Quality and Testing](AspectJFront#Quality_and_Testing)
-   [Documentation](AspectJFront#Documentation)
    -   [Publications](AspectJFront#Publications)
-   [Download](AspectJFront#Download)
    -   [Latest Release](AspectJFront#Latest_Release)
    -   [Installation](AspectJFront#Installation)
    -   [Subversion Checkout](AspectJFront#Subversion_Checkout)
-   [Project Info](AspectJFront#Project_Info)
    -   [Issue Tracking](AspectJFront#Issue_Tracking)
    -   [Contact and Mailing
        List](AspectJFront#Contact_and_Mailing_List)
    -   [Source Repository](AspectJFront#Source_Repository)
    -   [Feedback](AspectJFront#Feedback)
    -   [Team](AspectJFront#Team)
    -   [License](AspectJFront#License)
-   [Testsuite Issues](AspectJFront#Testsuite_Issues)
    -   [AJC](AspectJFront#AJC)
-   [Acknowledgements](AspectJFront#Acknowledgements)
:::

[]{#Introduction} Introduction
------------------------------

AspectJ-front provides:

-   Modular syntax definition for AspectJ 5.0 in
    [SDF](http://www.syntax-definition.org). The AspectJ syntax
    definition is an extension of the modular syntax definition of Java
    provided by [Java-front](JavaFront){.twikiLink}.

<!-- -->

-   Hand-crafted pretty-printer for AspectJ. The pretty-printer is an
    extension of the pretty-printer for the Java in
    [Java-front](JavaFront){.twikiLink}.

AspectJ-front can be used to parse AspectJ programs and pretty-print the
abstract syntax tree back to an AspectJ source file. The parse result is
in the ATerm format (which can be converted to XML using `aterm2xml`).

### []{#Applications} Applications

Possible applications of AspectJ-front include:

-   One of the killer features of the syntax definition is its
    *extensibility*. Therefore, one of the applications of AspectJ-front
    could be the prototyping of AspectJ extensions by a syntactic
    extension of the AspectJ syntax, followed by a desugaring (possibly
    implemented in [Stratego](WebHome){.twikiLink}) to plain AspectJ.

<!-- -->

-   AspectJ-front could be used in the *front-end* of an AspectJ
    compiler.

<!-- -->

-   AspectJ-front can be used for the *generation* of AspectJ programs
    using concrete AspectJ syntax (similar to
    [Meta-AspectJ](http://www-static.cc.gatech.edu/~yannis/maj/) and
    [JavaJava](JavaJava){.twikiLink}).

<!-- -->

-   AspectJ-front can be used to *analyse* AspectJ programs
    syntactically. If you need more semantic information, then you need
    to do more work or use an existing AspectJ compiler.

### []{#Variations} Variations

AspectJ-front defines three variations of the AspectJ language:

-   **AJF**, which is the most liberal definition, where only real
    ambiguities are resolved, for example by reserving keywords at very
    specific locations.

<!-- -->

-   **AJC**, which adds restrictions to the language (pseudo keywords)
    to be more compatible with the [official AspectJ
    compiler](http://wwww.aspectj.org).

<!-- -->

-   **ABC**, which reserves keywords in a context-sensitive way, thus
    defining the language supported by the
    [abc](http://abc.comlab.ox.ac.uk) compiler for AspectJ.

The main tool of aspectj-front, `parse-aspectj`, supports these
variations by the command-line options `--abc` and `--ajc`.

### []{#Quality_and_Testing} Quality and Testing

**Unit Testing.** AspectJ-front has a testsuite based on parse-unit, a
unit-testing tool for SDF. This testsuite mostly tests problematic
syntax that we have encountered while working on the AspectJ syntax
definition. In the testsuite, the results of the parses are checked by
comparing the resulting AST to an expected AST pattern.

**Roundtrip Testing.** AspectJ-front is not a complete compiler, so we
cannot just apply the existing testsuites for AspectJ. Instead, we run
roundtrip tests for all the valid source files in the available
testsuites. By roundtrip testing we refer to the full cycle of a parse,
followed by a pretty-print, followed by a second parse, followed by a
diff of the first and the second parse. Roundtrip testing is useful for
finding problems in the parser as well as the pretty-printer.

**AJC.** The *AJC* variant of the AspectJ syntax is continuously tested
in our buildfarm by a roundtrip test of all the valid AspectJ source
files in the ajc testsuite 1.5.0 ([download
checkout](ftp://ftp.stratego-language.org/pub/stratego/aspectj-front/aspectj-tests-1.5.0.tar.gz)).
The [latest test
reports](http://nix.cs.uu.nl/dist/stratego/aspectj-front-testing-0.1pre20060413-2034/docs/)
(warning: big file) are available and show all the abstract syntax trees
and the pretty-printed source files. There are a few minor issues that
have not solved because it is unclear if the syntax used in the test
files should be supported at all. The issues are
[discussed](AspectJFront#AjcIssues){.twikiAnchorLink} later at this
webpage.

**ABC.** The *ABC* variant has not yet been tested using the full abc
testsuite: we have only applied selected sources. We are working on a
full report of AspectJ-front applied to the abc testsuite.

See also the notes on quality and compliance for the [Java syntax
definition](JavaFront){.twikiLink} on which AspectJ-front is based.

[]{#Documentation} Documentation
--------------------------------

You can browse the syntax definition of AspectJ (including Java) online:

-   [Main AspectJ
    module](http://releases.strategoxt.org/docs/syntax/aspectj-front/stable/docs/html/languages/aspectj/JavaExtension.sdf.html)

Variations:

-   [ABC](http://releases.strategoxt.org/docs/syntax/aspectj-front/stable/docs/html/languages/aspectj/abc/Main.sdf.html)
-   [AJF](http://releases.strategoxt.org/docs/syntax/aspectj-front/stable/docs/html/languages/aspectj/ajf/Main.sdf.html)
-   [AJC](http://releases.strategoxt.org/docs/syntax/aspectj-front/stable/docs/html/languages/aspectj/ajc/Main.sdf.html)

### []{#Publications} Publications

AspectJ-front has been used for the following research publications and
dissertations (reverse chronological) :

-   Sérgio Bryton. **Modularity Improvements with Aspect-Oriented
    Programming**. MSc thesis, Universidade Nova de Lisboa, 2008.

<!-- -->

-   Pavel Avgustinov, Elnar Hajiyev, Neil Ongkingco, Oege de Moor,
    Damien Sereni, Julian Tibble, Mathieu Verbaere. **Semantics of
    static pointcuts in AspectJ**. In Proceedings of the SIGPLAN-SIGACT
    Symposium on Principles of Programming Language (POPL), Nice,
    France, January 2007. (
    [webpage](http://progtools.comlab.ox.ac.uk/members/oege/publications/popl07abc)
    )

<!-- -->

-   Martin Bravenboer, Éric Tanter, and Eelco Visser. **Declarative,
    Formal, and Extensible Syntax Definition for AspectJ - A Case for
    Scannerless Generalized-LR Parsing**. In Proceedings of the 21st ACM
    SIGPLAN *Conference on Object-Oriented Programming, Systems,
    Languages, and Applications ([OOPSLA
    2006](http://www.oopsla.org/2006/))*, Portland, USA, October 2006.
    ([pdf](http://www.cs.uu.nl/~martin/docs/oopsla06.pdf))

<!-- -->

-   Eric Tanter. **An Extensible Kernel Language for AOP**. In
    Proceedings of the AOSD Workshop on Open and Dynamic Aspect
    Languages (ODAL 2006). March 2006, Bonn, Germany.

<!-- -->

-   Martin Bravenboer, Rob Vermaas, Jurgen Vinju and Eelco Visser.
    **Generalized Type-Based Disambiguation of Meta Programs with
    Concrete Object Syntax**. In *Proceedings of the Fourth
    International Conference on Generative Programming and Component
    Engineering ([GPCE 2005](../Gpce05/index.html))*, Tallinn, Estonia,
    September 2005.
    ([pdf](http://www.cs.uu.nl/~martin/docs/disamb-gpce05.pdf),
    [presentation](http://www.cs.uu.nl/~martin/docs/gpce05-slides.pdf))

[]{#Download} Download
----------------------

### []{#Latest_Release} Latest Release

Distributions (source tarball, RPM, source RPM, binary for Microsoft
Windows) are created continuously:

-   <http://releases.strategoxt.org/aspectj-front/unstable/>

AspectJ-front contains a subpackage `aspectj-front-syntax` which just
provides the syntax definition and parsetables (not the command-line
tools and the pretty-printer). This subpackage has no dependencies at
all. The latest release is available at:

-   <http://releases.strategoxt.org/aspectj-front-syntax/unstable/>

### []{#Installation} Installation

AspectJ-front requires `aterm`, `sdf2-bundle`, `strategoxt`, and
`java-front`, which are available from the release page of
AspectJ-front. If necessary (e.g. for MinGW compilation) you can replace
`strategoxt` with `stratego-libraries` and leave out the `sdf2-bundle`.

Install AspectJ-front and its dependencies with the usual sequence of
commands:

    $ ./configure
    $ make
    $ make install

You might need to set your `PKG_CONFIG_PATH` if you did not install the
dependencies in a standard location. Configure will tell you to do this
if it cannot find aterm, java-front, stratego-libraries, or strategoxt.

On Cygwin and MinGW you need to increase the default stack size, or the
resulting tools will immediately produce a segmentation fault. You an do
this by setting `CFLAGS` to `-O2 -Wl,--stack=0x2300000`.

### []{#Subversion_Checkout} Subversion Checkout

The distributions contain the latest of the latest developments, but if
you really want to, the latest sources can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/aspectj-front/trunk

Before you can configure the package as described above you have to run
the `./bootstrap` script.

[]{#Project_Info} Project Info
------------------------------

### []{#Issue_Tracking} Issue Tracking

We use yellowgrass.org to keep track of issues. Please report any issues
that you encounter!

-   <http://yellowgrass.org/project/AspectJFront>

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [users\@strategoxt.org mailing
list](MailingList){.twikiLink}. Also, the AspectJ-front developers are
usually available on IRC at
[irc.freenode.net/stratego](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Source_Repository} Source Repository

The sources are available from Subversion:

-   <https://svn.strategoxt.org/repos/StrategoXT/aspectj-front/>

### []{#Feedback} Feedback

Questions:

-   <users@strategoxt.org> (subscribe to the [mailing
    list](MailingList){.twikiLink})

Please report bugs to our issue tracking system:

-   <http://yellowgrass.org/project/AspectJFront>

### []{#Team} Team

Contributors:

-   [Martin Bravenboer](http://www.cs.uu.nl/wiki/Martin) (lead
    developer)
-   [Rob Vermaas](../Main/RobVermaas){.twikiLink}

Feedback and bug reports:

-   [Eelco Visser](../Main/EelcoVisser){.twikiLink}
-   [Éric Tanter](http://www.dcc.uchile.cl/~etanter/)
-   Fabiano Ferrari

Sponsors:

-   [Department of Information and Computing Sciences, University of
    Utrecht](http://www.cs.uu.nl)
-   [NWO Jacquard](http://www.jacquard.nl/) project
    [TraCE](http://www.cs.uu.nl/wiki/Trace/WebHome)

### []{#License} License

AspectJ-front is [LGPL](LGPL){.twikiLink} (GNU Lesser General Public
License) software.

[]{#Testsuite_Issues} Testsuite Issues
--------------------------------------

[]{#AjcIssues}

### []{#AJC} AJC

The AJC roundtrip testsuite reports a few failures that we have
deliberately not resolved.

-   `new/IntroducedFieldInc.java`. For this file the final diff fails.
    However, there is a not a difference between the two files. The
    problem is that the AspectJ-front pretty-printer inserts parentheses
    only where necessary. The original file has unnecessary parentheses,
    which gives the parser slightly more information about the use of an
    identifier: `(i).count` is guaranteed to be a field access, where
    i.count requires semantic analysis to find out if `i` is a typename.

<!-- -->

-   `pureJava/test120/Driver.java`. This file uses a unicode escape
    outside of a string literal, which we do not support. The JLS
    requires unicode escapes to be processed before parsing (i.e.
    lexically). However, lexical preprocessing is inherently
    incompatible with composing languages, which is one of our main
    businesses. Therefore, we have not implemented such a preprocessor,
    though you can easily apply one if you want to (for example, the
    ANTLR grammar for Java comes with such a preprocessing tool).

<!-- -->

-   `bugs150/AnnotationPlusPatternParseError.aj`. This file uses the
    pointcut `call(* (@MemberOfMonitoredSet *)+.*(..))`. In the previous
    version of AspectJ, and according to the AspectJ 5 notebook, this is
    not allowed: subtype patterns are only allowed for names, not for
    type patterns. We will try to find out if this should be supported,
    and if so, change the syntax definition.

<!-- -->

-   `src/java5/annotations/aspectMembers/a/AnnotatedAspect08.aj`. This
    is an invalid source file that is not allowed by the `ajc` compiler
    itself. Currently it is unclear to us why this file is in the
    testsuite at all.

<!-- -->

-   `src/java5/generics/pointcuts/GenericDeclaringTypeWithParameterErasure.aj`.
    This file uses a parameterized execution pointcut, which is not
    allowed by `ajc` either.

[]{#Acknowledgements} Acknowledgements
--------------------------------------

The [SDF](SDF){.twikiLink} syntax definition for the aspect part of
AspectJ is based on the technical report

-   *\"The abc scanner and parser, including an LALR(1) grammar for
    AspectJ\"* by Laurie Hendren, Oege de Moor, Aske Simon Christensen
    and the abc team. ([AspectBench Compiler for
    AspectJ](http://abc.comlab.ox.ac.uk)).

This report defines the syntax of the AspectJ languages in more formal
way, which does not seem available from the AspectJ project themselves.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
