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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease08?t=1536825546)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease08)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease08)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease08?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease08?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/StrategoRelease08?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease08?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/StrategoRelease08?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease08?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoRelease08?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease08?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease08)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease08?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease08?template=oopsmore&param1=1.4&param2=1.4)
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
Stratego Release 08 {#stratego-release-08 .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

See
[DependencyGraph08[^?^](http://www.program-transformation.org/edit/Stratego/DependencyGraph08?topicparent=Stratego.StrategoRelease08)]{.twikiNewLink
style="background : #FFFFCE;"} for an overview of the dependencies
between the packages involved in Release 0.8

Release 0.8

-   [TermAnnotations](TermAnnotation){.twikiLink}
-   Simple [ListMatching](ListMatching){.twikiLink}
-   [ConfigurationFiles[^?^](http://www.program-transformation.org/edit/Stratego/ConfigurationFiles?topicparent=Stratego.StrategoRelease08)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [InnermostFusion](InnermostFusion){.twikiLink}
-   [ConcreteSyntax](ConcreteSyntax){.twikiLink} implemented by
    [StrategoFront](StrategoFront){.twikiLink} package with
    -   [StrategoSyntax](StrategoSyntax){.twikiLink} in
        [SDF](SDF){.twikiLink}
    -   [StrategoPrettyPrinter](StrategoPrettyPrinter){.twikiLink} (pp
        table for use with [GPP](GPP){.twikiLink})
    -   [StrategoSignature](StrategoSignature){.twikiLink}
-   Pipes

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 27 Jun 2002\

[]{#From_the_NEWS_file} From the NEWS file
------------------------------------------

    Version 0.8

     released: June 26, 2002

    SUMMARY OF CHANGES

     * Support for concrete object syntax is provided in the stratego-front package
       - this includes the full syntax of Stratego in SDF
       - a pretty-printer for Stratego
       - a signature for Stratego abstract syntax
       - stratego-desugar: removes simple syntactic abstractions
       - meta-explode: explodes embedded abstract syntax into Stratego abstract syntax
       - MetaStratego: specification of transformations on Stratego programs 
         using concrete syntax
       - Paper "Meta-Programming with Concrete Object Syntax" -- explanation
       - Paper "Building Interpreters with Rewriting Strategies" -- application

     * The implementation of term annotations has been completed.

     * Syntax for list variables, with implementation of very simple list
       matching [t*] and [t,t*] (this is still an experimental feature;
       full support to follow)

     * Innermost fusion: an optimization that specializes applications of innermost
       to its argument, typically a choice of rules.
       - Paper "Fusing logic and control with local transformations: 
         An example optimization."

     * Use of configuration ATerm files instead of wrapper scripts

     * Better usage information for `sc -h'

     * Changes and deletions to overcome problems with case insensitiveness on
       windows and macos; Stratego should now install on Windows+cygwin

     * Lower-level primitives for process control such as fork, exec, and pipe.
       High-level combinations to connect to a child process via a
       pipe. (experimental feature)

     * Stratego-connect: a separate package extending Stratego with interprocess
       communication (experimental; this package is not yet part of the standard
       stratego bundle because of portability problems)

    MORE INFORMATION

     * http://www.stratego-language.org/Stratego/StrategoRelease08

    CONTRIBUTIONS

     * Martin Bravenboer provided test suite and library modules for
       annotations

     * Collaboration with Patricia Johann on the reimplementation of 
       innermost fusion with dynamic rules and concrete syntax

     * Merijn de Jonge worked on porting to Cygwin

     * Eelco Dolstra worked on porting to MacOS

    CONFIGURATION

     * See ./configure --help for all configuration options. Here are some
       typical configurations:

     * To get a Stratego installation without concrete syntax configure as

       ./configure --prefix=`pwd` \
       --with-aterm=/home/xt/XT-1.0

       assuming that the aterm installation in /home/xt/XT-1.0 is used. This
       set-up will not compile the sources in stratego-front *and* will also
       not compile the source of the Stratego compiler in sc. 

     * To use concrete syntax a number of additional configuration parameters are
       required. For example, this is how I configure the stratego distribution:

       ./configure --prefix=`pwd` \
       --with-aterm=/home/xt/XT-1.0 \
        --with-sglr=/home/xt/XT-1.0 \
        --with-pgen=/home/xt/XT-1.0 \
       --with-asfix-tools=/home/xt/XT-1.0 \
       --with-stratego-tools=/home/xt/XT-1.0 \
       --with-sdf-tools=/home/xt/XT-1.0 \
       --enable-concrete

       The components in the stratego-front package are not bootstrapped, i.e.,
       require the Stratego compiler. However, the generated C files are
       included in the distribution.

       This requires an installation of XT-1.0. Future distributions of XT will 
       integrate the Stratego packages with concrete syntax support. A minimal
       bundle for Stratego with concrete syntax will also be provided.

     * To bootstrap the compiler sources in sc/ use the option

       --enable-boot

       This requires configuring the options needed for concrete syntax, since some
       of the compiler components are written in MetaStratego.

     * To install on Windows platform with Cygwin use the --enable-exe option.

    STRATEGO FRONT (CONCRETE SYNTAX)

     * Support for concrete syntax is provided in the stratego-front package, including
       - Stratego.sdf: the full syntax of Stratego in SDF
       - astratego2text: a pretty-printer for Stratego
       - Stratego.r: a signature for Stratego abstract syntax
       - stratego-desugar: removes simple syntactic abstractions
       - meta-explode: a transformation that translates embedded abstract syntax
         into Stratego abstract syntax
       - MetaStratego: specification of transformations on Stratego programs 
         using concrete syntax

     * Paper
       - E. Visser. Meta-programming with concrete object syntax.
         In D. Batory and C. Consel, editors, Generative Programming and
         Component Engineering (GPCE'02), Lecture Notes in Computer
         Science. Springer-Verlag, October 2002. To appear.

       - Describes the use and implementation of concrete syntax in Stratego and
         extends the approach to arbitrary (meta-)programming languages.

       - http://www.stratego-language.org/Stratego/MetaProgrammingWithConcreteObjectSyntax

     * Example
       - An example of the use of concrete syntax is provided in the lambdapp package,
         which contains the specification from the LDTA'02 paper "Building
         Interpreters with Rewriting Strategies"; a collection of interpreters for 
         the lambda calculus extended with pattern matching rules, failure, and choice.

       - http://www.stratego-language.org/Stratego/BuildingInterpretersWithRewritingStrategies

       - http://www.stratego-language.org/ftp/lambdapp-0.1.tar.gz

    STRATEGO COMPILER (SC, SC-BOOT)

     * Innermost fusion
       - An optimization that specializes applications of innermost
         to its argument, typically a choice of rules. This an elaboration
         of the optimization described in the WRS'01 paper "Fusing Logic and
         Control".

       - http://www.stratego-language.org/Stratego/FusingLogicAndControl

     * The implementation of annotations has been completed

     * Syntax for list variables, with implementation of very simple list
       matching [t*] and [t,t*] (this is still an experimental feature;
       full support to follow)

     * Use of configuration ATerm files instead of wrapper scripts.

     * Better usage information for `sc -h'.

    STRATEGO STANDARD LIBRARY (SSL)

     * Installing .rtree files (parsed modules) instead of .r files
       (sources); saves time when compiling and ensures syntactic
       correctness of library modules. First step towards separate
       compilation.

     * simple-list-traversal.r, spec/env-list-traversal.r: generic
       traversals in which lists are traversed by visiting head and tail,
       instead of visiting all elements (behaviour of all). Contributed by
       Otto Skrove Bagge.

     * fixpoint-traversal.r: innermost-tagged uses annotations to tag
       terms that are in normal form.

     * annotations.r: List of annotations. Additional operators for
       annotations: has-annotation, if-annotation, preserve-annotation
       (Martin Bravenboer) test in annotations-test.r

     * annotations-test.r: Contains an extensive set of unit tests describing
       the behaviour of annotations.

     * annotation-props.r: key/value pairs

     * config.r: Maintenance, import, and export of configuration
       information such as locations of executables and data files.

     * options.r: Use set-config to store option values in configuration
       table. Use <run-time> instead of dtime to measure time in iowrap.

     * time.r: support for time measurements extended with primitives calling
       the system calls clock and time. Module time defines a number of useful
       abstractions over this. In particular, <run-time> returns the seconds
       of total run-time so far, including the run-time of all child processes.
       The operator profile(msg, s) measures the time used to apply s and then
       prints user and system time, including children time.

     * dir.r: <readdir> d gives list of filenames of directory d

     * exec.r, Lower-level primitives for process control such as
       fork, exec, and pipe.

     * pipe.r: High-level combinations to connect to a child process via a
       pipe. (experimental)

    STRATEGO-CONNECT

     * This package provides an implementation of interprocess communication for
       Stratego. This package is experimental and not quite flushed
       out. There might be portability problems. Therefore, stratego-connect is
       not yet bundled in the main distribution.  The basic
       implementation was made by Hedzer Westra.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
