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
    Page](http://www.program-transformation.org/edit/Stratego/SimpleProjectCreation?t=1536825668)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SimpleProjectCreation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SimpleProjectCreation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SimpleProjectCreation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SimpleProjectCreation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/SimpleProjectCreation?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/SimpleProjectCreation?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/SimpleProjectCreation?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SimpleProjectCreation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SimpleProjectCreation?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/SimpleProjectCreation?template=oopsmore&param1=1.2&param2=1.2)
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
Simple Project Creation {#simple-project-creation .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Creating_a_Stratego_XT_project_t} Creating a Stratego/XT project the simple way
-----------------------------------------------------------------------------------

The easiest way to set up a working Stratego/XT project is to use the
Create-a-Project tool called `crap`, available in the
[strategoxt-utils](http://releases.strategoxt.org/strategoxt-utils/strategoxt-utils-unstable/)
package.

Once installed, creating a new project `p0` is as easy as one line:

    $ crap --new-project p0

This will generate an standard GNU Autotools-based build system,
including with a minimal example (`src/xmpl.str`):

    p0/
       Makefile.am
       README.Developer
       README
       AUTHORS
       bootstrap
       p0.spec.in
       NEWS
       p0.pc.in
       configure.ac
       ChangeLog
       xmpl/
            Makefile.am
       syn/
           Makefile.am
       tests/
             Makefile.am
       src/
           Makefile.am
           xmpl.str

The project is ready to be compiled,

    $ ./bootstrap
    $ ./configure --prefix=$HOME/apps/p0
    $ make all 

installed,

    $ make install

and executed:

    $ echo "foo" | $HOME/apps/p0/bin/xmpl
    Hello, World!

(The example is a transformation component using `io-wrap` \-- it takes
a term and spits out the string `"Hello, World!"`.)

### []{#Adding_project_dependencies} Adding project dependencies

Most non-trivial Stratego/XT projects rely on pre-existing libraries and
tools, such as one of the many language parsers available for
Stratego/XT. Using the `--deps` switch, you can add the necessary lines
to the `configure.ac` file as well as the appropriate include switches
to each `Makefile` automatically:

    $ crap --deps java-front,dryad --new-project p0

The above will create the project `p0` with `XT_USE_JAVA_FRONT` and
`XT_USE_DRYAD` added to your configure.ac, plus the necessary `-I`, `-L`
and `-l` flags throughout each generated `Makefile`.

It is possible to list the available dependencies which are addable to
your project using the `--list-available-providers` switch:

    $ crap --list-available-providers

This would give a list looking something like this:

    dryad
    stratego-aterm
    stratego-tool-doc
    stratego-sglr
    stratego-xtc
    stratego-gpp
    stratego-lib
    c-tools
    stratego-sdf
    java-front
    stratego-rtg

Beware: The dependency/provider system will change in future versions of
`crap`.

### []{#Adding_pre_made_syntax_fragments} Adding pre-made syntax fragments

`crap` comes with a small (but growing) collection of syntax modules
that may freely be used in your project. This might save you from a lot
of boring boilerplate code when defining a new language. To add a basic
definition of whitespaces and integer literals to your project, do:

    $ crap --create-project p0 --syntax-modules integer-literals,whitespace

To list the available syntax modules in your version of `crap`, use the
`--list-syntax-modules` switch:

    $ crap --list-syntax-modules

It will return a list on the form:

    floating-point-literals
    integer-literals
    whitespace

### []{#XTC_support} [XTC](XTC){.twikiLink} support

There is some basic support for setting up a build of
[XTC](XTC){.twikiLink} components using `crap`, using the `--xtc`
switch:

    $ crap --xtc --new-project p0

The above will create the following `src/` directory layout and content:

       src/
           Makefile.am
           xtc/
               Makefile.am
               xtcxmpl.str

The `xtcxmpl` will be compiled against `libstratego-xtc`. Upon
installation, it will registered as an [XTC](XTC){.twikiLink} component
and placed in `${prefix}/libexec`.

### []{#Making_libraries} Making libraries

Building libraries with Stratego requires a fair bit build setup. This
is done automatically for you using the `--library` switch:

    $ crap --library --new-project p0

This will create the following `src/` directory layout and content:

    src/
        Makefile.am
        lib/
            Makefile.am
            def-libxmpl.str
            xmpl/
                 foo.str

Upon compilation, the files `libxmpl.str`, `libxmpl.rtree`,
`libxmpl.ctree` and `libxmpl.so` (plus auxiliary libtool files) are
generated. The are all installed into `${prefix}/share` (`.ctree`,
`.rtree`) and `${prefix}/lib` (`.so`) as is normal for Stratego
libraries.

### []{#Working_with_Spoofax} Working with Spoofax

If you are developing with [Spoofax](http://www.spoofax.org), you can
generate the necessary Eclipse files (`.project`) as part of the project
creating using the `--eclipse` switch:

    $ crap --eclipse --new-project p0

### []{#Generation_source_code_documenta} Generation source code documentation

Source code documentation, Javadoc-style, can be generated from Stratego
code using the XDoc tool. By adding the `--xdoc` switch, the build
system will be set up to generate source code documentation in the
`doc/api` directory:

    $ crap --xdoc --new-project p0

This will add a `doc/` directory and an appropriate `Makefile`.

       doc/
           Makefile.am

### []{#Questions_Bugs}[]{#Questions_Bugs_} Questions? Bugs?

If you have questions, please post them to the [Stratego
mailinglist](https://mail.cs.uu.nl/mailman/listinfo/stratego). Bugs are
best reported using our [issue tracker](https://bugs.strategoxt.org).

\-- [KarlTrygveKalleberg](../Main/KarlTrygveKalleberg){.twikiLink} - 23
May 2008\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
