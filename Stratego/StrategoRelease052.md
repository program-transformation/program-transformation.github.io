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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease052?t=1536825681)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease052)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease052)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease052?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease052?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease052?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease052)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease052?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease052?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego Release 052 {#stratego-release-052 .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

    2001-04-13  Eelco Visser  <visser@acm.org>

       * spec/slib/spec/Makefile.am: Simplified makefile for library

       * spec/slib/spec/share-test.r: Defined test

    2001-04-12  Eelco Visser  <visser@acm.org>

       * bootinstall

       * resolved inconsistencies in repository

       * spec/back/s2c.r: translation of strategies to (idiomatic) C

       * spec/c: C signature and utitlities

       * spec/sc/sc: removed, is generated from sc.in

       * spec/slib/spec/scoped-finite-map.r: commented debugging code

       * spec/slib/spec/io.r: new-file creates a new not existing file
       name of the form c_n.tmp with c a character and n a number.

       * /spec/si/si.r: Changed display- operations to table-
       operations

       * spec/sc/proto-sc.r: Built in support for translation to
       idiomatic C code using s2c, PP-C and C-Format.

       * spec/slib/spec/list-set.r: typo

    2001-04-05  Eelco Visser  <visser@acm.org>

       * spec/slib/spec/string.r: <copy-char>(n,c) creates a string
       consisting of n copies of character c, which should be represented
       by its ascii code.

    2001-04-02  Hedzer Westra <hhwestra@cs.uu.nl>

       * new module: char.r for character strategies. includes
         char-test.r

    2001-04-02  Eelco Visser  <visser@acm.org>

       * spec/slib/spec/tables.r, display.r: Reorganized and documented
       the tables modules. The strategies formerly in the display module
       are now defined as normal "table" operations in the table module.
       Names have been normalized. Many operators have become obsolete.
       
       * spec/slib/spec/term-zip.r: Generic definition of zipping
       two term structures; can be used to implement pattern matching
       for example. 

       * spec/slib/spec/scoped-finite-map.r: Keeping track of scopes of
       table entries. Removing entries from tables is done automatically
       when the scope is exited. This is a candidate for support at the
       language level.
       
    2001-03-31  Eelco Visser  <visser@acm.org>

       * spec/slib/spec/list-set.r: Repaired bug in nrofoccs (Arne de
       Bruijn). foldr-kids is obsolete, use crush.

       * spec/slib/spec/list-set-test.r: Added test for nrofoccs

    2001-03-29  Hedzer Westra <hhwestra@cs.uu.nl>

            * extra library routines in options.r, list-basic.r and string.r
         (including tests)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
