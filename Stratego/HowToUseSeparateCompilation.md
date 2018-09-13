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
    Page](http://www.program-transformation.org/edit/Stratego/HowToUseSeparateCompilation?t=1536825586)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/HowToUseSeparateCompilation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/HowToUseSeparateCompilation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/HowToUseSeparateCompilation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/HowToUseSeparateCompilation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/HowToUseSeparateCompilation?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/HowToUseSeparateCompilation?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/HowToUseSeparateCompilation?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/HowToUseSeparateCompilation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/HowToUseSeparateCompilation?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/HowToUseSeparateCompilation?template=oopsmore&param1=1.2&param2=1.2)
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
How To Use Separate Compilation {#how-to-use-separate-compilation .twikiTopicTitle}
===============================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

This manual is under construction!

[]{#Table_of_Contents} Table of Contents
----------------------------------------

::: {.twikiToc}
-   [Table of Contents](HowToUseSeparateCompilation#Table_of_Contents)
-   [Introduction](HowToUseSeparateCompilation#Introduction)
-   [Using a library](HowToUseSeparateCompilation#Using_a_library)
    -   [Using strc at the
        command-line](HowToUseSeparateCompilation#Using_strc_at_the_command_line)
    -   [Using AutoXT and
        Automake](HowToUseSeparateCompilation#Using_AutoXT_and_Automake)
-   [Creating your own
    library](HowToUseSeparateCompilation#Creating_your_own_library)
    -   [Producing the C
        code](HowToUseSeparateCompilation#Producing_the_C_code)
    -   [Compile and link to a
        library](HowToUseSeparateCompilation#Compile_and_link_to_a_library)
:::

[]{#Introduction} Introduction
------------------------------

[]{#Using_a_library} Using a library
------------------------------------

At the command-line, or in Automake.

### []{#Using_strc_at_the_command_line} Using `strc` at the command-line

      module foo
      imports lib
      strategies
        ...

      module foo
      imports liblib
      strategies
        ...

      strc -i foo.str -la stratego-lib

### []{#Using_AutoXT_and_Automake} Using AutoXT and Automake

Libtool, Automake and [AutoXT](AutoXT){.twikiLink} make separate
compilation in Makefiles almost trivial.

Use libtool for linking.

-   Invoking `libtoolize` or `glibtoolize` (MacOS X) in `bootstrap`
-   Add `AC_PROG_LIBTOOL` to `configur.ac`

Libtool will add the path of a dynamic library to the search path in the
executable. If you don\'t use Libtool, then you might need to set the
`LD_LIBRARY_PATH` environment variable.

For the separately compiled SSL `Makefile.xt` defines the variable
`SSL_LIBS`.

All program:

      LDADD += $(SSL_LIBS)

Just for the program foo:

      foo_LDADD = $(SSL_LIBS)

Other libraries: use `-L` and `-l`.

[]{#Creating_your_own_library} Creating your own library
--------------------------------------------------------

      module mod
      imports liblib
        strategies
          ...

### []{#Producing_the_C_code} Producing the C code

The Stratego Compiler strc can be used now to generate a library from a
module file.str with the command

      strc -i mod.str -c -o libmod.rtee --library 

This produces three files:

-   libmod.c
-   libmod.str
-   libmod.rtree

The first is the C implementation of the closure of `mod.str`. It
provides C functions for all user-defined strategies, and static C
functions for strategies generated at compile-time. The last two are the
concrete syntax and abstract syntax files for a Stratego module with
external definitions for all strategies defined in `mod.str` and
imported modules. It is now possible to import libmod in another
Stratego program, instead of mod. Note that `libmod.str` is produced
mainly for documentation, `libmod.rtree` should be used to import. This
is done automatically by the compiler as long as the file is present.

Note that no modules from the \'library\' should be imported in the
program via another path. This will lead to doubly defined strategies;
it is not allowed to extend external definitions.

### []{#Compile_and_link_to_a_library} Compile and link to a library

The C program `libmod.c` can be compiled to an object file `libmod.o`
and to a static (`liblibmod.a`) or shared (`liblibmod.so`) library. This
should be done in a makefile; strc does not deal with C compilation of
libraries.

Static linking of the libraries thus produced may actually lead to
larger executables since no unused-function-removal is performed on the
library (for obvious reasons). Shared libraries are the solution here to
save diskspace. This can be achieved by proper use of libtool in the
buildenvironment; again strc does not provide support for this.

Compiling and linking a library using Libtool and Autmake is very easy.
Basically, the only thing you need to do is to declare that you want to
have a library:

      pkglib_LTLIBRARIES   = libmod.la 
      pkgdata_DATA         = libmod.rtree

      liblibmod_la_SOURCES = libmod.c
      AM_CPPFLAGS          = -I$(SRTS)/include -I$(ATERM)/include

      libmod.c : 
       $(STRC)/bin/strc -c --library -i ./mod.str -o libmod.rtree

\-- [MartKolthof](../Main/MartKolthof){.twikiLink} - 23 Jun 2005\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
