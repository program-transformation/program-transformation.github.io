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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease09?t=1536825503)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease09)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease09)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease09?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease09?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    39](http://www.program-transformation.org/view/Stratego/StrategoRelease09?rev=1.39)
    [(diff 38)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease09?rev1=1.39&rev2=1.38)
-   [Rev
    38](http://www.program-transformation.org/view/Stratego/StrategoRelease09?rev=1.38)
    [(diff 37)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease09?rev1=1.38&rev2=1.37)
-   [Rev
    37](http://www.program-transformation.org/view/Stratego/StrategoRelease09?rev=1.37)
    [(diff 36)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease09?rev1=1.37&rev2=1.36)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease09)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease09?template=oopsmore&param1=1.39&param2=1.39)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease09?template=oopsmore&param1=1.39&param2=1.39)
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
Stratego/XT 0.9 {#strategoxt-0.9 .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Stratego/XT 0.9 \-- released on January 26, 2003

[]{#Contents} Contents
----------------------

::: {.twikiToc}
-   [Contents](StrategoRelease09#Contents)
-   [Download](StrategoRelease09#Download)
    -   [Source distribution](StrategoRelease09#Source_distribution)
    -   [Binary distribution](StrategoRelease09#Binary_distribution)
    -   [CVS development
        snapshot](StrategoRelease09#CVS_development_snapshot)
-   [License](StrategoRelease09#License)
-   [Bugs](StrategoRelease09#Bugs)
-   [Dependencies](StrategoRelease09#Dependencies)
-   [Installation](StrategoRelease09#Installation)
-   [Packages](StrategoRelease09#Packages)
-   [Changes](StrategoRelease09#Changes)
-   [Previous Releases](StrategoRelease09#Previous_Releases)
-   [NEWS](StrategoRelease09#NEWS)
:::

[]{#Download} Download
----------------------

### []{#Source_distribution} Source distribution

[StrategoXT](StrategoXT){.twikiLink} is built using the
[ATermLibrary](ATermLibrary){.twikiLink}, the [SDF](SDF){.twikiLink}
syntax definition formalism and parser generator, and optionally the
Nancy Choice Point Library cpl (with some adaptations for Stratego).

-   [StrategoXT-0.9.tar.gz](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/StrategoXT-0.9.tar.gz)
-   [aterm-1.6.7.tar.gz](ftp://ftp.stratego-language.org/pub/stratego/aterm/aterm-1.6.7.tar.gz)
-   [sdf2-1.5.tar.gz](ftp://ftp.stratego-language.org/pub/stratego/sdf2/sdf2-1.5.tar.gz)
-   [cpl-stratego-0.4.tar.gz](ftp://ftp.stratego-language.org/pub/stratego/stratego/cpl-stratego-0.4.tar.gz)

### []{#Binary_distribution} Binary distribution

Binary distributions built on [RedHat](http://www.redhat.com) Linux 8.0

-   [StrategoXT-0.9-3.i386.rpm](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/StrategoXT-0.9-3.i386.rpm)
-   [aterm-1.6.7-2.i386.rpm](ftp://ftp.stratego-language.org/pub/stratego/aterm/aterm-1.6.7-2.i386.rpm)
-   [sdf2-1.5-2.i386.rpm](ftp://ftp.stratego-language.org/pub/stratego/sdf2/sdf2-1.5-2.i386.rpm)

Source RPMs

-   [StrategoXT-0.9-3.src.rpm](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/StrategoXT-0.9-3.src.rpm)
-   [aterm-1.6.7-2.src.rpm](ftp://ftp.stratego-language.org/pub/stratego/aterm/aterm-1.6.7-2.src.rpm)
-   [sdf2-1.5-2.src.rpm](ftp://ftp.stratego-language.org/pub/stratego/sdf2/sdf2-1.5-2.src.rpm)

### []{#CVS_development_snapshot} CVS development snapshot

After [Stratego Release 09](StrategoRelease09){.twikiLink} the sources
of the [StrategoXT](StrategoXT){.twikiLink} distribution have been moved
to a Subversion repository. See [Latest
Sources[^?^](http://www.program-transformation.org/edit/Stratego/LatestSources?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
style="background : #FFFFCE;"} for information on how to obtain the
latest developments (at your own risk).

[]{#License} License
--------------------

[StrategoXT](StrategoXT){.twikiLink} is free software; you can
redistribute it and/or modify it under the terms of the GNU Lesser
General Public License as published by the Free Software Foundation;
either version 2 of the License, or (at your option) any later version.

This software is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Lesser
General Public License for more details.

[]{#Bugs} Bugs
--------------

Please report any problems with installation or bugs in the
implementation to the
[stratego-bugs](https://mail.cs.uu.nl/mailman/listinfo/stratego-bugs)
mailing list. Please check the archive of the list to see if a report
about the problem was already submitted.

[]{#Dependencies} Dependencies
------------------------------

Besides the dependency on the aterm-1.6.7 and sdf2-1.5,
[StrategoXT](StrategoXT){.twikiLink} has the following dependencies:

The Stratego Compiler depends on

-   gcc (the extension of C with nested functions)

The build of the source distribution depends on the following software
packages

-   gmake

Developers who need to rebuild Makefiles and the configure scripts will
need

-   automake 1.6
-   autoconf 2.53

In addition the autoxt package that is part of the
[StrategoXT](StrategoXT){.twikiLink} distribution should be installed
prior to autobootstrapping such that the autoxt tool is visible from the
path.

[]{#Installation} Installation
------------------------------

The following sequence of commands takes care of building and installing
the aterm, sdf2, and [StrategoXT](StrategoXT){.twikiLink} packages from
source.

       DIR=`pwd`

       tar zxf aterm-1.6.7.tar.gz
       cd aterm-1.6.7
       ./configure --prefix=$DIR --with-all  
       make
       make install
       cd ..

       tar zxf sdf2-1.5.tar.gz
       cd sdf2-1.5
       ./configure --prefix=$DIR --with-aterm=$DIR
       make
       make install
       cd ..

       tar zxf StrategoXT-0.9.tar.gz
       cd StrategoXT-0.9
       ./configure --prefix=$DIR --with-aterm=$DIR --with-sdf=$DIR
       make
       cd ..

Optionally you can install the choice point library prior to
installation of [StrategoXT](StrategoXT){.twikiLink}:

       tar zxf cpl-stratego-0.4.tar.gz
       cd cpl-stratego-0.4
       ./configure --prefix=$DIR 
       make
       make install
       cd ..

To use the choice point library configure
[StrategoXT](StrategoXT){.twikiLink} as follows:

       ./configure --prefix=$DIR --with-aterm=$DIR --with-sdf=$DIR --with-cpl=$DIR 

[]{#Packages} Packages
----------------------

The [StrategoXT](StrategoXT){.twikiLink} distribution consists of the
following [StrategoXT Packages](StrategoXTPackages){.twikiLink}

-   [autoxt](AutoXT){.twikiLink} \-- autoconf/make support for packages
    using XT

<!-- -->

-   [srts[^?^](http://www.program-transformation.org/edit/Stratego/SRTS?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- Stratego run-time system

<!-- -->

-   [xtc](XTC){.twikiLink} \-- Transformation tool composition
    (component model)
-   sdf-import \-- [XTC](XTC){.twikiLink} registration of
    [SDF](SDF){.twikiLink} tools

<!-- -->

-   [stratego-front](StrategoFront){.twikiLink} \-- Stratego syntax and
    support for concrete object syntax
-   [sc[^?^](http://www.program-transformation.org/edit/Stratego/SC?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- Stratego compiler
-   [GPP](GPP){.twikiLink} \-- Pretty-printing tools based on box
-   [c-tools](CTools){.twikiLink} \-- Improved support for the
    generation of C code

<!-- -->

-   [ssl[^?^](http://www.program-transformation.org/edit/Stratego/SSL?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- Stratego Standard Library

<!-- -->

-   [aterm-tools](../Tools/ATermTools){.twikiLink} \-- Generic term
    operations
-   [asfix-tools](../Tools/AsFixTools){.twikiLink} \-- Operations on
    concrete syntax trees
-   [sdf-tools](../Tools/SdfTools){.twikiLink} \-- Transformations on
    syntax definitions
-   [stratego-tools](StrategoTools){.twikiLink} \-- Generation of
    Stratego code
-   [dot-tools[^?^](http://www.program-transformation.org/edit/Stratego/DotTools?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- Support for processing Dot graph
    representations
-   [graph-tools](../Tools/GraphTools){.twikiLink}

<!-- -->

-   boxenv \--
    [LaTeX[^?^](http://www.program-transformation.org/edit/Stratego/LaTeX?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
    style="background : #FFFFCE;"} run-time system for Box

<!-- -->

-   xt \-- some tool compositions

[]{#Changes} Changes
--------------------

-   [Fusion of Stratego and XT](FusionOfStrategoAndXT){.twikiLink}
-   [Stratego Run Time System](StrategoRunTimeSystem){.twikiLink}
-   [AutoXT](AutoXT){.twikiLink}
    -   [Upgrade to new Autotools](UpgradeToNewAutotools){.twikiLink}
    -   [Automake support for
        Stratego[^?^](http://www.program-transformation.org/edit/Stratego/AutomakeSupportForStratego?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Str
        extension[^?^](http://www.program-transformation.org/edit/Stratego/StrExtension?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Bootstrapped packages containing generated
        sources[^?^](http://www.program-transformation.org/edit/Stratego/BootstrappedPackagesContainingGeneratedSources?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
        style="background : #FFFFCE;"}
-   [XTC](XTC){.twikiLink} \-- [Transformation Tool
    Composition](TransformationToolComposition){.twikiLink}
-   Language/compiler
    -   [Retire Transform.YetAnotherCompilerCompiler
        Grammar[^?^](http://www.program-transformation.org/edit/Stratego/RetireTransformYetAnotherCompilerCompilerGrammar?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Character syntax](CharacterSyntax){.twikiLink}
    -   [Dynamic Rule Semantics](DynamicRuleSemantics){.twikiLink} \--
        Overlapping Left-Hand Sides bug
-   New packages
    -   [C Tools](CTools){.twikiLink}
-   [GPP](GPP){.twikiLink} refactored
-   Binary distributions

To do

-   [Distinguish build and use
    dependencies[^?^](http://www.program-transformation.org/edit/Stratego/DistinguishBuildAndUseDependencies?topicparent=Stratego.StrategoRelease09)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [Separate Compilation](SeparateCompilation){.twikiLink}

[]{#Previous_Releases} Previous Releases
----------------------------------------

Note that this wiki page is versioned. Pointers to earlier (beta)
releases can be found on earlier versions of this page. Not all beta
distributions are guaranteed to be available though.

-   [0.9beta10](http://www.stratego-language.org/twiki/bin/view/Stratego/StrategoRelease09?rev=1.31)
-   [0.9beta9](http://www.stratego-language.org/twiki/bin/view/Stratego/StrategoRelease09?rev=1.28)
-   [0.9beta8](http://www.stratego-language.org/twiki/bin/view/Stratego/StrategoRelease09?rev=1.22)
-   [0.9beta7](http://www.stratego-language.org/twiki/bin/view/Stratego/StrategoRelease09?rev=1.21)
-   [0.9beta6](http://www.stratego-language.org/twiki/bin/view/Stratego/StrategoRelease09?rev=1.16)
-   [0.9beta5](http://www.stratego-language.org/twiki/bin/view/Stratego/StrategoRelease09?rev=1.15)
-   [0.9beta3](http://www.stratego-language.org/twiki/bin/view/Stratego/StrategoRelease09?rev=1.13)
-   [0.9beta2](http://www.stratego-language.org/twiki/bin/view/Stratego/StrategoRelease09?rev=1.10)
-   [0.9beta1](http://www.stratego-language.org/twiki/bin/view/Stratego/StrategoRelease09?rev=1.7)
-   [StrategoDownload08](StrategoDownload08){.twikiLink}
-   [StrategoDownloadHistory](StrategoDownloadHistory){.twikiLink}

[]{#NEWS} NEWS
--------------

From the NEWS file

    StrategoXT 0.9 -- released January 26, 2003

    This release completely integrates concrete object syntax into
    Stratego. The extension of Stratego with concrete syntax implies a
    dependence of the compiler on several of the XT packages. Therefore,
    the new StrategoXT distribution integrates Stratego and XT. The parser
    for modules is now only based on SDF/SGLR; the LEX/YACC grammar has
    been retired. The XTC transformation tool composition framework
    provides a setting for easily creating transformation systems composed
    from transformation components.  The AutoXT package provides support
    for autoconf/make packages using the StrategoXT toolset. This has
    greatly simplified the configuration of the StrategoXT
    packages. Several new tools and libraries have been added, and
    existing packages have been refactored to use AutoXT and XTC. The
    distribution is available in binary form. Currently only in the form
    of RedHat 8.0 RPMs.

    DOWNLOAD AND INSTALLATION

      The download page contains the source distribution and instructions
      for installation

      * http://www.stratego-language.org/Stratego/StrategoRelease09

    SUMMARY OF CHANGES 

      * StrategoXT
        - XT CVS repository moved from CWI to UU
        - Merged XT and Stratego repositories
        - Single distribution for StrategoXT
        - Separate packages will also be available

      * AutoXT 
        - Autoconf/make support for XT packages
        - Building the distribution uses only the C compiler

      * SRTS
        - Complete run-time system for Stratego programs, including
          library primitives. After C generation, this package is
          all that is needed to compile a Stratego program.

      * XTC
        - Transformation tool composition
        - Sdf-import -- XTC registration of sdf tools

      * GPP
        - Refactoring of the package using XTC
        - A boxes supported by abox2text

      * STRATEGO-TOOLS
        - Format checker generation 

      * STRATEGO-FRONT
        - Support for ToBuild and FromApp to implement ASP style quotation

      * C-TOOLS
        - Support for C generation (and transformation)
        - Refactoring of the cgen package which is now obsolete
        
      * DOT-TOOLS 
        - Support for generation of dot files

      * SC
        - Bug in dynamic rules with overlapping left-hand sides fixed
        - LEX/YACC grammar retired; the compiler now depends on SDF
        - Stricter bound variables checking

      * SSL 
        - Parenthesize is a generic strategy for placing parentheses
          based on priority information. flatten-list completely flattens a list.
        - For-each-pair(s) produces the list of pairs <s>(x,y) for each pair 
          of x from xs and y from ys.
        - Execution of external processes (call) now defined in terms of primitives
          fork, wait and such

      * STRATEGO-TOOLS
        - Format checker generation 

      * SDF-TOOLS
        - Parse-unit is a tool for unit testing SDF definitions. 

      * SDF-IMPORT
        - The sdf-import package registers the SDF tools sdf2table and
          sglr in an XTC repository to make them available for XTC programs.

      * RPM
        - construction of binary distributions with rpm

      * Many bug fixes and refactorings

    BUGS / KNOWN PROBLEMS

      * The build of the StrategoXT package invokes 'make install' since the 
        installation of the libraries in srts are needed for the build of the
        rest of the package. This makes building of debian packages
        problematic. This problem will be addressed in future releases.

      * When bootstrapping the package from CVS it is necessary to install the
        autoxt package before calling the main 'bootstrap' script since that
        calls the autoxt tool.

    DETAILS

      Details about the changes since 0.8.1 can be found in the descriptions 
      of the 0.9beta releases in the NEWS file in the distribution. Further
      documentation can be found on the website.

    CONTRIBUTIONS

      * The StrategoXT-0.9 release involved a major refactoring of the
        stratego and XT packages and the introduction of several new
        packages. In particular, the introduction of XTC and AutoXT provide
        a significant improvement of the composition of tools and the
        configuration of packages. The production of the final release
        involved 10 beta releases.   

      * Bug reports and suggestions for improvements where submitted by: 

        Karina Olmos, Martin Bravenboer, Jonne van Wijngaarden, Lennart
        Swart, Alan van Dam, Jozef Kruger, Armijn Hemel, Eelco Dolstra,
        Julien LEMOINE, ChoJin, Akim Demaille

      * The major developments were carried out by 

        Eelco Visser, Martin Bravenboer

    ------------------------------------------------------------------------------

    Version 0.9beta10 - released January 12, 2003

    DOWNLOAD AND INSTALLATION

    The download page contains the source distribution and instructions
    for installation

      * http://www.stratego-language.org/Stratego/StrategoRelease09

    CHANGES with respect to 0.9beta9

      * SSL : parenthesize is a generic strategy for placing parentheses
        based on priority information. flatten-list completely flattens a list.

      * SRTS : intall header files for SSL primitives in
        PREFIX/include/srts instead of PREFIX/include/ssl to avoid conflicts
        with OpenSSL

      * XTC : 'xtc call prog' to call program prog relative to XTC repository,
        and 'xtc get file' to find location of file in XTC repository.

      * SC : started using concrete C syntax in s2c

      * AUTOXT/Makefile.xt : Register repository declared with XTC_IMPORT in
        a makefile

      * Use CFLAGS="-D__NO_CTYPE" in RPM build to allow portability to
        suse (hopefully)

    DOCUMENTATION

      * Reference Card 

        See http://www.stratego-language.org/Stratego/ReferenceCard for a
        data-flow diagram explaining the relation between many of the StrategoXT
        tools

    ------------------------------------------------------------------------------

    Version 0.9beta9 - released January 5, 2003

    DOWNLOAD AND INSTALLATION

    The download page contains the source distribution and instructions
    for installation

      * http://www.stratego-language.org/Stratego/StrategoRelease09

    SUMMARY OF CHANGES with respect to 0.9beta8

      * box-tools: a refactoring of gpp using xtc and improved Box support
      * stratego-tools: format checker generation
      * ssl: for-each-pair
      * sc: bugfixes
      * binary distribution with RPM (StrategoXT.spec)

    DETAILS

    * BOX-TOOLS (formerly GPP)
     
      Martin Bravenboer refactored the GPP package to use XTC
      and improved the functionality 

      * All tools are implemented in Stratego, shell-scripts
        are replaced by XTC tools.
      * important changes that might cause problems with 
        existing software:
          - verbose options are now all the standard Stratego
            options: --verbose int and -S. The -v argument has
            another meaning: the version of the tool will
            be shown.
          - Makefile to pretty print terms or parse pretty print
            tables is gone. You should use the new tools.
          - tohtml is not yet available as part of box-tools
      * gen-css-boxstyle: generate css for abox2html. 
        Uses standard -o argument to specify target. 
        abox2html -c just forwards to gen-css-boxstyle and
        also listens to the -o argument.
      * abox2text listens to width argument
      * abox2text supports HV boxes
      * abox2text now supports the HV and A/R boxes. The current
        implementation does not support R cells that will occupy 
        more than one line and must be aligned center or right.
        Left alignment should work. Single line cells works for
        all alginments.
      * new tools: pp-box, parse-box, parse-pp-table, pp-pp-table.
      * ast2abox accepts .pp.af pretty print tables as arguments.
        If you pass a .pp argument the tool will look for an
        existing .af version of this table and use this one if the
        .pp version is not newer. In all other cases the .pp table
        will be parsed to _temporary_ file.
      * grammars and pretty print tables of box and pp-tables are 
        separated.
      * abox-format doesn't complain about AOPTIONS.

    * STRATEGO-TOOLS

      format checker generation 

    * SSL
      - for-each-pair(s) produces the list of pairs <s>(x,y) for each pair 
        of x from xs and y from ys.

    * SC
      - bugfix in compilation of dynamic rules
      - sc: compilation without -o argument does the right thing again
      - pack-stratego: module searching faithful to path

    * RPM

      RPMs can be built using the 'make rpm' target. This requires
      the installation of rpms for aterm, sdf2, srts and xtc prior to
      building the rpm. RPMs for srts and xtc can be produced using
      the rpm targets in the srts/ and xtc/ directories.
      In order to install the StrategoXT rpm the srts and xtc rpms
      should be erased first.

    ------------------------------------------------------------------------------

    Version 0.9beta8 - released January 2, 2003

    DOWNLOAD AND INSTALLATION

    The download page contains the source distribution and instructions
    for installation

      * http://www.stratego-language.org/Stratego/StrategoRelease09

    SUMMARY OF CHANGES with respect to 0.9beta7

      * Bugfix: dynamic rules with overlapping left-hand sides 
      * XTC -- polishing
      * More tools based on XTC -- parse-stratego, sc, pack-stratego
      * C-Tools -- support for C generation (and transformation)
      * AutoXT -- support for recursive 
      * Bug fixes and refactorings

    DETAILS

    * Dynamic rules with overlapping left-hand sides 

      The desugaring of dynamic rules has been changed to repair the
      problems arising when two dynamic rules with the same name have
      different left-hand sides, but the same number of context variables
      in the left-hand side. The key that is used for a dynamic rule is
      now the entire left-hand side, modulo non-context variables. The
      new implementation will also make it easier to define (or even
      generate) operations for saving, restoring, and intersecting sets
      of dynamic rules, as used in data-flow optimizations.

    * XTC

      The XTC support library is further polished. The xtc-iowrap(s) strategy
      is the XTC variant of the traditional iowrap. It takes care of option 
      parsing, setting up the input file, and writing to the output file. The
      s strategy is typically a chain of xtc transformations. But it can also
      be used as replacement for iowrap, by wrapping xtc-io-transform(..) around
      a term transformation.

    * C-Tools

      The c-tools package is a refactoring of the cgen package for C code
      generation (by Martin Bravenboer). The package will replace cgen
      in future releases; it is not yet used within StrategoXT.

    * Using XTC

      The implementation of many composite tools is greatly simplified by
      using XTC. Configuration files are now obsolete, at least the import
      mechanism for configuration files. Any resources a component needs
      should be obtained through an XTC repository.

    * SDF Tools
      
      Parse-unit is a tool for unit testing SDF definitions. Contribution
      by Martin Bravenboer.

    * SSL / exec
       
      - fork-and-wait fails if the child returns with a non-zero exit
        status.

      - call definined in terms of fork and execvp in Stratego; previous
        implementation was complex C implementation. 

      - call(init-child) is like call, but applies init-child in the
        child process before the execvp
          
      - redirect-stdout-to-file and redirect-stdin-from-file do as their
        name suggest. They can be used with call(...) to redirect input
        and/or output of the child process. Using this files can be copied
        using the cat program as follows:
       
         cat :
           (filein, fileout) -> fileout
           where <call(<redirect-stdin-from-file> filein;
                  <redirect-stdout-to-file> fileout)> ("cat", [])

        Typical use of all this is to coerce programs that only read or
        write using stdio into using file io.

    * AutoXT

      Added support for recursive bootclean target to Makefile.xt. To use
      it Makefile.xt should be included in every Makefile.am in the
      directory structure. The subdirectories that should be bootcleaned
      should be declared in BOOTCLEAN_SUBDIRS variable. Leaf directories
      that don't use Makefile.xt should declare the target bootclean.

    * Bug fixes and refactorings

      While fixing bugs and adding functionality, the compiler components
      are gradually refactored to use more modern Stratego techniques.


    ------------------------------------------------------------------------------

    Version 0.9beta7 - released December 13, 2002

    DOWNLOAD AND INSTALLATION

    The download page contains the source distribution and instructions
    for installation

      * http://www.stratego-language.org/Stratego/StrategoRelease09

    SUMMARY OF CHANGES

      * AutoXT -- autoconf/make support for XT packages
      * XTC -- Transformation tool composition
      * Sdf-import -- XTC registration of sdf tools
      * Dot-tools -- syntax of the dot language

      * LEX/YACC grammar retired
      * All StrategoXT packages use autoxt
      * Building the distribution uses only the C compiler

    DETAILS

    * AutoXT
     
      The autoxt package provides autoconf and automake support for packages
      constructed with the XT toolset. The package provides the autoxt tool
      which should be run as part of the autoconf/make bootstrapping process,
      prior to running autoconf. A typical bootstrap script looks like:

      ------------------------------------------------ bootstrap
      #! /bin/sh
      autoxt
      aclocal -I .
      autoconf
      automake -a
      ------------------------------------------------

      Autoxt installs a set of m4 macros autoxt.m4 with support for
      package configuration switches. By just including the macro call
      USE_XT_PACKAGES a configure.in file can be parameterized with
      switches for all the StrategoXT packages:

      ------------------------------------------------ configure.in
      AC_INIT(syn/Dot.sdf)
      AM_INIT_AUTOMAKE(dot-tools,0.9beta7)
      USE_XT_PACKAGES
      AC_PROG_CC
      AC_PROG_INSTALL
      AC_OUTPUT(Makefile syn/Makefile)
      ------------------------------------------------

      Furthermore, autoxt installs Makefile.xt, a collection of automake
      rules for compiling Stratego programs and applying other XT tools,
      such as signature generation. Using this makefile, a makefile
      reduces to a declaration of programs to be compiled. The makefile
      automatically takes care of distributing the generated C code. The
      specification will only be compiled when it is newer than the C
      code. This means that packages using autoxt can be built using only
      the Stratego Run-Time System (srts).

      ------------------------------------------------ Makefile.am
      include $(top_srcdir)/Makefile.xt
      include $(wildcard *.dep)

      bin_PROGRAMS    = xtc
      pkgdata_DATA    = xtc-lib.rtree xtc-rep.rtree
      SCFLAGS         = --main $* $(XTCFLAGS)
      EXTRA_DIST      = $(wildcard *.str) $(wildcard *.meta)
      CLEANFILES      = $(wildcard *.dep)
      BOOTCLEANFILES  = xtc.c

      xtc.o           : xtc-conf.h
      ------------------------------------------------ 

    * XTC -- Transformation Tool Composition

      StrategoXT encourages a development model in which stand-alone
      components are developed for separate aspects of program
      transformation, instead of implementing integrated monolithic
      transformation systems. A typical component reads a program
      represented by means of an ATerm, transforms it, and writes out a
      transformed ATerm. The advantage of this approach is that the
      components can be reused in different transformation systems. The
      composition mechanisms used to date include makefiles, shell
      scripts, and Stratego programs. The problem with the approach is
      keeping track of all available components and their installation
      locations. As a consequence of making components available in small
      packages (to increase reusability), compositions need to be
      parameterized with a large number of installation paths. The XTC
      component model and API supports the easy composition of XT
      components using a repository to keep track of available components.

      XTC implements the XT component model and provides support for creating
      compositions of XT components. The xtc tool is used to register components
      in an XTC repository. For example the command:

        > xtc -r /usr/share/StrategoXT/XTC register -t sglr -l /bin -V 3.8
      
      registers version 3.8 of sglr which is installed in /bin in the XTC
      repository located in /usr/share/StrategoXT. The generic Makefile.xt
      provided by AutoXT automatically registers all installed tools with the
      package repository.

      XTC repositories can be used to find the installation location of a tool
      without needing to know all the installation paths. For example, the
      following query can be used to find out where sglr is installed:

        > xtc -r /usr/share/StrategoXT/XTC query -t sglr 
        sglr (3.8) : /bin/sglr

      An existing repository can be inherited by importing it

        > xtc -r /home/user/share/tiger/XTC import /usr/share/StrategoXT/XTC

      In addition to the command-line tool for registration and querying of
      repositories, XTC also provides a Stratego API for approaching XTC
      repositories. All that is required to use this API is (1) importing
      the xtc-lib module and (2) including an xtc-conf.h header file in
      the generated C code. The details are supported by Makefile.xt. 
      To use XTC add the following to your Makefile.am: 

      ------------------------------------------------ 
      bin_PROGRAMS  = term-to-dot
      SCFLAGS       = --main $* $(XTCFLAGS)
      term-to-dot.o : xtc-conf.h
      ------------------------------------------------ 

      The depedency of term-to-dot.o on xtc-conf.h is needed to ensure
      that it is generated. The xtc-conf.h header file contains the name
      of the XTC repository used by the package. 

      The XTC API supports easy calling of external Stratego components
      and mixing them with internally defined transformations. Here is an
      example:

      ------------------------------------------------ 
      module term-to-dot
      imports xtc-lib lib term-to-adot
      strategies
        term-to-dot =
          parse-options(term-to-adot-options <+ io-options)
          ; xtc-temp-files(
              (!FILE(<get-config> "-i") <+ !stdin)
              ; read-from
              ; to-adot
              ; write-to
              ; xtc-transform(!"ast2abox", !["-p", <xtc-find> "Dot-pretty.pp"])
              ; xtc-transform(!"abox2text")
              ; rename-to(<get-config> "-o"))
          ; <exit> 0
      ------------------------------------------------ 

      Note that no code is needed to load the repository. Whenever a query is
      done (e.g., by xtc-transform to find "ast2abox"), and no repository is
      loaded the XTC repository is loaded.

      AutoXT provides support for XTC by means of a package switch --with-repository
      that can be used to indicate the repository in which to register tools.
      The default is $prefix/share/$PACKAGE/XTC, i.e., the XTC file in the package
      data directory. In the StrategoXT distribution the sub-packages inherit the
      repository location from the super-package, i.e., all StrategoXT tools are
      registered in $prefix/share/StrategoXT/XTC.

      Makefile.xt implements an automake install hook to install all programs,
      scripts, and data. Thus it is not necessary to include make rules for
      this purpose. The Makefile example above is sufficient to register
      tools and data.

    * SDF-import

      The sdf-import package registers the SDF tools sdf2table and sglr in
      an XTC repository to make them available for XTC programs.

    * Dot-tools

      This package provides a refactored syntax definition of the Dot language,
      generated signature, pretty-printer, and Stratego embedding.

    * LEX/YACC Grammar Retired

      Since SDF is starting to be used structurally in the Stratego
      compiler, the LEX/YACC definition is no longer part of the distribution. It
      is a pain to maintain and to keep the two definitions in synch. 

    ------------------------------------------------------------------------------

    Version 0.9beta2

    SUMMARY OF CHANGES

      * StrategoXT
      * XT CVS repository from CWI to UU
      * Autotools

    CHANGES

    * XT CVS repository from CWI to UU

      Only Merijn, Joost, and I had access to the CVS repository at
      CWI. This was fine at first, but really hampered development in the
      last year or so. Now developers can get an account at the CVS server
      at UU to contribute directly to the source tree instead of via
      patches, which requires a lot of work from our side.

    * Autotools

      Akim Demaille pointed out that the use of autoconf and automake in
      Stratego and XT is antiquated, and badly needs to be updated to more
      modern versions of these tools. I had already encountered this
      problem when trying to build on a FreeBSD machine. The first fix is
      to renovate the current scripts and makefiles such that they will
      pass through newer versions of the autotools.

      This turned out not to be such a problem. The issues were:

      Automake enforces consistent usage of = and += 

      The AC_OUTPUT_SUBDIRS macro used in the Autobundle macro
      AB_CONFIG_PKG is no longer used. I found a simple fix for this
      problem using google. The fix defines the old style macro in terms
      of the new one, if it was not defined yet:

      ifdef([AC_OUTPUT_SUBDIRS],[],
        [AC_DEFUN([AC_OUTPUT_SUBDIRS],[subdirs=$1; _AC_OUTPUT_SUBDIRS])])

      (I noticed only later that Akim is one of the authors of the new
      autotools, and was pushing his own work;-)

      The 0.9beta1 release is generated using autoconf 2.53 and automake 1.5

    * StrategoXT

      The development of most Stratego applications involves tools from XT
      for parsing, imploding, pretty-printing, generating signatures, and
      so on. The introduction of concrete syntax in Stratego made this
      link even more important.  The slow development this year made it
      very hard to get a distribution of XT out with good support for
      concrete syntax. Since several of the XT tools are used in the
      compilation of .cr modules (implode-asfix in particular), and some
      others in the build of stratego-front, bootstrapping the compiler
      now involves these XT packages. In order to get a quick development
      and release cycle for Stratego, the XT packages should evolve at the
      same pace. (Recently some changes where needed to implode-asfix to
      support list variables used in list matching.)

      To make this easier I have merged the CVS repositories of Stratego
      and XT into a single new repository StrategoXT, which will also
      be the name of the distribution. There are a few changes with
      respect to the old XT bundle:

      - The repository itself has a main level package structure
        (inherited from Stratego). This makes it possible to build
        StrategoXT directly from the repository without having to go through
        autobundle. The sub-packages should still be distributed separately,
        and be subject to bundling in other packages, but development of
        StrategoXT should be smooth.

      - External packages (aterm, sdf, cpl-stratego) have been factored
        out since they are, well, external, and relatively stable with
        respect to StrategoXT development. In this way we can develop
        StrategoXT against a stable baseline of aterm and sdf2, and 
        every now and then upgrade to newer versions.

      - A separate bundle for sdf2-1.5 is available from the stratego site

      - The grammar base has been factored out of the bundle since
        development and distribution of grammars should not be directed
        by tool distribution. Grammars evolve much faster 

      - Application packages such as autobundle have been factored out,
        since they are, well, applications. I propose to create a new
        repository xtapp (better name?) in which such packages live
        as modules. (There exists already a repository sp [stratego
        projects] with projects such as tiger.)

      - Grammar-recovery is not included presently; should it be?

      - Version numbering: I have promoted all packages to the Stratego
        numbering scheme, except for the packages such as gpp, which
        were already past 1.0. I don't know what to do about that
        yet.

    ------------------------------------------------------------------------------

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
