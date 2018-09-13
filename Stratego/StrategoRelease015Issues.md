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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease015Issues?t=1536825680)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease015Issues)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease015Issues)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease015Issues?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease015Issues?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoRelease015Issues?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease015Issues?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease015Issues?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease015Issues)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease015Issues?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease015Issues?template=oopsmore&param1=1.2&param2=1.2)
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
Stratego Release 015 Issues {#stratego-release-015-issues .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Release Notes - Stratego/XT - Version 0.15 (Stratego Core Compiler
Experimental)

[]{#Bug} Bug
------------

-   \[[STR-220](http://yellowgrass.org/STR-220)\] - syntax priority
    issue: \'s1 \< s2 + s3 + s4\' is ambiguous
-   \[[STR-224](http://yellowgrass.org/STR-224)\] - Term projection in
    annotations is broken
-   \[[STR-235](http://yellowgrass.org/STR-235)\] - Syntactical
    ambiguity with higher order arguments
-   \[[STR-264](http://yellowgrass.org/STR-264)\] - collect-all: recurse
    to current term instead of children of current term
-   \[[STR-290](http://yellowgrass.org/STR-290)\] - concat-strings seg
    fault
-   \[[STR-293](http://yellowgrass.org/STR-293)\] - strc tests:
    Makefile.am must use XT\_DARWIN
-   \[[STR-318](http://yellowgrass.org/STR-318)\] - format-check fails
    when reporting incorrect types at top-level (start-symbols)
-   \[[STR-322](http://yellowgrass.org/STR-322)\] - Concatenation of two
    iter-star-sep lists is not imploded.

[]{#New_Feature} New Feature
----------------------------

-   \[[STR-111](http://yellowgrass.org/STR-111)\] - pptable-diff:
    consider number of arguments in pp rule
-   \[[STR-164](http://yellowgrass.org/STR-164)\] - Let: support rule
    syntax
-   \[[STR-316](http://yellowgrass.org/STR-316)\] - Old style dynamic
    rules no longer supported

[]{#Task} Task
--------------

-   \[[STR-5](http://yellowgrass.org/STR-5)\] - Automate creation of
    binary distributions for Microsoft Windows + Cygwin.
-   \[[STR-58](http://yellowgrass.org/STR-58)\] - Stratego Core Language
-   \[[STR-307](http://yellowgrass.org/STR-307)\] - Move
    stratego-desugar from stratego-front to strc-core
-   \[[STR-313](http://yellowgrass.org/STR-313)\] - Build order of
    stratego-front and stratego-lib
-   \[[STR-315](http://yellowgrass.org/STR-315)\] - Merge improvements
    to strc with strc-core
-   \[[STR-319](http://yellowgrass.org/STR-319)\] - Update meta-explode
    to Stratego-Sugar abstract syntax
-   \[[STR-321](http://yellowgrass.org/STR-321)\] - List variables in
    concrete syntax and abstract syntax should have \* suffix
-   \[[STR-324](http://yellowgrass.org/STR-324)\] - Disable build of
    sig2rtg

[]{#Improvement} Improvement
----------------------------

-   \[[STR-210](http://yellowgrass.org/STR-210)\] - Conc support: conc
    the Conc arguments in build.
-   \[[STR-217](http://yellowgrass.org/STR-217)\] - Emacs mode: support
    fill-paragraph (alt-q) of xdoc comments
-   \[[STR-219](http://yellowgrass.org/STR-219)\] - Emacs mode: abstract
    syntax buffer for concrete objects syntax
-   \[[STR-242](http://yellowgrass.org/STR-242)\] - Define native ssl
    functions as external definitions
-   \[[STR-278](http://yellowgrass.org/STR-278)\] - ppgen: incorrect
    report of missing constructor
-   \[[STR-279](http://yellowgrass.org/STR-279)\] - conc-strings:
    support tuples of \>2 strings
-   \[[STR-310](http://yellowgrass.org/STR-310)\] - remove obscure
    features

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
