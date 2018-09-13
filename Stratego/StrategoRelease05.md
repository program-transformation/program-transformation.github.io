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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease05?t=1536825561)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease05)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease05)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease05?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease05?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoRelease05?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease05?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease05?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease05)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease05?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease05?template=oopsmore&param1=1.2&param2=1.2)
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
Stratego Release 05 {#stratego-release-05 .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

    Version 0.5

     released: March 26, 2001

     SUMMARY OF CHANGES 
     
     (with respect to release 0.4.22)

     * StrategoScript an interpreter for Stratego
     * Syntax clean up
     * Compiler and library maintenance
     * Website under TWiki
     * Online documentation
     * Stratego alpha release with anonymous CVS
     * Daily build

     INTERPRETER

     * StrategoScript is an interpreted language for strategic rewriting. 
       The interpreter has been designed for fast turn around time and
       not for performance; it will not replace the compiler. Possible
       applications are
      
       - learning Stratego
       - rapid prototyping
       - unit testing
       - glueing transformation components

     * A StrategoScript has the form

       #!/bin/sh stratego
       stratego script
       <commands and declarations>

       A script evaluates the commands and declarations sequentially. 
       Commands are strategy expressions that are applied to the current
       subject term. The starting term is the list of command-line options.
       Declarations are the usual declarations of signatures, overlays, rules, 
       strategies and imports that a normal Stratego module contains. In 
       addition a script can dump the current state of the intepreter and load 
       a previously dumped state. Thus, it is possible to load a previously 
       pre-compiled version of the library.

     * The implementation of the interpreter still lacks some features:
       - signatures and overlay declarations in scripts are not interpreted
       - nullary variables are not recognized without parentheses, i.e.,
         instead of Nil write Nil()
       - loading and precompiling modules should be more incremental

     * See doc/tutorial/exercises/pico for some example scripts

     LANGUAGE

     * Local strategy definitions 

         let f1(...) = s1 ... fn(...) = sn in s

       This means that the identifier "in" has become a reserved word. Use
       'in to indicate the identifier. Note that only strategy operators
       without arguments are supported in this release.

     * Syntax ?t <= s has been removed

     * Syntax << l -> r >> has been removed. For local rules of the form
       {x1,...,xn: <<l -> r>>} use \ l -> r \, if the xi correspond to the
       variables in l. Otherwise use {x1,...,xn: ?l; !r}.

     * Formerly reserved words are no longer reserved: match, build

     * operations keyword in signatures has been removed; use constructors

     COMPILER

     * Caching of symbols used when building terms (Arne de Bruijn)
     * Repaired bug in optimization rule for oncetd (Thanks Hedzer Westra)
     * Compiled specifications are now linked with optimized libraries.

     LIBRARY
      
     * uniq strategy now preserves order (Merijn de Jonge)
     * string-to-real and real-to-string conversion (Arne de Bruijn)
     * call now waits for all sub-processes to terminate (Merijn de Jonge)

     WEBSITE

     * The wiki server running the www.stratego-language.org website has been
       replaced by TWiki, a much more powerful wiki system. All pages from
       the old website (including pages that were not under wiki) have been
       moved to the new TWiki. Pages can be edited and new pages can be
       created by registered users; anyone can register.

     * The Stratego documentation (Tutorial, Reference Manual and Library)
       is now readable online at www.stratego-language.org; follow the
       links at StrategoDocumentation. The HTML is generated from LaTeX using
       HeVeA.

     CVS DISTRIBUTION

     * The latest developments in the Stratego system are now available
       via anonymous CVS. (Thanks Eelco Dolstra)

       To checkout the repository proceed as follows:

       % export CVSROOT=:pserver:anoncvs@losser.st-lab.cs.uu.nl:/home/cvsrepo
       % cvs login
       Password: anon
       % cvs checkout stratego

       Note that this distribution is very unstable.

     DAILY BUILD

     * The Stratego CVS distribution is now included in the daily build process
       at CWI (http://www.cwi.nl/~daybuild/dbs/). This will make it easier to
       release minor releases more often. Minor releases will now be made
       whenever relevant changes have been made and the daily build succeeds. 
       Minor releases will only be announced to the stratego-developers mailing
       list. Major releases will be made when enough significant changes have
       accumulated.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
