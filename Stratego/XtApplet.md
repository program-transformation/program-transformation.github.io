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
    Page](http://www.program-transformation.org/edit/Stratego/XtApplet?t=1536825460)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/XtApplet)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/XtApplet)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/XtApplet?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/XtApplet?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Stratego/XtApplet?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/XtApplet?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Stratego/XtApplet?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/XtApplet?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/XtApplet?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/XtApplet?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/XtApplet)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/XtApplet?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Stratego/XtApplet?template=oopsmore&param1=1.9&param2=1.9)
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
XT Applet {#xt-applet .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

XT Applet is a small package configured with automake that you can use
to get started with writing Stratego/XT applications. The `src/`
subdirectory contains a sample [SDF2](../Sdf/WebHome){.twikiLink}
definition and a tiny Stratego transformation. The `Makefile.am`
contains generic make rules for applying these. The packages also
illustrates the use of [AutoXT](AutoXT){.twikiLink} and
[XTC](XTC){.twikiLink}.

The latest distribution is available at:

-   <http://releases.strategoxt.org/xt-applet-unstable-latest/>

Currently, this distribution is created for [Stratego/XT
0.14](StrategoRelease014){.twikiLink}

Older releases:

-   <http://www.stratego-language.org/ftp/xt-applet-0.3.tar.gz>

[]{#Short_Introduction} Short Introduction
------------------------------------------

`Trafo` is an ATerm to ATerm utility. You can just pass an expression in
plain concrete syntax to it. It has to be parsed first:

    $ sglri -i test1.exp -p Exp.tbl | ./Trafo
    Plus(Id("abc"),Bracket(Plus(Id("hij"),Mul(Bracket(Plus(Id("jkl"),Id("ghi"))),Id("def")))))

`exp-transform` is the right tool to pass expressions in concrete syntax
to. It implements the complete pipeline from expression to expression.
Note: `exp-transform` only works after installation. You can choose:
install the package, or specify the build time [XTC](XTC){.twikiLink}
repository:

    XTC_REPOSITORY=../XTC ./exp-transform -i test1.exp

or just (after installation)

    $ ${xt-applet-prefix}/bin/exp-transform -i test1.exp

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.XtApplet moved from Stratego.GetStartedWithXtApp on 04 Mar
2002 - 00:21 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put
it
back](http://www.program-transformation.org/rename/Stratego/XtApplet?newweb=Stratego&newtopic=GetStartedWithXtApp&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
