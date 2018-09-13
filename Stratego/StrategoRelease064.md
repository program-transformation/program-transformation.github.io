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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease064?t=1536825546)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease064)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease064)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease064?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease064?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoRelease064?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease064?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease064?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease064)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease064?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease064?template=oopsmore&param1=1.2&param2=1.2)
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
Stratego Release 064 {#stratego-release-064 .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Stratego 0.6.4 is now available from

-   <http://www.stratego-language.org>

The release fixes a \"fikse bug in Stratego!!\" in the translation of
Strategy Rules (rules of the form

      L :: s1 --> s2 where s3
    </verbatim>). Thanks to Hedzer for letting me know. See 

       * http://www.stratego-language.org/Stratego/StrategyRule

    for more about these rules. Since it is not widely advertised feature, it
    doesn't probably affect your specifications and it will be safe to wait until
    the next release, which will have some new goodies again.

    -- Main.EelcoVisser - 03 Jan 2002 <br />

    -------

    <verbatim>
    Version 0.6.4

     released: January 3, 2002

    SUMMARY OF CHANGES

     (with respect to release 0.6)

     * Term wrap syntax generalizes split
     * Term project syntax generalizes projection
     * New library strategies
     * Tracing of evaluation
     * CGEN package adapted to grammar identifiers
     * New version of gpp
     * Several bug repairs
     * Anonymous CVS checkout is possible again
     * Website runs new twiki

    CONTRIBUTIONS

     * Bug reports by Otto Skrove Bagge, Robert Feldt (configuration),
       Merijn de Jonge (strings & #), Hedzer Westra
     * Bug repairs by Merijn de Jonge (strings & #)
     * Library contributions by Otto Skrove Bagge (insert), 
       Martin Bravenboer
     * CVS support by Henk van Lingen
     * Web hosting by Henk Penning

    LANGUAGE

     * Term patterns can contain strategy applications <s>. 

     * Term wrap patterns simplify wrapping some complex constructor pattern
       around a term. For instance, split(f,g) can now be written as
       !(<f>,<g>), and this generalizes to arbitrary build patterns.

     * Term project patterns simplify projection of sub-terms. A strategy
       application <s> inside a match pattern selects the corresponding sub-term
       and applies s to it. For example, instead of writing 
       \ Typed(Var(x),_) -> x \ it is now possible to write ?Typed(Var(<id>),_)
       This feature can also be used to perform tests on subterm in a
       match pattern, e.g., the pattern ?[x | <not([])>] binds the head of a list
       to x, checks that the tail is not empty and produces the tail as
       result.

    COMPILER

     * Improved efficiency of needed
       definition extraction by using dynamic rules instead of a list of
       definitions to look up definitions in. The effect of this change
       is that the order of evaluation of definitions for the same label
       is reversed.  This is fine since the order of evaluation of
       rules/definitions with the same name is undefined, but it might
       break some specifications. It might be a good idea to change the
       evaluation order with every distribution in order to force
       programmers to use left choice when the order is relevant.

     * Added compile time option to generate code to trace strategies
       - --trace-all: trace all strategies
       - -t f: trace strategy f
       - Note: -t option does not work properly yet.

     * Optimization is set to O2 by default (used to be O4). The higher
       optimization level (which comes down to inlining functions in addition
       to the O2 optimizations) seems to produce faulty code on some
       machine/compiler combinations. Optimization can be increased by
       passing the option -CI "O3" to SC. However, it seems appropriate to
       leave inlining decisions to SC.

     * Repair in implementation of dynamic rules; added rule stamp in order
       to record to which rule the information belongs.

     * Repair of compilation of overlays

     * New version of GPP in GPP-BOOT

     * CGEN now supports GB grammar identifiers

     * Repaired bug in compilation of :: --> rules (Hedzer Westra)

    LIBRARY

     * Repair of term explosion for strings (Merijn de Jonge). Quoted
       identifiers (strings) can now be used as constructor symbols.
       Not yet supported in signatures.
     * Type annotations added to strategy operators with higher-order
       arguments.
     * Numerous small refactorings, including
        - memo in terms of dynamic rules
     * Some new tests
     * New
        - occurrences(s): all occurrence for which s succeeds
        - om-occurrences(s): outermost occurrences only
        - collect-all(s): collect all occurrences
        - collect-om(s): collect outermost occurrences only
        - innermost-memo(s): memoization of intermediate results
        - restore(s,r): always perform restoration r after doing s,
          even when s fails
     * Obsolete: 
        - collect-kids/1 -> crush/3

    DISTRIBUTION

     * The Stratego CVS repository is accessible again. To check out the contents
       of the repository type:

          cvs -d :pserver:anonymous@cvs.cs.uu.nl:/data/cvs-rep checkout Stratego

       Thanks to Henk van Lingen for setting up the cvs server.

     * If you would like to get involved in development of the compiler or library,
       it is also possible to obtain write access to the repository. Contact me
       if you're interested.

    WEBSITE

     * The twiki running the website has moved from losser to the production server
       of the Utrecht University CS department. Thanks to Henk Penning for making 
       this possible. Individual pages are now bookmarkable under the 
       stratego-language.org URL. Access control has been improved. Users need to 
       re-register to enter a password.
    </verbatim>
    -----
    ReleasePlan | StrategoDownload

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
