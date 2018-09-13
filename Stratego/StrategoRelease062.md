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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease062?t=1536825560)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease062)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease062)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease062?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease062?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoRelease062?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease062?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease062?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease062)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease062?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease062?template=oopsmore&param1=1.2&param2=1.2)
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
Stratego Release 062 {#stratego-release-062 .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Stratego version 0.6.2 is now available from
[StrategoDownload](StrategoDownload){.twikiLink}

     released: October 6, 2001

     SUMMARY OF CHANGES

     (with respect to release 0.6)

     CONTRIBUTIONS

     * Bug reports by: Otto Skrove Bagge, Merijn de Jonge, Hedzer Westra
     * Bug repairs by: Merijn de Jonge

     LANGUAGE

     COMPILER

     * Added compile time option to generate code to trace strategies
       - --trace-all: trace all strategies
       - -t f: trace strategy f

     * Optimization is set to O2 by default (used to be O4). The higher
     optimization level (which comes down to inlining functions in addition
     to the O2 optimizations) seems to produce faulty code on some
     machine/compiler combinations. Optimization can be increased by
     passing the option -CI "O3" to SC. However, it seems appropriate to
     leave inlining decisions to SC.

     * Repair in implementation of dynamic rules; added rule stamp in order
     to record to which rule the information belongs.

     * Repair of compilation of overlays

     RUN-TIME SYSTEM

     * Repair of term explosion for strings (Merijn de Jonge)

     LIBRARY

     * Type annotations added to strategy operators with higher-order
     arguments.

     * Numerous small refactorings.
       
     * Some new tests

     * New
        - occurrences(s): all occurrence for which s succeeds
        - om-occurrences(s): outermost occurrences only

     * Obsolete: 
        - collect-kids/1 -> crush/3

------------------------------------------------------------------------

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 01 Oct 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
