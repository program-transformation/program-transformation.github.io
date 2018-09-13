::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
[![PHP-SatLogo](../pub/PHP/PhpSatLogo/PHP-SAT-LOGO-100px.jpg)](WebHome){.twikiLink}

**[PHP-sat](PhpSat){.twikiLink}**

-   [Download](PhpSatReleases){.twikiLink}
-   [Documentation](PhpSatDocumentation){.twikiLink}
-   [Bugpatterns](PhpSatBugPatterns){.twikiLink}
-   [Quality](PhpSatQuality){.twikiLink}
-   [Origin](PhpSatOrigin){.twikiLink}
-   [Name](PhpSatName){.twikiLink}

**[PHP-front](PhpFront){.twikiLink}**

-   [Download](PhpFrontReleases){.twikiLink}
-   [Documentation](PhpFrontDocumentation){.twikiLink}
-   [Quality](PhpFrontQuality){.twikiLink}
-   [Origin](PhpFrontOrigin){.twikiLink}

**[PHP-tools](PhpTools){.twikiLink}**

**[Support](PhpSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Issues](http://bugs.strategoxt.org/browse/PSAT)

**[Developers](PhpSatDevelopers){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/psat/)
-   [Continuous Builds](ContinuousBuilds){.twikiLink}
-   [Blog](http://ericbouwers.blogspot.com/)

**[The logo](PhpSatLogo){.twikiLink}**

**[Thanks](ThankYou){.twikiLink}**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/PHP/TheEmptyModule?t=1536826877)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/TheEmptyModule)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/TheEmptyModule)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/TheEmptyModule?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/TheEmptyModule?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/PHP/TheEmptyModule?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/PHP/TheEmptyModule?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/PHP/TheEmptyModule?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/TheEmptyModule)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/TheEmptyModule?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/PHP/TheEmptyModule?template=oopsmore&param1=1.2&param2=1.2)
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
The Empty Module {#the-empty-module .twikiTopicTitle}
================

::: {.twikiWebTitle}
Static analysis for PHP
:::

The empty module is a top-level directory in the SVN-repository which
contains everything you need to start your own project based on
PHP-Front. The special name that is used for this \'project\' is
*empty-module*. This name can/should be replaced with the name of your
own project.

This page explains the contents of the directory and the purpose of
several files. [TheExampleProject](TheExampleProject){.twikiLink}
explains how this directory can be used in order to set up a new
project. Note that the following explanation is based on the structure
of PHP-Front and PHP-Sat. There is also an explanation
[available](http://hydra.nixos.org/jobset/psat/strategoxt-manual-unstable-latest/manual/chunk-chapter/library-building.html#id3631738)
for Stratego programs in general.

The directory has three top-level directories: *branches*, *tags* and
*trunk*. We will only discuss the contents of the *trunk* here because
that is where the magic happens. You can find a good explanation of how
to use the other directories
[here](http://ariejan.net/2006/11/24/svn-how-to-structure-your-repository/).

The directory contains the following directories (red) and files (blue):

::: {.twikiToc}
-   [config](TheEmptyModule#config_font)
-   [doc](TheEmptyModule#doc_font)
-   [src](TheEmptyModule#src_font)
    -   [grammar](TheEmptyModule#grammar_font)
        -   [grammar/Makefile.am](TheEmptyModule#grammar_Makefile_am)
    -   [lib](TheEmptyModule#lib_font)
        -   [lib/Makefile.am](TheEmptyModule#lib_Makefile_am)
    -   [tools](TheEmptyModule#tools_font)
        -   [tools/Makefile.am](TheEmptyModule#tools_Makefile_am)
    -   [Makefile.am](TheEmptyModule#Makefile_am)
-   [tests](TheEmptyModule#tests_font)
    -   [Makefile.am-grammar](TheEmptyModule#Makefile_am_grammar)
    -   [Makefile.am-libtool](TheEmptyModule#Makefile_am_libtool)
-   [AUTHORS](TheEmptyModule#AUTHORS)
-   [bootstrap](TheEmptyModule#bootstrap)
-   [Changelog](TheEmptyModule#Changelog)
-   [configure.ac](TheEmptyModule#configure_ac)
-   [empty-module.pc.in](TheEmptyModule#empty_module_pc_in)
-   [empty-module.spec.in](TheEmptyModule#empty_module_spec_in)
-   [Makefile.am](TheEmptyModule#Makefile_am)
-   [NEWS](TheEmptyModule#NEWS)
-   [README](TheEmptyModule#README)
:::

[]{#config_font}[]{#_config_font_} config
-----------------------------------------

This directory will contain the configuration files after you run the
*bootstrap* file, just here for convenience.

[]{#doc_font}[]{#_doc_font_} doc
--------------------------------

Documentation directory. It is a good practice to document the tools /
library that you made in your project in different sub-directories.

[]{#src_font}[]{#_src_font_} src
--------------------------------

The actual sources of your project, there are three different kind of
sources:

### []{#grammar_font}[]{#_grammar_font_} grammar

Grammar sources are \*.sdf files that define a grammar for your project,
for example the grammar of your configuration file.\
The grammar is usually defined in a sub-directory
*languages/empty-module* with one file at top-level, *empty-module.sdf*.
A good example is the [PHP-Sat
structure](https://svn.strategoxt.org/repos/psat/php-sat/trunk/src/grammar/).

#### []{#grammar_Makefile_am} grammar/Makefile.am

This file is the input file for the generation of the actual Makefile.
It already defines a grammar that should be defined in the
*languages/empty-module* -directory with a toplevel file called
*empty-module.sdf*.

### []{#lib_font}[]{#_lib_font_} lib

Library sources are libraries that should be build for your project.
Making a library is useful if you want to make a set of tools that share
common functionality. Library sources should be defined as normal
stratego-files (\*.str) which are placed in the directory
*empty-module/* with a top-level-file called *empty-module.str*.

#### []{#lib_Makefile_am} lib/Makefile.am

This file is the input for the generation of the actual Makefile. It
already defines a library called *libempty-module.la*, which is defined
in the directory *empty-module/* with a toplevel-file called
*empty-module.str*. Apart from the library is also generates the
signature-file of the grammar defined in the *src/grammar/* -directory.
It also compiles this grammar to a C-file so that it can be imported
into the library.\
The configuration is also aware of any \*.meta files in the
*empty-module* -subdirectory.

### []{#tools_font}[]{#_tools_font_} tools

Tool sources are the actual tools defined in \*.str files. These files
are build as separate tools that are linked to the PHP-Front-library and
the libary you defined yourself.

#### []{#tools_Makefile_am} tools/Makefile.am

This file is the input for the generation of the actual Makefile. It
already defines one tool called *empty-module.str* which is defined in
this directory.

### []{#Makefile_am} Makefile.am

This file is the input for the generation of the actual Makefile. It
just instruct `make` to go into the subdirectories.

[]{#tests_font}[]{#_tests_font_} tests
--------------------------------------

Contains all the tests of your project, please use this! Tests help you
by thinking about the code you write, checking what you have done and
making sure that you did not break anything. We have added two files
that can serve as input for the Makefile for testing the different parts
of your project.

### []{#Makefile_am_grammar} Makefile.am-grammar

This file is the input for the generation of the actual Makefile. It
defines a sdf-testsuite called *empty-module.testsuite* which should
contain the tests for your grammar.

### []{#Makefile_am_libtool} Makefile.am-libtool

This file is the input for the generation of the actual Makefile. It
defines a tool called *empty-module-tests* that should test (a part of)
your library or a tool. This tool should be defined in a file called
*empty-module-tests.str* in the same directory.

[]{#AUTHORS} AUTHORS
--------------------

The name explains it all I guess.

[]{#bootstrap} bootstrap
------------------------

This script will bootstrap your project and will generate all the actual
Makefile-files and a script called *configure*. This *configure* script
is used to find all the required tools that are necessary for the
project.

[]{#Changelog} Changelog
------------------------

Use this file to keep track of the changes of your project, or just one
line with **upgraded project**.

[]{#configure_ac} configure.ac
------------------------------

This file is the input file for the configuration of the actual
*configure* -script. It defines the name of the project, the
email-address of the project and the input files it should use to
generate the *configure* -script. It also lists all the Makefile-files
it should generate.

[]{#empty_module_pc_in} empty-module.pc.in
------------------------------------------

One of the two files used to create the \_configure\_-script. Should
have a name and a description for the project.

[]{#empty_module_spec_in} empty-module.spec.in
----------------------------------------------

One of the two files used to create the \_configure\_-script. Should
have a summary and a URL for the project.

[]{#Makefile_am} Makefile.am
----------------------------

Top-level Makefile.am which will generate the top-level Makefile. It
just tells `make` to go into the subdirectories.

[]{#NEWS} NEWS
--------------

This file should contain all the latests news about your project.

[]{#README} README
------------------

The name of this file explains exactly what needs to be in this file.
Think about what the people that will use your project need to know
before they install/use your project.

\-- [EricBouwers](../Main/EricBouwers){.twikiLink} - 01 Jan 2007\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
