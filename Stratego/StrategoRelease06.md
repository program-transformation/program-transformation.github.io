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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease06?t=1536825547)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease06)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease06)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease06?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease06?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Stratego/StrategoRelease06?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease06?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/StrategoRelease06?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease06?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/StrategoRelease06?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease06?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease06)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease06?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease06?template=oopsmore&param1=1.8&param2=1.8)
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
Stratego Release 06 {#stratego-release-06 .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

See also

-   [StrategoRelease061](StrategoRelease061){.twikiLink}
-   [StrategoRelease062](StrategoRelease062){.twikiLink}
-   [StrategoRelease063](StrategoRelease063){.twikiLink}

<!-- -->

     Stratego version 0.6 is available from www.stratego-language.org
     
     SUMMARY OF CHANGES
     
     (with respect to release 0.5)
     
     * A new compilation scheme has been implemented. The compiler
       now compiles to C with nested functions (a GCC extension). Choices
       are handled using setjmp/longjmp. The new scheme makes it very easy
       to write foreign functions that can be used in Stratego programs,
       or to call Stratego strategies from C functions. Both compilation
       and generated code are much faster.
     
     * Dynamic rules make it possible to generate context-specific rules
       at run-time. This is useful for many transformations, including
       inlining, dead code elimination, and variable renaming. A rule
       is generated at the place where the information (e.g., a function
       declaration) is available, and can be used at any other place (e.g.
       a function call site). See the paper "Scoped Dynamic Rewrite Rules"
       to be presented at the RULE'01 workshop for examples.
     
     * The distribution has been split up into a distribution of the
       run-time system, the library, and the compiler. In addition a
       package for generation of C code is used. Thus to install Stratego
       you now need the following packages:
     
            - srts     : Stratego Run-Time System
            - ssl      : Stratego Standard Library
            - sc-boot  : Stratego Compiler (bootstrapped C sources)
            - gpp-boot : Generic Pretty-Printing utilities (bootstrapped C sources)
            - cgen     : C generation utilities
            - sc       : Stratego Compiler (Stratego sources)
     
       In addition the following external packages are required
     
            - aterm : ATerm library
            - gpp   : generic pretty-printing
     
       These packages are also available as a single integrated package produced
       with autobundle:
     
            - stratego-0.6
     
     * The documentation of Stratego is not part of any of these packages at
       the moment. New documentation is in the making.
     
     CONTRIBUTIONS
     
     * Eelco Dolstra traced the problem of using nested functions on Sun machines
       to the executability of code on the stack, and pointed out the solution using   mprotect.
     
     * Merijn de Jonge tested the new distribution on various machines and
       provided an extension of the run-time system to call mprotect when
       necessary.
     
     * Arne de Bruijn, Merijn de Jonge, and Hedzer Westra contributed various
       strategies to the library.                                                   
     * The new compiler was implemented by Eelco Visser
     
     LANGUAGE
     
     * Dynamic rules: a new feature that allows generation of rules a run-time.
       Dynamic rules are explained in the paper "Scoped Dynamic Rewrite Rules"
       to be presented at the RULE'01 workshop.
     
     * Recursive strategy definitions are now fully supported.
     
     * The syntax has been liberalized: rule and strategy definition can
       now be defined under both the rules and strategies keywords. In effect,
       rules and strategy definitions can be mixed in any order.
     
     * Constructor declarations are required for all constructors used in a
       specification. A term that is transformed can still contain other
       constructors, though.
     
     * Type annotations for higher-order arguments of strategy operators.
       Strategy operators (instead of strategies) can now be passed to strategy
       operators. This requires that the argument of the strategy operator is
       given a proper type annotation.
     
     * Primitive strategies that are implemented in C should be called with
       all their arguments: ?n; prim("SSL_exit", n) instead of prim("SSL_exit")
     
     COMPILER
     
     * The Stratego Compiler is distributed separately in the SC package
     
     * The compiler uses a new translation scheme producing idiomatic,
       high-level C code. The C stack is used instead of dedicated stacks.
       Setjmp and longjmp are used to implement choice. The GCC extension
       of C with nested functions is used to represent strategies to be
       passed to strategies (using function pointers). As a result of these
       changes, C compilation time has been reduced drastically. Also
       generated code is much faster than before.
     
     * The CGEN package supports generation (pretty-printing) of C code.
       It is available as a separate package and could be used in other
       projects.
     
     * The names of the generated C functions are the same as the original
       names in the specification, making inspection of the generated code
       possible. Also the new compilation scheme makes it easy to link
       generated code with other C code. For example, to use external
       C functions in Stratego programs, or to call Stratego transformations
       from C code.
     
     * Because of the new implementation scheme, much less inlining has
       to be done. This is beneficial for code size, and thus compilation
       time, but a number of optimizations opportunities are thereby missed.
       More aggresive optimization and separate compilation are issues for
       a future version. Also the fusion of the innermost strategy with
       rules is not yet integrated with the new compiler.
     
     RUN-TIME SYSTEM
     
     * The Stratego Run-Time System is distributed separately in the SRTS package.
     
     * The run-time system has been reduced to the definition of the
       generic traversal operators and an interface to the choice mechanism
       (setjmp/longjmp currently). Most of the work is done by the ATerm library.   

     LIBRARY
     
     * The Stratego Standard Library is now distributed separately in the
       SSL package. Lots of new library strategies have been added since
       Version 0.5. Many strategies are now documented by means of executable
       tests in the -test.r modules. All library modules were redocumented.
     
     * scoped-finite-map.r:  Keeping track of scopes of table entries. Removing
       entries from tables is done automatically when the scope is exited. This
       module provides the basis for the implementation of dynamic rules.
     
     * tables.r: Reorganized and documented the tables modules. The strategies
       formerly in the display module are now defined as normal "table" operations
       in the table module. Names have been normalized. Many operators have become
       obsolete.
     
     * tables.c: primitive operations more robust; no need to initialize
       tables
     
     * char.r: utilities for character manipulation
     
     * term-zip.r:  Generic definition of zipping two term structures; can be
       used to implement pattern matching, for example.
     
     * io.r: new-file
     
     * string.r: string comparison (Hedzer), repaired basename (Merijn)
     
     * env-traversal.r: traversals involving one
     
     * apply.r
     
     * LayoutPreserve.r, SList.r, LList.r: abstract syntax with layout
     
     * options.r: New strategy iowrap/3 is also parameterized with a
       strategy for printing usage information. Other variants are
       implemented in terms of this one. (Merijn de Jonge)
       The iowrapO operators have been renamed to iowrap.
     
     * list-set.r: Repaired bug in nrofoccs (Arne de Bruijn).
     
     * list-filter.r: partition                                     
     
     * foldr-kids is obsolete, use crush.
     
     CVS DISTRIBUTION and DAILY BUILD
     
     * A new CVS repository has been created for the new set-up of the compiler.
       The CVS repository is not yet publicly accessible. The Stratego compiler
       is automatically build in the daily builds at CWI: http://www.cwi.nl/~daybuild/

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
