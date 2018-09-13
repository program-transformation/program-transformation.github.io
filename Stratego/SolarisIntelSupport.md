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
    Page](http://www.program-transformation.org/edit/Stratego/SolarisIntelSupport?t=1536825669)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SolarisIntelSupport)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SolarisIntelSupport)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SolarisIntelSupport?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SolarisIntelSupport?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Stratego/SolarisIntelSupport?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/SolarisIntelSupport?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/SolarisIntelSupport?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/SolarisIntelSupport?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/SolarisIntelSupport?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/SolarisIntelSupport?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SolarisIntelSupport)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SolarisIntelSupport?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Stratego/SolarisIntelSupport?template=oopsmore&param1=1.5&param2=1.5)
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
Solaris Intel Support {#solaris-intel-support .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Solaris/x86 support is scheduled for
[StrategoXT](StrategoXT){.twikiLink} 0.9.4. Work has begun on
pinpointing what is different from already working systems.

The following packages are needed:

-   GNU m4
-   GNU autoconf
-   GNU automake
-   GCC
-   GNU make
-   teTeX

Advisable packages to install:

-   libiconv
-   GNU grep

You can get pre-compiled versions of these packages at
<http://www.sunfreeware.com/>

\-- [ArmijnHemel](../Main/ArmijnHemel){.twikiLink} - 25 Jun 2003

[StrategoXT 0.9.2](StrategoRelease092){.twikiLink} compiles on Solaris
8/x86. Still one problem with boxenv/latex. Boxenv assumes latex binary
is in \${LATEX}/bin/ , but the latex binary is not always located there.

\-- [RobVermaas](../Main/RobVermaas){.twikiLink} - 25 Jun 2003

The latex binary is now located by the configure script. Not yet tested
on Solaris however.

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 09 Dec
2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
