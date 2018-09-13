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
    Page](http://www.program-transformation.org/edit/Stratego/HowToSetUpAStrategoPackage?t=1536825586)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/HowToSetUpAStrategoPackage)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/HowToSetUpAStrategoPackage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/HowToSetUpAStrategoPackage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/HowToSetUpAStrategoPackage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    15](http://www.program-transformation.org/view/Stratego/HowToSetUpAStrategoPackage?rev=1.15)
    [(diff 14)](http://www.program-transformation.org/rdiff/Stratego/HowToSetUpAStrategoPackage?rev1=1.15&rev2=1.14)
-   [Rev
    14](http://www.program-transformation.org/view/Stratego/HowToSetUpAStrategoPackage?rev=1.14)
    [(diff 13)](http://www.program-transformation.org/rdiff/Stratego/HowToSetUpAStrategoPackage?rev1=1.14&rev2=1.13)
-   [Rev
    13](http://www.program-transformation.org/view/Stratego/HowToSetUpAStrategoPackage?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Stratego/HowToSetUpAStrategoPackage?rev1=1.13&rev2=1.12)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/HowToSetUpAStrategoPackage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/HowToSetUpAStrategoPackage?template=oopsmore&param1=1.15&param2=1.15)
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
    \...](http://www.program-transformation.org/oops/Stratego/HowToSetUpAStrategoPackage?template=oopsmore&param1=1.15&param2=1.15)
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
How To Set Up AStratego Package {#how-to-set-up-astratego-package .twikiTopicTitle}
===============================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

\[under construction \-- [EelcoVisser](../Main/EelcoVisser){.twikiLink}
- 16 May 2003\]

A full fledged Stratego application does more than transform an ATerm
into another ATerm. To transform programs it is necessary to parse the
input program, turn the [parse tree](../Transform/ParseTree){.twikiLink}
into a an [abstract syntax tree](AbstractSyntaxTree){.twikiLink}, apply
several transformations, and [pretty
print[^?^](http://www.program-transformation.org/edit/Stratego/PrettyPrint?topicparent=Stratego.HowToSetUpAStrategoPackage)]{.twikiNewLink
style="background : #FFFFCE;"} the output program. These separate
operations should also be glued together into a complete transformation
system. The [StrategoXT](StrategoXT){.twikiLink} tools support the
creation and composition of components for all aspects of transformation
systems. Since the tool set is very flexible and programmable, there are
many possibilities for using it.

This page provides a guideline for setting up a typical [Stratego
application](StrategoApplication){.twikiLink}. The application is
developed as a package under the control of
[AutoMake[^?^](http://www.program-transformation.org/edit/Tools/AutoMake?topicparent=Stratego.HowToSetUpAStrategoPackage)]{.twikiNewLink
style="background : #FFFFCE;"} and
[AutoConf[^?^](http://www.program-transformation.org/edit/Tools/AutoConf?topicparent=Stratego.HowToSetUpAStrategoPackage)]{.twikiNewLink
style="background : #FFFFCE;"} using the [AutoXT](AutoXT){.twikiLink}
abstractions developed for [StrategoXT](StrategoXT){.twikiLink}.

As an example we examine the [prolog-tools](PrologTools){.twikiLink}
package, which provides basic support for transforming Prolog programs.

::: {.twikiToc}
-   [Structure of the
    Package](HowToSetUpAStrategoPackage#Structure_of_the_Package)
-   [Configuration](HowToSetUpAStrategoPackage#Configuration)
    -   [Configure.in](HowToSetUpAStrategoPackage#Configure_in)
    -   [bootstrap](HowToSetUpAStrategoPackage#bootstrap)
    -   [Makefile.am](HowToSetUpAStrategoPackage#Makefile_am)
    -   [Other Required
        Files](HowToSetUpAStrategoPackage#Other_Required_Files)
    -   [Configuring the
        Package](HowToSetUpAStrategoPackage#Configuring_the_Package)
-   [Syntax Definition
    (syn)](HowToSetUpAStrategoPackage#Syntax_Definition_syn)
-   [Signature (sig)](HowToSetUpAStrategoPackage#Signature_sig)
-   [Pretty-Printer (pp)](HowToSetUpAStrategoPackage#Pretty_Printer_pp)
-   [Tool Composition
    (xtc)](HowToSetUpAStrategoPackage#Tool_Composition_xtc)
-   [Tests (tests)](HowToSetUpAStrategoPackage#Tests_tests)
:::

[]{#Structure_of_the_Package} Structure of the Package
------------------------------------------------------

A source-to-source transformation system consists of a parser, several
transformation components, and a pretty-printer. These components are
specified in subdirectories of the package. The following directories
are standard in a package providing support for one or more languages:

-   [syn](https://svn.strategoxt.org/repos/StrategoXT/trunk/prolog-tools/syn)
    \-- syntax definitions
-   [sig](https://svn.strategoxt.org/repos/StrategoXT/trunk/prolog-tools/sig)
    \-- signatures describing abstract syntax trees
-   [pp](https://svn.strategoxt.org/repos/StrategoXT/trunk/prolog-tools/pp)
    \-- pretty-print tables
-   [xtc](https://svn.strategoxt.org/repos/StrategoXT/trunk/prolog-tools/xtc)
    \-- tool compositions
-   [tests](https://svn.strategoxt.org/repos/StrategoXT/trunk/prolog-tools/tests)
    \-- unit and integration tests

In addition a package can contain several directories for transformation
componens.

[]{#Configuration} Configuration
--------------------------------

It is customary to develop Stratego packages using the
[AutoMake[^?^](http://www.program-transformation.org/edit/Tools/AutoMake?topicparent=Stratego.HowToSetUpAStrategoPackage)]{.twikiNewLink
style="background : #FFFFCE;"} and
[AutoConf[^?^](http://www.program-transformation.org/edit/Tools/AutoConf?topicparent=Stratego.HowToSetUpAStrategoPackage)]{.twikiNewLink
style="background : #FFFFCE;"} in order to make packages easiliy
portable to many (Unix compatible) platforms. If you are not familiar
with these tools please check out their documentation.

### []{#Configure_in} Configure.in

From the `configure.in` file, the build-time `configure` script is
generated. It takes configuration parameters such as external packages
and substitutes them in makefiles and other source files. The
`USE_XT_PACKAGES` macro can be used in order to get parameterization of
the [StrategoXT packages](StrategoXTPackages){.twikiLink}.

<https://svn.strategoxt.org/repos/StrategoXT/prolog-tools/trunk/configure.in>

    ---------------------------------
     __Note:__  Included topic [[https:..svn.strategoxt.org.repos.StrategoXT.prolog-tools.trunk.configure.in]] does not exist yet
    ---------------------------------

### []{#bootstrap} bootstrap

In order to generate the `configure` script and instantiate the makefile
templates several tools from the autoX family should be applied. The
`bootstrap` script calls these tools in the right order. One unusual
tool is [autoxt](AutoXT){.twikiLink}, which installs
[AutoMake[^?^](http://www.program-transformation.org/edit/Tools/AutoMake?topicparent=Stratego.HowToSetUpAStrategoPackage)]{.twikiNewLink
style="background : #FFFFCE;"} macros supporting the use of
[StrategoXT](StrategoXT){.twikiLink} tools. The `bootstrap` script
assumes that `autoxt` can be found in the path.

    ---------------------------------
     __Note:__  Included topic [[https:..svn.strategoxt.org.repos.StrategoXT.prolog-tools.trunk.bootstrap]] does not exist yet
    ---------------------------------

### []{#Makefile_am} Makefile.am

Each directory in the package should have a `Makefile`. These
`Makefiles` are generated by automake and autoconf from a declarative
`Makefile.am`. The top-level Makefile just declares its subdirectory
such that navigation code can be generated. The `Makefile.xt` is
installed by `autoxt` and contains standard make rules for applying
[StrategoXT](StrategoXT){.twikiLink} tools. It should be included in
each makefile in the package.

    ---------------------------------
     __Note:__  Included topic [[https:..svn.strategoxt.org.repos.StrategoXT.prolog-tools.trunk.Makefile.am]] does not exist yet
    ---------------------------------

The `AC_CONFIG_FILES` macro defines all files that should be created by
`configure`.

### []{#Other_Required_Files} Other Required Files

Automake/conf require the following files to exist in the package:

-   [README](https://svn.strategoxt.org/repos/StrategoXT/prolog-tools/trunk/README)
    \-- name and purpose of the package
-   [AUTHORS](https://svn.strategoxt.org/repos/StrategoXT/prolog-tools/trunk/AUTHORS)
-   [ChangeLog](https://svn.strategoxt.org/repos/StrategoXT/prolog-tools/trunk/ChangeLog)
    \-- fine grained log of changes
-   [NEWS](https://svn.strategoxt.org/repos/StrategoXT/prolog-tools/trunk/NEWS)
    \-- course grained description of changes

### []{#Configuring_the_Package} Configuring the Package

Once the basic configuration is set up you can configure the package
with the following sequence of commands:

       > ./bootstrap
       > ./configure  --prefix=/installation/directory  --with-xt=/usr

Assuming that the [StrategoXT](StrategoXT){.twikiLink}, ATerm, and
[SDF](SDF){.twikiLink} distributions have been installed in `/usr`. Now
it should be possible to `make` and `install` the components in the
package using the commands:

       > make
       > make install

Exported components are installed in subdirectories of the
`/installation/directory`.

[]{#Syntax_Definition_syn}[]{#Syntax_Definition_syn_} Syntax Definition (syn)
-----------------------------------------------------------------------------

The syntax definition of the language under consideration (Prolog in
this case) is defined in directory `syn/`. The directory contains the
following files:

-   [Prolog.sdf](https://svn.strategoxt.org/repos/StrategoXT/trunk/prolog-tools/syn/Prolog.sdf)
    \-- syntax definition of Prolog
-   [Stratego-Prolog.sdf](https://svn.strategoxt.org/repos/StrategoXT/trunk/prolog-tools/syn/Stratego-Prolog.sdf)
    \-- embedding of Prolog in Stratego for use of concrete Prolog
    syntax in Stratego
-   [sicstus\_45.html](https://svn.strategoxt.org/repos/StrategoXT/trunk/prolog-tools/syn/sicstus_45.html)
    \-- informal definition of Prolog syntax

The `Makefile.am` defines which parse tables to make (`.tbl` extension):

    ---------------------------------
     __Note:__  Included topic [[https:..svn.strategoxt.org.repos.StrategoXT.prolog-tools.trunk.syn.Makefile.am]] does not exist yet
    ---------------------------------

[]{#Signature_sig}[]{#Signature_sig_} Signature (sig)
-----------------------------------------------------

The [algebraic signature](AlgebraicSignature){.twikiLink} defines the
[abstract syntax](AbstractSyntax){.twikiLink} of a language. The
signature of Prolog abstract syntax is defined in the `Prolog.str`:

-   [Prolog.str](https://svn.strategoxt.org/repos/StrategoXT/trunk/prolog-tools/sig/Prolog.str)
    \-- signature of Prolog abstract syntax

The signature can be derived automatically from a syntax definition
using the tool `sdf-to-sig`. The make rules in `Makefile.xt` invoke this
tool based on the dependency of `.str` files on `.def` files. The
`Prolog.def` file is made available via a symbolic link to the `../syn/`
directory.

    ---------------------------------
     __Note:__  Included topic [[https:..svn.strategoxt.org.repos.StrategoXT.prolog-tools.trunk.sig.Makefile.am]] does not exist yet
    ---------------------------------

[]{#Pretty_Printer_pp}[]{#Pretty_Printer_pp_} Pretty-Printer (pp)
-----------------------------------------------------------------

A pretty-printer renders an abstract syntax tree as text. The
[GPP](../Tools/GenericPrettyPrinter){.twikiLink} package in
[StrategoXT](StrategoXT){.twikiLink} provides tools for rendering ASTs
as ascii text, html, and latex. The translation works by first
translating an AST to a Box term, which declares formatting
independently of the target device *and* the source language. A Box can
be formatted in different ways. The translation from AST to Box can be
done in two ways. [GPP](GPP){.twikiLink} supports
[pp-tables](../Tools/PrettyPrintTable){.twikiLink} which define a
mapping from AST constructors to Box terms. The
[pp-gen[^?^](http://www.program-transformation.org/edit/Tools/PrettyPrintTableGenerator?topicparent=Stratego.HowToSetUpAStrategoPackage)]{.twikiNewLink
style="background : #FFFFCE;"} tool generates a default pp-table from a
syntax definition. Alternatively one can program the translation from
AST to Box in a Stratego program. Although the latter is more work, it
may be necessary when more sophisticated formatting is required. The
Prolog package uses both methods.

-   [Prolog.pp](https://svn.strategoxt.org/repos/StrategoXT/prolog-tools/trunk/pp/Prolog.pp)
    \-- default pretty-print table for Prolog
-   [Prolog2abox.str](https://svn.strategoxt.org/repos/StrategoXT/prolog-tools/trunk/pp/Prolog.pp)
    \-- Stratego transformation from Prolog abstract syntax to Box

<!-- -->

    ---------------------------------
     __Note:__  Included topic [[https:..svn.strategoxt.org.repos.StrategoXT.prolog-tools.trunk.pp.Makefile.am]] does not exist yet
    ---------------------------------

[]{#Tool_Composition_xtc}[]{#Tool_Composition_xtc_} Tool Composition (xtc)
--------------------------------------------------------------------------

    ---------------------------------
     __Note:__  Included topic [[https:..svn.strategoxt.org.repos.StrategoXT.prolog-tools.trunk.xtc.Makefile.am]] does not exist yet
    ---------------------------------

[]{#Tests_tests}[]{#Tests_tests_} Tests (tests)
-----------------------------------------------

    ---------------------------------
     __Note:__  Included topic [[https:..svn.strategoxt.org.repos.StrategoXT.prolog-tools.trunk.tests.Makefile.am]] does not exist yet
    ---------------------------------

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
