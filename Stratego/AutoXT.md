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
    Page](http://www.program-transformation.org/edit/Stratego/AutoXT?t=1536825555)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/AutoXT)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/AutoXT)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/AutoXT?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/AutoXT?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Stratego/AutoXT?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/AutoXT?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/AutoXT?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/AutoXT?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/AutoXT?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/AutoXT?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/AutoXT)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/AutoXT?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Stratego/AutoXT?template=oopsmore&param1=1.7&param2=1.7)
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
Auto XT {#auto-xt .twikiTopicTitle}
=======

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The autoxt package provides Autoconf and Automake support for packages
constructed with the XT toolset. The package provides the `autoxt` tool
which should be run as part of the Autoconf/Automake bootstrapping
process, prior to running `autoconf`. A typical `bootstrap` script looks
like:

    #! /bin/sh

    autoxt
    autoreconf -if

The toplevel `Makefile.am` should declare:

    ACLOCAL_AMFLAGS = -I .

[]{#Autoconf} Autoconf
----------------------

Autoxt installs a set of m4 macros `autoxt.m4` with support for package
configuration switches. By just including the macro call
`XT_USE_XT_PACKAGES` a `configure.ac` file can be parameterized with
switches for all the StrategoXT packages:

    AC_INIT([java-front],[0.6],[stratego-bugs@cs.uu.nl])
    AM_INIT_AUTOMAKE

    XT_USE_XT_PACKAGES
    XT_PKG_ATERM
    XT_PKG_SDF
    XT_PKG_STRATEGOXT

    AC_PROG_CC
    AC_PROG_INSTALL
    AC_CONFIG_FILES([Makefile syn/Makefile])
    AC_OUTPUT

### []{#Available_Macros} Available Macros

-   `XT_USE_XT_PACKAGES`\
    Adds configuration options to configure the package with the
    location of the ATerm library, SDF and StrategoXT.

<!-- -->

-   `XT_PKG_ATERM`\
    Checks if the ATerm library is installed at the specified prefix of
    the ATerm library.

<!-- -->

-   `XT_PKG_SDF`\
    Checks if the SDF packages are installed at the specified prefix of
    SDF.

<!-- -->

-   `XT_PKG_STRATEGOXT`\
    checks if StrategoXT is installed at the specified prefix of
    StrategoXT.

<!-- -->

-   `XT_TERM_DEFINE`\
    Defines some Stratego strategies that will return the values (as
    strings) of various Autoconf variables: `PACKAGE_NAME_TERM()`,
    `PACKAGE_TARNAME_TERM()`, `PACKAGE_VERSION_TERM()`,
    `PACKAGE_BUGREPORT_TERM()`, and `SVN_REVISION_TERM()`. These
    strategies can be used in any Stratego program in this package.

<!-- -->

-   `XT_PRE_RELEASE`\
    Adds the suffix `pre${SVN_REVISION}` to the `PACKAGE_VERSION` and
    `VERSION` variables. This is a naming convention for unstable
    packages that we are using in our release management system.

[]{#Automake} Automake
----------------------

Furthermore, autoxt installs `Makefile.xt`, a collection of automake
rules for compiling Stratego programs and applying other XT tools, such
as signature generation. Using this makefile, a makefile reduces to a
declaration of programs to be compiled. The makefile automatically takes
care of distributing the generated C code. The specification will only
be compiled when it is newer than the C code. This means that packages
using autoxt can be built using only the Stratego Run-Time System
(srts).

    include $(top_srcdir)/Makefile.xt
    include $(wildcard *.dep)

    bin_PROGRAMS    = xtc
    pkgdata_DATA    = xtc-lib.rtree xtc-rep.rtree xtc-proc.rtree
    SCFLAGS         = --main $*
    STRINCLUDES     = -I $(XTC)/share/xtc
    EXTRA_DIST      = $(pkgdata_DATA) $(wildcard *.str) $(wildcard *.meta)
    CLEANFILES      = $(wildcard *.dep)
    BOOTCLEANFILES  = xtc.c

### []{#Explanation_of_the_example} Explanation of the example

-   `include $(top_srcdir)/Makefile.xt`\
    Instructs the Stratego compiler to compile the Stratego files.

<!-- -->

-   `include $(wildcard *.dep)`\
    The Stratego compiler generates .dep files which contain information
    about file dependencies. When these .dep files are included a
    rebuild is forced when a dependent file changes.

<!-- -->

-   `bin_PROGRAMS`\
    Specifies the resulting binaries from the compilation.

<!-- -->

-   `pkgdata_DATA`\
    Are the files that will be placed in *\$prefix/share/pkg*, see: [How
    to Use Separate
    Compilation](HowToUseSeparateCompilation){.twikiLink}

<!-- -->

-   `SCFLAGS`\
    Contains compiler flags passed to the Stratego compiler.

<!-- -->

-   `STRINCLUDES`\
    Are the additional includes necessary for a succesful compilation.

<!-- -->

-   `EXTRA_DIST`\
    Specifies which auxilary files have to be included in the
    distribution.

<!-- -->

-   `CLEANFILES`\
    Deletes these files when the *make clean* command is issued.

<!-- -->

-   `BOOTCLEANFILES`\
    In addition to files specified in *CLEANFILES*, deletes these files
    when the *make bootclean* command is issued.

See also:

-   [How to Use Separate
    Compilation](HowToUseSeparateCompilation){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
