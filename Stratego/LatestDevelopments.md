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
    Page](http://www.program-transformation.org/edit/Stratego/LatestDevelopments?t=1536825368)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/LatestDevelopments)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/LatestDevelopments)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/LatestDevelopments?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/LatestDevelopments?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    13](http://www.program-transformation.org/view/Stratego/LatestDevelopments?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Stratego/LatestDevelopments?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Stratego/LatestDevelopments?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Stratego/LatestDevelopments?rev1=1.12&rev2=1.11)
-   [Rev
    11](http://www.program-transformation.org/view/Stratego/LatestDevelopments?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Stratego/LatestDevelopments?rev1=1.11&rev2=1.10)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/LatestDevelopments)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/LatestDevelopments?template=oopsmore&param1=1.13&param2=1.13)
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
    \...](http://www.program-transformation.org/oops/Stratego/LatestDevelopments?template=oopsmore&param1=1.13&param2=1.13)
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
Latest Developments {#latest-developments .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.newsitem}
*2013-10-05*

### []{#FTP_available_via_HTTP} FTP available via HTTP

All the material of the ftp directory of strategoxt.org, including all
historic releases of Stratego and Stratego/XT are now also available via
HTTP:

<http://ftp.strategoxt.org/>
:::

::: {.newsitem}
[]{#1.1}

### []{#Spoofax_1_1_released} Spoofax 1.1 released

We are happy to announce the release of Spoofax 1.1! This is the first
major release since version 1.0.2 and includes major features and
improvements. Spoofax 1.1 supports all current Eclipse versions, up to
version 4.2.2.

You can update your Eclipse from
<http://download.spoofax.org/update/stable>

One of the most important improvements in Spoofax 1.1 is the inclusion
of [NaBL](../Spoofax/NaBL){.twikiLink}, the Spoofax Name Binding
Language. [NaBL](../Spoofax/NaBL){.twikiLink} is used in all new
projects created and significantly simplifies name binding analysis, as
well as any editor services that depend on it (e.g., code completion,
reference resolving)

[NaBL](../Spoofax/NaBL){.twikiLink} is documented at the following
pages:

-   Tutorial <http://metaborg.org/wiki/nabl>
-   Examples <http://metaborg.org/wiki/nabl/examples>
-   Research paper <http://researchr.org/publication/KonatKWV13>

Other highlights of the 1.1 release include:

-   Improved build process: generated files can be deleted, building &
    loading are separated, projects can be cleaned
    (<http://yellowgrass.org/issue/Spoofax/577>,
    <http://yellowgrass.org/issue/Spoofax/591>,
    <http://yellowgrass.org/issue/Spoofax/578>)
-   Improved Stratego editor with multi-file reference resolving based
    on [NaBL](../Spoofax/NaBL){.twikiLink}
    (<http://yellowgrass.org/issue/Spoofax/12>)
-   Extended support for customizing refactoring UI
    (<http://yellowgrass.org/issue/Spoofax/440>)
-   Automatic configuration of git/svn ignore settings
    (<http://yellowgrass.org/issue/Spoofax/573>)
-   Added support loading for Java-based plugin dependencies, in case
    your plugin depends on some other plugin such as EMF
    (<http://yellowgrass.org/issue/Spoofax/322>)

And there were a number of notable changes under the hood:

-   Much improved completion engine
    (<http://yellowgrass.org/issue/Spoofax/360>)
-   We now show a nice warning if Eclipse is not configured with a
    proper stack and heap size
    (<http://yellowgrass.org/issue/Spoofax/86>)
-   Files are now queued for re-analysis even if their editor is not
    open (<http://yellowgrass.org/issue/Spoofax/224>)

A comprehensive list of changes can be viewed at
<http://yellowgrass.org/tag/Spoofax/1.1>.

*2013-01-28*

### []{#Spoofax_QA} Spoofax Q&A

We have started a Q&A site for Spoofax to build a knowledge base of
common questions and answers. Join us at
<http://yellowgrass.org/questions/Spoofax>

[]{#1.0.2} *2012-02-15*

### []{#Spoofax_1_0_2_maintenance_releas} Spoofax 1.0.2 maintenance release

Today we\'re releasing a minor maintenance release of Spoofax, version
1.0.2. This release fixes a memory leak that was introduced in the 1.0
release. There are no new features in this release, those will be
included in the upcoming 1.1 release instead. The new version is now
available from the update site at `http://spoofax.org/update/stable`.

[]{#1.0}

::: {.newsitem}
*2011-12-28*

### []{#Spoofax_1_0} Spoofax 1.0

We\'re pleased to announce the release of Spoofax 1.0. A number of
significant new features have been added since the last stable release,
a long list of bugs has been fixed, and various minor improvements were
introduced.

Highlights of the release include:

-   Support for [writing tests for language
    definitions](../Spoofax/Testing){.twikiLink}
-   Support for [defining
    refactorings](../Spoofax/Refactorings){.twikiLink}
-   Major improvements to content completion:
    [Spoofax/289](http://yellowgrass.org/issue/Spoofax/289),
    [Spoofax/357](http://yellowgrass.org/issue/Spoofax/357)
-   Support for using rewrite rules to disambiguate syntax:
    [Spoofax/328](http://yellowgrass.org/issue/Spoofax/328)

The new version is now available from the update site at
`http://spoofax.org/update/stable`.

In addition to these features, we\'re actively working on improving
Spoofax with new features. In particular, we are now working on
providing full support for debugging, on an interactive shell for
Stratego and custom languages, and a new meta-language called
SpoofaxLang to define languages in a more modular fashion.

A full list of feature requests and issues addressed in the new version
is provided at <http://yellowgrass.org/tag/Spoofax/1.0>.
:::

::: {.newsitem}
*2010-05-28*

### []{#Introducing_the_Spoofax_Language} Introducing the Spoofax Language Workbench

[![Installation](http://strategoxt.org/pub/Spoofax/WebHome/eclipse_logo_white-300x174.jpg "Install in Eclipse"){width="150"
height="87"}](http://www.program-transformation.org/Stratego/Download)

We\'re pleased to announce the 0.5 release of the [Spoofax language
workbench](../Spoofax/WebHome){.twikiLink}, an Eclipse plugin that
seamlessly integrates Java versions of Stratego and SDF into Eclipse.
Spoofax can be used to develop new languages and transformations based
on SDF and Stratego in the Eclipse environment. Read on below and be
sure to follow our [tour with screenshots](../Spoofax/Tour){.twikiLink}
for more information.

##### []{#Stratego_and_SDF_for_Java} Stratego and SDF for Java

Stratego and SDF have traditonally been implemented using C, but to
increase portability we have developed Java versions of the [Stratego
compiler](STRJ){.twikiLink} and [the JSGLR parser for
SDF](JSGLR){.twikiLink}. These new implementations are seamlessly
integrated into the Spoofax environment, but can also be used as
stand-alone tools.

##### []{#Building_programming_languages_w} Building programming languages with IDE support

IDE support has become essential for developers to be productive with
programming languages. Spoofax provides IDE support for Stratego and SDF
for developers of languages and transformations. It also aids in the
development of IDE support for new languages: from the first version of
an SDF grammar, an editor can be created for the language and used
[side-by-side](../Spoofax/Features){.twikiLink} with the definition in
Eclipse. Using Stratego, the editor can be enhanced with transformations
and semantic editor services such as reference resolving and content
completion.

The screenshot below illustrates some of the IDE features supported by
editors created with Spoofax (click to enlarge):

[![Spoofax editor
features](http://strategoxt.org/pub/Spoofax/Features/screenshot-annotated-smaller-2.png){width="460"
height="249"}](http://strategoxt.org/pub/Spoofax/Features/screenshot-annotated-small.png)

##### []{#More_information} More information

Spoofax can be downloaded from [spoofax.org](http://www.spoofax.org) or
[strategoxt.org/Spoofax](http://www.strategoxt.org/Spoofax). When
installed in Eclipse, the plugin provides a \"New project\" wizard that
creates a new skeleton project illustrating some of the Spoofax
features. The website also includes a
[tour](../Spoofax/Tour){.twikiLink} further showcasing the features of
the workbench. For migrating C-based Stratego projects to Spoofax,
please read our [FAQ](http://strategoxt.org/Spoofax/FAQ) or contact us
in case of other questions.

An overview of the architecture of Spoofax and how Spoofax can be used
in the development of new languages and IDE services is given in the
paper [The Spoofax Language Workbench. Rules for Declarative
Specification of Languages and
IDEs](http://researchr.org/publication/KatsVisser2010) by Lennart Kats
and Eelco Visser, accepted for publication at [SPLASH/OOPSLA
2010](http://www.splashcon.org/). Further documentation can be found on
the Spoofax website.

::: {.newsitem}
*2008-05-24*

### []{#Stack_traces_on_rewriting_failed} Stack traces on \"rewriting failed\"

Since late March, the Stratego compiler and auxiliary libraries have
supported stack traces upon rewriting failed. The following trace is
taken from a typical [XTC](XTC){.twikiLink} component that uses
`io-wrap`:

    ./prog: rewriting failed, trace:
            main_0_0
            io_wrap_1_0
            option_wrap_5_0
            lifted144
            input_1_0
            lifted145
            output_1_0
            lifted0
            my_wrap_1_0
            foo_0_0
            bar_0_0
            zap_0_0

More details may be found in
[two](http://journal.boblycat.org/node/2937)
[posts](http://journal.boblycat.org/node/2934) to our planet.
:::

::: {.newsitem}
*2008-04-24*

### []{#New_URLs_for_Subversion_Releases} New URLs for Subversion, Releases, and Bug-tracking

All the Stratego/XT development tools have been moved to subdomains of
[strategoxt.org](http://strategoxt.org). An overview:

-   At <https://svn.strategoxt.org> you can find the Stratego/XT
    Subversion server. Please let us know if there are still old
    svn.cs.uu.nl URLs around somewhere. If you want to relocate your
    checkout, run
    `svn switch --relocate https://svn.cs.uu.nl:12443 https://svn.strategoxt.org`.
-   At <http://releases.strategoxt.org> you can find releases of
    Stratego/XT and its extensions. Most of the URLs on the website have
    been updated to point to this website. If you still have Nix
    channels subscriptions for the old buildfarm, please update!
-   At <http://bugs.strategoxt.org> we now host our issue tracking
    system.

Thanks to Eelco Dolstra for doing most of this work!
:::

::: {.newsitem}
*2007-04-26*

### []{#Global_Variables} Global Variables

Stratego now supports **scoped** global variables. In the context of a
dynamic rules section one can now write

        rules( Foo := <compute> )

which abbreviates the following commonly used programming pattern:

        x := <compute>
        ; rules( Foo : _ -> x )

The value bound in the assignment can be retrieved by the application
\<Foo\>. The usual scoping features of dynamic rules apply to global
variable as well. For more information see this
[blog](http://blog.eelcovisser.net/index.php?/archives/53-Global-Variables.html).
:::

::: {.newsitem}
*2007-04-03*

### []{#AspectJ_front_revived_support_fo} AspectJ-front revived, support for Microsoft Windows

The [AspectJ-front](AspectJFront){.twikiLink} package has been updated
to be easier to install and be more portable. The AspectJ syntax
definition of AspectJ-front heavily exercises the [SDF](SDF){.twikiLink}
parser generator, which used to make it rather difficult to install the
package on machines with a limited amount of memory. The new packages
includes the compiled parse tables and also the package is more
portable, including support for native Microsoft Windows! The package
now also provides a library (DLL on Microsoft Windows) for parsing and
pretty-printing AspectJ source files.
:::

::: {.newsitem}
*2007-03-01*

### []{#x86_64_support_for_Stratego_XT}[]{#x86_64_support_for_Stratego_XT_} x86-64 support for Stratego/XT!

Stratego/XT supports x86-64 processors (in 64-bit mode) from release
[0.17M3pre16744](http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt/strategoxt-0.17M3pre16744/)
([or
later](http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt/strategoxt-unstable-latest/)),
the sdf2-bundle from release
[2.4pre212034](http://buildfarm.st.ewi.tudelft.nl/releases/meta-environment/sdf2-bundle-2.4pre212034-sqzzbkp3/)
([or
later](http://buildfarm.st.ewi.tudelft.nl/releases/meta-environment/sdf2-bundle-unstable-latest/)).
The preliminary releases are available from our new [Nix buildfarm at
the TU Delft](http://buildfarm.st.ewi.tudelft.nl/releases). The x86-64
support is based on a branch of the ATerm library developed by Eelco
Dolstra and Erik Scheffers, and some new 64-bit patches for the
sdf2-bundle. The x86-64 bit requirements are completely hidden in the
ATerm library and the Auto/XT build system, thus packages based on
Stratego/XT should support x86-64 machines out of the box if they do not
contain custom native C code. The preliminary releases with 64-bit
support will soon be used in the Stratego/XT packages [integration
build](IntegrationBuild){.twikiLink}, which currently still refers to
the [Nix Buildfarm at Utrecht University](http://nix.cs.uu.nl/dist/).
More information about the issues and the specific patches required for
x86-64 support is available in a
[post](http://mbravenboer.blogspot.com/2007/03/x86-64-support-for-strategoxt.html)
at [Subject to Meta Programming](http://mbravenboer.blogspot.com).
:::

::: {.newsitem}
*2007-01-18*

### []{#Stratego_XT_Packages_Channel} Stratego/XT Packages Channel

The Stratego/XT packages channel now provides [integration
builds](IntegrationBuild){.twikiLink} for Stratego/XT, its dependencies,
and packages based on Stratego/XT. We have created this channel after
frequent questions about which packages work together. From now on, this
is the way to install the latest developments of Stratego/XT. If you
install packages from this channel, then they are guaranteed to work
together. If your favorite Stratego/XT package is currently not on the
channel, just send us a request. If the package is maintained and in
reasonable use, then we will add it to the channel.
:::

::: {.newsitem}
*2006-08-20*

### []{#New_Translation_Scheme} New Translation Scheme

By a [new translation
scheme](http://eelcovisser.blogspot.com/2006/08/getting-rid-of-nested-functions.html)
in the back-end of the Stratego compiler, the dependency on nested
functions in gcc has been eliminated. The compiler now produces ANSI C
compliant code, increasing the portability of Stratego code in terms of
compilers and platforms.
:::

::: {.newsitem}
*2006-06-05*

### []{#Support_for_Mac_OSX_Intel} Support for Mac OSX / Intel

[Announced](http://mail.cs.uu.nl/pipermail/stratego-dev/2006q2/001135.html)
support for Mac/Intel machines in the the latest unstable releases,
including an installer.
:::

::: {.newsitem}
*2005-11-04*

### []{#Stratego_XT_Manual} Stratego/XT Manual

The first Stratego/XT Manual has been released with [tutorial, examples,
and reference material](StrategoDocumentation){.twikiLink}.
:::

::: {.newsitem}
*2005-11-04*

### []{#Stratego_XT_0_16} Stratego/XT 0.16

[Stratego/XT 0.16](StrategoRelease016){.twikiLink} has been released.
This release introduces a major refactoring of the Stratego Language and
compiler. Furthermore, many outstanding issues have been addressed, and
we have a manual!
:::

::: {.newsitem}
*2005-11-04*

### []{#Stratego_Shell_0_6} Stratego Shell 0.6

[Stratego Shell 0.6](StrategoShellRelease06){.twikiLink} has been
released. This release features a major reimplementation of the
interpreter and compatability with the Stratego Core language introduced
in [Stratego/XT 0.16](StrategoRelease016){.twikiLink}.
:::

::: {.newsitem}
*2005-11-04*

### []{#BibTex_Tools_0_2} BibTex Tools 0.2

[BibTex Tools 0.2](BibtexToolsRelease02){.twikiLink} is the first
official release of the Stratego/XT [BibTeX
Tools](BibtexTools){.twikiLink} package, which provides components for
processing BibTeX files, mainly for producing publication lists.
:::

::: {.newsitem}
*2005-11-04*

### []{#Java_front_0_8} Java-front 0.8

[Java-front 0.8](JavaFrontRelease08){.twikiLink} has been released. This
is a major update, fixing some usability issues in parse-java, improving
the support for compilation the command-line, and fixes in the
pretty-printer.
:::

**2005-08-31** [Stratego/XT 0.16M1](StrategoRelease016M1){.twikiLink}
has been released. This releases features a redesign of the Stratego
compiler, e.g. a new compilation scheme which should give a huge
performance boost on Mac OS X machines.

**2005-07-05** [Stratego/XT 0.15](StrategoRelease015){.twikiLink} is now
available. It is an experimental release featuring a major refactoring
of the internal representation of Stratego and the Stratego compiler.

**2005-05-24** [Java-front 0.7](JavaFrontRelease07){.twikiLink} is now
available. A few minor bugs in the syntax definition have been fixed and
hexadecimal floating-point literals are now supported.

**2005-05-20** [Stratego Shell 0.5](StrategoShellRelease05){.twikiLink}
is now available. This release fixes various bugs and supports
[Stratego/XT 0.14](StrategoRelease014){.twikiLink}.

**2005-01-14**\
[Stratego Shell 0.4](StrategoShellRelease04){.twikiLink}, the first
offical release, is now available! The [Stratego
Shell](StrategoShell){.twikiLink} implements a Stratego interpreter and
an interactive shell for Stratego programming. The interpreter and shell
are very useful for learning Stratego and for implementing small tests.

**2005-01-14**\
[Java-front 0.6](JavaFrontRelease06){.twikiLink} has been released. This
release improves the embedding of Java in Stratego.

**2005-01-13**\
[Stratego/XT 0.13](StrategoRelease013){.twikiLink} has been released.
This releases features the implementation of *dependent dynamic rewrite
rules* and various bug-fixes and new features of the Stratego compiler
and the transformation tools of Stratego/XT. See the release page for
more details.

**2004-11-24**

Builds of Stratego/XT and extension packages is now done
[continuously](ContinuousBuild){.twikiLink} using a
[Nix](http://www.cs.uu.nl/groups/ST/Trace/Nix) build farm. Source and
binary distributions are available only hours after committing a change.

**2004-10-04**

[Java-front 0.5](JavaFrontRelease05){.twikiLink} has been released.
Java-front adds support for Java program transformation to StrategoXT.
It provides a handcrafted [SDF](SDF){.twikiLink} syntax definition and
pretty-printer for Java (J2SE 5.0).

**2004-10-04**

[StrategoXT 0.12](StrategoRelease012){.twikiLink} has been released.
This releases improves the usability of several tools and extends the
support for XML exchange. Also, the error reporting of format-check has
improved drastically.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
:::
:::
