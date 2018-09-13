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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease017?t=1536825497)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease017)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease017)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease017?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease017?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    22](http://www.program-transformation.org/view/Stratego/StrategoRelease017?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease017?rev1=1.22&rev2=1.21)
-   [Rev
    21](http://www.program-transformation.org/view/Stratego/StrategoRelease017?rev=1.21)
    [(diff 20)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease017?rev1=1.21&rev2=1.20)
-   [Rev
    20](http://www.program-transformation.org/view/Stratego/StrategoRelease017?rev=1.20)
    [(diff 19)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease017?rev1=1.20&rev2=1.19)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease017)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease017?template=oopsmore&param1=1.22&param2=1.22)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease017?template=oopsmore&param1=1.22&param2=1.22)
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
Stratego/XT 0.17 {#strategoxt-0.17 .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Stratego/XT 0.17 - released July 2009

[]{#Known_issues}[]{#_Known_issues} Known issues
------------------------------------------------

-   On 64 bit systems, parsing using SGLR (which is used in many
    Stratego programs) can result in SEGV due to limited stack size.
    This can be solved by executing `ulimit -s unlimited`, or with any
    bigger stack size than the current one.
-   The ATerm library needs [this
    patch](https://svn.nixos.org/repos/nix/nixpkgs/trunk/pkgs/development/libraries/aterm/max-long.patch)
    to work.

[]{#Download}[]{#_Download} Download
------------------------------------

See the [installation
instructions](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/installation.html)
if you are not familiar with the standard installation procedure of
tarballs or RPMs.

![](http://buildfarm.info/images/src-pkg.png) Source tar.gz

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/aterm-2.5.tar.gz)
    (use [this
    patch](https://svn.nixos.org/repos/nix/nixpkgs/trunk/pkgs/development/libraries/aterm/max-long.patch))
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/sdf2-bundle-2.4.tar.gz)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/strategoxt-0.17.tar.gz)

![](http://buildfarm.info/images/suse.png) SuSE Linux RPM

SuSE 11.0:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse103i386/aterm-2.5-1.i586.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse103i386/sdf2-bundle-2.4-1.i586.rpm)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse103i386/strategoxt-0.17-1.i586.rpm)

SuSE 10.3:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse110i386/aterm-2.5-1.i586.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse110i386/sdf2-bundle-2.4-1.i586.rpm)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse110i386/strategoxt-0.17-1.i586.rpm)

![](http://buildfarm.info/images/fedora.png)Fedora Core RPM

Fedora Core 11:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora11i386/aterm-2.5-1.i386.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora11i386/sdf2-bundle-2.4-1.i386.rpm)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora11i386/strategoxt-0.17-1.i386.rpm)

Fedora Core 10:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora10i386/aterm-2.5-1.i386.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora10i386/sdf2-bundle-2.4-1.i386.rpm)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora10i386/strategoxt-0.17-1.i386.rpm)

Fedora Core 9:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora9i386/aterm-2.5-1.i386.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora9i386/sdf2-bundle-2.4-1.i386.rpm)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora9i386/strategoxt-0.17-1.i386.rpm)

Fedora Core 5:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora5i386/aterm-2.5-1.i386.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora5i386/sdf2-bundle-2.4-1.i386.rpm)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora5i386/strategoxt-0.17-1.i386.rpm)

![](http://buildfarm.info/images/debian.png)Debian DEB

Debian 5.0:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/debian50i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/debian50i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/debian50i386/strategoxt_0.17-1_i386.deb)

Debian 4.0:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/debian40i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/debian40i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/debian40i386/strategoxt_0.17-1_i386.deb)

![](http://buildfarm.info/images/debian.png)Ubuntu DEB

Ubuntu 9.04:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu904i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu904i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu904i386/strategoxt_0.17-1_i386.deb)

Ubuntu 8.10:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu810i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu810i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu810i386/strategoxt_0.17-1_i386.deb)

Ubuntu 8.04:

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu804i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu804i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu804i386/strategoxt_0.17-1_i386.deb)

![](http://buildfarm.info/images/win32.png)
![](http://buildfarm.info/images/cygwin.gif) Microsoft Windows Cygwin
binaries

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/cygwin/aterm-2.5-cygwin.tar.gz)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/cygwin/sdf2-bundle-2.4-cygwin.tar.gz)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/cygwin/strategoxt-0.17-cygwin.tar.gz)
-   [aterm-2.5 + sdf2-bundle-2.4 +
    strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/cygwin/strategoxt-superbundle-0.17-cygwin.tar.gz)

<!-- -->

-   The \*-cygwin.tar.gz files contain a file `README` with installation
    instructions.

![](http://buildfarm.info/images/macosx.gif) Mac OS X binaries

-   [aterm-2.5](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/macosx/aterm-2.5-macosx.tar.gz)
-   [sdf2-bundle-2.4](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/macosx/sdf2-bundle-2.4-macosx.tar.gz)
-   [strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/macosx/strategoxt-0.17-macosx.tar.gz)
-   [aterm-2.5 + sdf2-bundle-2.4 +
    strategoxt-0.17](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/macosx/strategoxt-superbundle-0.17-macosx.tar.gz)

<!-- -->

-   The \*-macosx.tar.gz files contain a file `README` with installation
    instructions.

![](http://buildfarm.info/images/package.png) Nix Package

One-click installation using [Nix](http://nixos.org), open with
`nix-install-package`

-   [aterm-2.5](http://hydra.nixos.org/job/nixpkgs/trunk/aterm25)
-   [sdf2-bundle-2.4](http://hydra.nixos.org/job/nixpkgs/trunk/strategoPackages.sdf)
-   [strategoxt-0.17](http://hydra.nixos.org/job/nixpkgs/trunk/strategoPackages.strategoxt)

[]{#Documentation}[]{#_Documentation} Documentation
---------------------------------------------------

### []{#Stratego_XT_Manual}[]{#_Stratego_XT_Manual} Stratego/XT Manual

The Stratego/XT Manual is a series of three books: a tutorial, a series
of examples, and a reference manual with the finer details of the
language and tools. The manual is available online and can be downloaded
for offline use.

-   [Stratego/XT 0.17 Manual - Online
    version](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/)
-   [Stratego/XT 0.17 Manual - Offline
    version](http://hydra.nixos.org/build/45929)
-   [Stratego/XT 0.17 Manual - Preliminary PDF
    version](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/pdf/latest/download/1)

Warning: this manual is specific for Stratego/XT 0.17 and will not be
extended. The latest version of the manual, available at at the
[documentation](StrategoDocumentation){.twikiLink} page, might be more
extensive, but might also cover features that were not yet available in
Stratego/XT 0.17.

### []{#Stratego_XT_API_Documentation}[]{#_Stratego_XT_API_Documentation} Stratego/XT API Documentation

Online API documentation:

-   [Stratego
    Library](http://buildfarm.info/docs/libstratego-lib-docs-0.17/)

Download API documentation for local and offline use:

-   Stratego Library:
    [libstratego-lib-docs-0.17.tar.gz](ftp://ftp.stratego-language.org/pub/stratego/StrategoXT/strategoxt-0.17/docs/libstratego-lib-docs-0.17.tar.gz)

[]{#License}[]{#_License} License
---------------------------------

Stratego/XT is free software; you can redistribute it and/or modify it
under the terms of the GNU Lesser General Public License as published by
the Free Software Foundation; either version 2 of the License, or (at
your option) any later version.

This software is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Lesser
General Public License for more details.

### []{#Support}[]{#_Support} Support

Despite the disclaimer above we do our best to help users of
Stratego/XT. Subscribe to the Stratego [mailing
lists](MailingList){.twikiLink}, in particular the stratego-announce and
stratego mailing lists to get announcements of new releases and ask
questions about usage of the languages and tools. Also we\'re interested
to know what people are using Stratego/XT for and how it might be
improved, so feel free to drop [us](StrategoCommunity){.twikiLink} a
line.

------------------------------------------------------------------------

Stratego/XT 0.17 - released July 2009

------------------------------------------------------------------------

[]{#Summary_of_Changes}[]{#_Summary_of_Changes} Summary of Changes
------------------------------------------------------------------

Stratego/XT 0.17 introduces major improvements across the board,
including language additions, a new compiler library, numerous
improvements to the compiler, significant changes to the library
handling, new libraries for parsing, pretty printing and term
validation, 64-bit support, stack traces and more.

For this release, over 200 outstanding issues have been addressed, much
thanks to the efforts of external bug reporters and contributors.

The manual has been updated to reflect the changes made to the language
and libraries, and the new libraries come with up-to-date source code
documentation.

::: {.twikiToc}
-   [Stratego in Print](StrategoRelease017#Stratego_in_Print)
-   [Stratego Compiler](StrategoRelease017#Stratego_Compiler)
    -   [Standard C: Dropped GCC\'s nested
        functions](StrategoRelease017#Standard_C_Dropped_GCC_s_nested)
    -   [Stack traces on \"rewriting
        failed\"](StrategoRelease017#Stack_traces_on_rewriting_failed)
    -   [A new \"with\" construct for rewrite
        rules](StrategoRelease017#A_new_with_construct_for_rewrite)
    -   [Compiler library](StrategoRelease017#Compiler_library)
-   [Stratego Language](StrategoRelease017#Stratego_Language)
    -   [Assignment operator](StrategoRelease017#Assignment_operator)
    -   [Dynamic rules](StrategoRelease017#Dynamic_rules)
        -   [Improved flow-sensitive
            transformations](StrategoRelease017#Improved_flow_sensitive_transfor)
        -   [Scoped global
            variables](StrategoRelease017#Scoped_global_variables)
        -   [Chained dynamic
            rules](StrategoRelease017#Chained_dynamic_rules)
    -   [External Constructor
        Declarations](StrategoRelease017#External_Constructor_Declaration)
    -   [Rule syntax in let](StrategoRelease017#Rule_syntax_in_let)
    -   [Import ATerm from
        file](StrategoRelease017#Import_ATerm_from_file)
-   [Stratego Libraries](StrategoRelease017#Stratego_Libraries)
    -   [Migrating from XTC to
        libraries](StrategoRelease017#Migrating_from_XTC_to_libraries)
    -   [strcflags](StrategoRelease017#strcflags)
    -   [Easy library
        creation](StrategoRelease017#Easy_library_creation)
-   [Deployment](StrategoRelease017#Deployment)
    -   [Standards-compliant
        libraries](StrategoRelease017#Standards_compliant_libraries)
    -   [Native Windows Support
        (MinGW)](StrategoRelease017#Native_Windows_Support_MinGW)
    -   [OSX support](StrategoRelease017#OSX_support)
    -   [x86-64 support](StrategoRelease017#x86_64_support)
:::

[]{#Stratego_in_Print} Stratego in Print
----------------------------------------

M. Bravenboer, K. T. Kalleberg, R. Vermaas, and E. Visser. Stratego/XT
0.17. A Language and Toolset for Program Transformation. Science of
Computer Programming, 2008. Special issue on Experimental Systems and
Tools, <http://dx.doi.org/10.1016/j.scico.2007.11.003>

[]{#Stratego_Compiler} Stratego Compiler
----------------------------------------

### []{#Standard_C_Dropped_GCC_s_nested}[]{#Standard_C_Dropped_GCC_s_nested_} Standard C: Dropped GCC\'s nested functions

The backend has been changed so that the GCC-specific nested functions
feature is no longer required. This makes the C-code a lot more portable
across GCC-supported platforms, since nested functions are not reliably
supported on all architectures, notably not on MIPS and OSX/Intel.
Furthermore, this allows Stratego to use other C compilers for than GCC
for the generation of platform-specific binary code.

-   \[[STR-697](http://bugs.strategoxt.org/browse/STR-697)\] -
    Standalone strc; allow users to override \--cc and \-\--ld
-   \[[STR-119](http://bugs.strategoxt.org/browse/STR-119)\] - Replace
    GCC nested functions by stack-allocated closures as structs

### []{#Stack_traces_on_rewriting_failed} Stack traces on \"rewriting failed\"

The compiler backend and supporting runtime code have been modified to
provide full stack traces for the dreaded \"rewriting failed\"
situations.

Consider the following program:

      main = foo

      foo = bar

      bar = fap ; zap

      fap = id

      zap = fail 

When executed, it will print:

    prog: rewriting failed, trace:
            main_0_0
            foo_0_0
            bar_0_0
            zap_0_0 

This also works when you use `io-wrap` and friends, but there are some
caveats:

-   Only code compiled with the new compiler will show up in the stack
    trace: if you call old libraries, stack frames for those strategies
    will be invisble.

<!-- -->

-   `let` blocks and other reasons for lifting will show up as
    `lifted_X` frames.

A tiny set of stack introspection strategies for debugging purposes has
also been introduced.

### []{#A_new_with_construct_for_rewrite} A new \"with\" construct for rewrite rules

A new `with` construct has been added for rewrite rules, which makes use
of the stack tracing feature above. A `with` clause works much like a
regular `where` clause, and can for example be used to assign variables
for use in the right-hand side of a rule:

      desugar:
        |[ e1 + e2 ]| -> |[ x_add(e1, e2) ]|
        where
          <typeof> e1 => Int()
        ; <typeof> e2 => Int()
        with
          x_add := <new-add-operation> (e1, e2)

However, unlike the `where` clause, its operations are not allowed to
fail, or a run-time error will be reported with a stack trace. Thus,
this addition allows Stratego programmers to explicitly distinguish
between *conditions* of a rule (the `where` clause) and *operations*
that must always succeed (the `with` clause). This helps in readability
and in debugging errors in rewrite rules. Any failures inside a `with`
clause are considered programmer errors: the contract specified by the
`with` clause is then not satisfied (for example, a rule may require
some dynamic rule to be defined). By immediately reporting such errors,
this feature allows them to be quickly identified, avoiding problems
that are only detected in the result of a transformation (e.g., after
some rules did not fire in a topdown(try(s)) strategy).

For every rewrite rule, an unrestricted number of `with` and `where`
clauses can be used. In strategies, `with` can be used as a strategy
invocation, similar to `where` (e.g., `with(<may-not-fail> t)`).

### []{#Compiler_library} Compiler library

The compiler has been librarified. Program analysis and transformation
tools which work on Stratego code may now be based on the Stratego
compiler library. The intent is to make meta-programming with Stratego a
lot easier and speedup the Stratego compiler.

-   \[[STR-311](http://bugs.strategoxt.org/browse/STR-311)\] - strc-lib
    : a library for compilation (meta-programming) Stratego

[]{#Stratego_Language} Stratego Language
----------------------------------------

### []{#Assignment_operator} Assignment operator

An assignment operator has been added to the language as a more
attractive syntax for the common pattern `s => t`. In the assignment
operator, the variable name is now before the right-hand side. Also, the
right-hand side is a term pattern.

      get-signature(|file) :
        Method(_, returntype, name, types, _, _) -> 
        MethodSignature(cn, returntype, name, types)
        where
          cn := <get-classname> file

This used to be written as:

      <get-classname> file => cn

Note that this is a purely syntactic change: the variable can only be
assigned to once.

-   \[[STR-550](http://bugs.strategoxt.org/browse/STR-550)\] -
    Assignment operator

### []{#Dynamic_rules} Dynamic rules

#### []{#Improved_flow_sensitive_transfor} Improved flow-sensitive transformations

Thanks to Bogdan Dumitriu, the dynamic rule facility of Stratego has
been extended to deal with additional control flow constructs, including
break, break to label, continue and exceptions (try-catch-finally). Some
of the dynamic rule strategies, such as `dr-fix-and-intersect` and
`dr-fix-and-union` have been extended to work with labels, and new
dynamic rule prefixes `break-` and `break-to-label-` are introduced.

A
[presentation](ftp://ftp.strategoxt.org/pub/stratego/SUD06/sud06-bogdan.pdf)
from Stratego User Days 2006 provides a high-level walk-through.

#### []{#Scoped_global_variables} Scoped global variables

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

#### []{#Chained_dynamic_rules} Chained dynamic rules

A useful extension to the standard strategies generated for invoking
dynamic rules such as bagof-Foo, once-Foo, etc.

The idea is that it is in general useful to apply a sequence of dynamic
rules, but not produce all possible results, but chain each result to
the next dynamic rule invocation.

Suppose that you have two dynamic rules defined:

     Foo : x -> (1, x)
     Foo : x -> (2, x)

With these two rules defined, applying 0 will result in (2, (1, 0)).

In this way, you can apply a series of dynamic rules to a term. Note
that you can achieve this with repeat(once-Foo) as well, but once-Foo
will remove the rule from the environment, which is not always
desirable.

While chain-Foo only applies the rules visible in the current scope,
bigchain-Foo applies the rules from all scopes.

### []{#External_Constructor_Declaration} External Constructor Declarations

-   \[[STR-672](http://bugs.strategoxt.org/browse/STR-672)\]: fix
    multiple external definitions problems

While proper strategy definitions that are imported as externals are not
exported as externals from a library (as per August 2006), constructors
imported by a library, were also exported by that library. This caused
congruences to be regenerated, possibly not in that same library, but in
a library one step further in the import chain. Thus, the external
definitions for congruences from an imported library, prevented
generation of new congruences. However, since imported external
definitions are not exported, the next library does not see those
congruence definitions, and will re-generate them; giving rise to a
warning when the external definition for this new congruence is imported
in another application or library.

To solve this issue constructors are now treated in the same way as
strategy definitions.

There is now a notion of \"external\" constructor declarations. Syntax:

      external Foo : A * B -> C

These external constructor declarations are exported by a library along
with the external definitions for the strategies in the library. Thus,
importing libraries and programs can use these constructors in rules and
strategies.

However, external constructors are not exported from an importing
library. Just like external definitions are not exported from an
importing library. This entails that a third library that imports the
second, does not get the constructor declarations of the first. In order
to use those, the first library needs to be imported explicitly. Here is
an example:

    Library A
    -----------------
    module A
      constructors
        Foo : A
    ----------------->
    module libA
      constructors
        external Foo : A
    -----------------

    Library B
    -----------------
    module B
      imports libA
      strategies
        bar = !Foo()
        // constructor Foo is available through libA import
    ----------------->
    module libB
      strategies
        external bar
        // only strategy bar is exported, not constructor Foo
    -----------------

    Library or Application C
    -----------------
    module C
      imports libB
      strategies
        baz = !Foo(); ...; bar
              // error! libB does not export constructor Foo
    ------------------

    Library or Application C // corrected
    -----------------
    module C
      imports libB libA
      strategies
        baz = !Foo(); ...; bar
        // Foo is imported through libA
    ------------------

This change may break existing code; explicit imports of indirectly
imported libraries are needed. In practice, the change had a minimal
impact on the code in Stratego/XT and derived projects.

### []{#Rule_syntax_in_let} Rule syntax in let

The `let` construct now allows the defition of rules in addition to
strategies:

      let R : p1 -> p2
      in 
        ...
      end

### []{#Import_ATerm_from_file} Import ATerm from file

A new language construct called `import-term` was added which allows the
embedding of terms (data) directly into the program.

      get-pp-table = import-term(pptable.trm)

This removes the need for external data files, such as parse and
pretty-print tables. The resulting executable is self-contained, thus
making deployment of your program transformation tools easier.

-   \[[STR-577](http://bugs.strategoxt.org/browse/STR-577)\] - Stratego:
    support import of an ATerm from a file

[]{#Stratego_Libraries} Stratego Libraries
------------------------------------------

A new discipline for library naming and usage is introduces in 0.17. The
standard library is now named `libstratego-lib`, whereas the XTC library
is named `libstratego-xtc`. Additional libraries have been added for
parsing, pretty printing and term validation, see below.

### []{#Migrating_from_XTC_to_libraries} Migrating from XTC to libraries

To avoid the term serialization paid when composing transformation
pipelines using XTC, the compiler and all supporting tools have been
rearchitected as libraries in addition to the familiar XTC components.

For Stratego/XT users, the most significant change is that the SGLR
parser, the various RTG tools and the GPP tools are now available as
libraries, respectively named `libstratego-sglr`, `libstratego-rtg` and
`libstratego-gpp`.

The librarification allows parse tables to be loaded once, at startup,
and used repeatedly when multiple files must be parsed (when using XTC,
the parse table is loaded by the `sglr` child process every time a file
must be parsed).

Consider the following program:

    module foo
    imports
      libstratego-lib
      libstratego-sglr
    strategies
      main =
        tbl := <import-term(Exp.tbl); open-parse-table>
        ; <parse-string(|tbl)> "a+b"

It assumes the existence of a parse table (`Exp.tbl`). This table is
included into the program using the `import-term` construct (introduced
above). The call to `open-parse-table` will register the parse table
with the `libstratego-sglr` library, and subsequent calls to
`parse-string` will not need to reload the parse table.

Compiling and executing the program:

    $ strc -i foo.str $(strcflags stratego-lib stratego-sglr)
    $ ./foo 
    Plus(Var("a"),Var("b"))

The resulting program `foo` is now fully self-contained. It does not
need the `Exp.tbl` file to execute.

API documentation for the Stratego Libraries is available from the
Documentation page on the Stratego/XT website.

### []{#strcflags} strcflags

The new tool `strcflags` makes it no longer necessary to know all the
details of how to invoke the Stratego compiler when you\'re using a
certain library. Given the name of a package or Stratego library, the
tool returns the flags (such as include paths) for strc.

Example:

    $ strc -i foo.str $(strcflags stratego-lib)

You can also specify multiple packages. For example, if you\'re using
java-front, then you are usually using the Stratego library as well.

    $ strc -i foo.str $(strcflags stratego-lib java-front)

The tool strcflags is a simple wrapper around the tool `pkg-config`,
which we are using for configuring Stratego/XT packages when building
packages from source.

To support strcflags with your own packages, add a declaration of a
variable `strcflags` to the pkg-config `.pc` files.

### []{#Easy_library_creation} Easy library creation

Creating libraries using the Stratego compiler has never been easier. By
using the `--library` option to the compiler, all necessary library
files will be created.

    $ strc -i foo.str --library

The resulting output includes static and dynamic libraries, as well as
libtool support files:

    libfoo.a  libfoo.c  libfoo.la  libfoo.lo  libfoo.o  libfoo.rtree  libfoo.so 

This option is intended for creating libraries that are not part of an
autoconf/automake package, similar to invoking `strc` to compile a
program all the way to an executable.

[]{#Deployment} Deployment
--------------------------

This release brings about major improvements to the deployment
capabilities of Stratego/XT.

### []{#Standards_compliant_libraries} Standards-compliant libraries

The Stratego libraries expose various features from the underlying
platform Stratego/XT executes on. In 0.17, the library has been
refactored so that the dependence on platforms is clearer, and this
gives rise to several variants of the library, including one for C99,
POSIX and one for POSIX+XSI. The great majority of Stratego/XT programs,
use the high-level strategies for file and term I/O, and these programs
will be unaffected.

The main benefit of this change is that we can now build all the
Stratego libraries on platforms that only support functions from
standard C99 (i.e. not full POSIX). This enables the deployment of
Stratego applications on such platforms. Some strategies from the
Stratego library are only available in the POSIX and POSIX+XSI
extensions. The name of the modules defining these strategies reflect
this.

-   \[STR-613\] - Stratego library: Allow creation of library for
    specific standard (C99, POSIX, POSIX XSI)

### []{#Native_Windows_Support_MinGW}[]{#Native_Windows_Support_MinGW_} Native Windows Support (MinGW)

Stratego/XT now supports compiling natively on Microsoft Windows using
MinGW. This results in a smaller footprint because of significantly
fewer and smaller dependencies as compared with Cygwin.

Binaries created for MinGW can be deployed to Microsoft Windows users
without any dependencies.

For this purpose, the `stratego-libraries` package is also available
separately from Stratego/XT as source tarball and native Microsoft
Windows binaries. If you already have Stratego/XT, then there is no need
to install the `stratego-libraries`.

### []{#OSX_support} OSX support

Stratego/XT 0.17 now fully supports OSX on PowerPC as well as Intel
CPUs.

### []{#x86_64_support} x86-64 support

Thanks to patches from Eelco Dolstra, the ATerm library now supports
64-bit machines, and the final blocker preventing Stratego/XT running on
64-bit is now removed. This means 64-bit support is finally here. Binary
packages for 64-bit Linux distributions are provided for your
convenience.

-   \[[STR-698](http://yellowgrass.org/issue/StrategoXT/698)\] - x86\_64
    support

[]{#Detailed_List_of_Issues}[]{#_Detailed_List_of_Issues} Detailed List of Issues
---------------------------------------------------------------------------------

The full list of issues closed in this release is available at:

-   <http://yellowgrass.org/tag/StrategoXT/0.17>

[]{#Download_and_Installation}[]{#_Download_and_Installation} Download and Installation
---------------------------------------------------------------------------------------

The release page contains the source distributions, binary RPMs, and
detailed instructions on how to install the distributions:

-   <http://www.strategoxt.org/Stratego/StrategoRelease017>

[]{#Bugs_and_Known_Problems}[]{#_Bugs_and_Known_Problems} Bugs and Known Problems
---------------------------------------------------------------------------------

See our issue tracking systems for reports about (open) bugs:

-   <http://yellowgrass.org/project/StrategoXT>

Please report any problems with installation or bugs in the
implementation to our issue tracking system. Please check the existing
issues to see if a report about the problem was already submitted.

[]{#Contributions}[]{#_Contributions} Contributions
---------------------------------------------------

Developments, bug reports, and beta tests carried out by

-   Sigoure Benoit
-   Eric Bouwers
-   Martin Bravenboer
-   Arthur van Dam
-   Valentin David
-   Eelco Dolstra
-   Bogdan Dumitriu
-   Karl Trygve Kalleberg
-   Lennart Kats
-   Nicolas Pierron
-   Zef Hemel
-   Rob Vermaas
-   Eelco Visser

Thanks!

------------------------------------------------------------------------

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
