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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease053?t=1536825681)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease053)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease053)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease053?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease053?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease053?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease053)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease053?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease053?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego Release 053 {#stratego-release-053 .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Changes since [StrategoRelease052](StrategoRelease052){.twikiLink}

    2001-05-22    <visser@acm.org>

       * bootinstall
       
       * bootstrap

       * spec/slib/spec/sunit.r: Replaced FAIL with fail. fail should be
       safe, i.e., not eliminate actions with side-effects.

       * spec/slib/spec/options.r: typo

     2001-05-20    <visser@acm.org>

       * spec/slib/spec/iteration.r: Import conditional

       * spec/slib/spec/conditional.r: Else branch of if is not
       called when the then branch fails, only when the condition
       fails. (Using cut construct from RhoStratego.)

    2001-05-18    <visser@acm.org>

       * src/front/Makefile.am (inline_SOURCES): inline.c instead of
       inlining.c. This caused bug in (not) renaming of let
       expressions. (Thanks Arne de Bruijn)

    2001-05-12    <visser@acm.org>

       * bootinstall

    2001-05-11    <visser@acm.org>

       * spec/slib/spec/char.r,string.r: Typos, forgotten import 

    2001-05-11  Hedzer Westra <hhwestra@cs.uu.nl>

       * added parsing of negative Integers

       * fixed char.r and string.r (which Eelco did too..)

       * bugfixed LayoutPreserve.r (not finished yet, though)

    2001-05-10  Hedzer Westra <hhwestra@cs.uu.nl>

       * added inc and dec rules to integers.r (fix for apply-test.r)

    2001-05-08  Hedzer Westra <hhwestra@cs.uu.nl>

       * added strategies to char.r, int-list.r, list-set, string.r

       * added expect.r

       * added SList.r, LList.r, LayoutPreserve.r

       * added these files to doc/library/body.ltx

       * re-added previous changes, hope I did it right now :-)

    2001-04-23  Hedzer Westra <hhwestra@cs.uu.nl>

       * added apply.r and apply-test.r to library

       * added is-interval and int-sort to int-list

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
