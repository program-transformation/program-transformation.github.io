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
    Page](http://www.program-transformation.org/edit/Stratego/SolarisUltraSparcSupport?t=1536825670)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SolarisUltraSparcSupport)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SolarisUltraSparcSupport)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SolarisUltraSparcSupport?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SolarisUltraSparcSupport?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/SolarisUltraSparcSupport?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/SolarisUltraSparcSupport?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/SolarisUltraSparcSupport?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SolarisUltraSparcSupport)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SolarisUltraSparcSupport?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/SolarisUltraSparcSupport?template=oopsmore&param1=1.2&param2=1.2)
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
Solaris Ultra Sparc Support {#solaris-ultra-sparc-support .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The
[UltraSparc[^?^](http://www.program-transformation.org/edit/Stratego/UltraSparc?topicparent=Stratego.SolarisUltraSparcSupport)]{.twikiNewLink
style="background : #FFFFCE;"} platform is the 64 bit version of the
Sparc platform. It (and the Solaris operating system) can handle both 32
bit and 64 bit executables. The default compile target for compilers
available on Solaris on
[UltraSparc[^?^](http://www.program-transformation.org/edit/Stratego/UltraSparc?topicparent=Stratego.SolarisUltraSparcSupport)]{.twikiNewLink
style="background : #FFFFCE;"} is to compile 32 bit binaries. To compile
64 bit binaries you need to specify special flags for the compiler.
Compiling and using Stratego in 32 bit mode is no problem. For 64 bit
support there still are a few problems:

The ATerm library doesn\'t yet compile cleanly in 64 bit mode:

-   some of the tests fail, this is most likely a forgotten \#ifdef in
    one of the tests
-   there is rudimentary support for 64 bit compiles in the
    autoconf/automake rules, but cleanups are needed (options for 64 bit
    are not propagated to debug and profiling variants)
-   different compilers (Sun workshop, gcc) need to be tested and
    supported (which is not trivial to get right, because they all of
    different flags for 64 bit compiles)

After that all the other tools need to be checked for 64 bit safeness.

Please note, gcc 2.95.\* cannot generate good 64 bit code for
[UltraSparc[^?^](http://www.program-transformation.org/edit/Stratego/UltraSparc?topicparent=Stratego.SolarisUltraSparcSupport)]{.twikiNewLink
style="background : #FFFFCE;"}!!! (For more information about this, the
mailinglists for Linux on
[UltraSparc[^?^](http://www.program-transformation.org/edit/Stratego/UltraSparc?topicparent=Stratego.SolarisUltraSparcSupport)]{.twikiNewLink
style="background : #FFFFCE;"} is probably your best bet.) Use a recent
gcc 3.x instead.

\-- [ArmijnHemel](../Main/ArmijnHemel){.twikiLink} - 12 Jan 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
