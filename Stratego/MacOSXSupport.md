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
    Page](http://www.program-transformation.org/edit/Stratego/MacOSXSupport?t=1536825598)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/MacOSXSupport)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/MacOSXSupport)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/MacOSXSupport?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/MacOSXSupport?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Stratego/MacOSXSupport?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/MacOSXSupport?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/MacOSXSupport?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/MacOSXSupport?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/MacOSXSupport?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/MacOSXSupport?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/MacOSXSupport)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/MacOSXSupport?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Stratego/MacOSXSupport?template=oopsmore&param1=1.8&param2=1.8)
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
[]{#Mac_OS_X_Intel} Mac OS X / Intel
------------------------------------

The latest unstable releases of Stratego/XT 0.17 support Mac OS X on
Intel machines. An experimental installer is available. See the
[announcement on the mailing
list](http://mail.cs.uu.nl/pipermail/stratego-dev/2006q2/001135.html).

Please note that Stratego/XT 0.16 does not support Mac OS X running on
Intel machines.

[]{#Mac_OS_X_PowerPC} Mac OS X / PowerPC
----------------------------------------

Stratego/XT supports Mac OS X on PowerPC from release 0.11. The release
page of the latest release contains links to binary distributions for
Mac OS X.

The performance of Stratego/XT at Mac OS X on PowerPC is rather poor.

-   The main reason for this is probably the architecture of the G4,
    which doesn\'t play too well with the implementation of choices
    (based on `jmp_buf`) in the Stratego compiler. The size of a
    `jmp_buf` depends on the architecture of the processor and
    unfortunately RISC processors need a very large `jmp_buf`.
-   Another reason might be the performance of nested functions. This
    will be solved when the Stratego compiler no longer uses nested
    functions for the implementation of lexical scope of strategies in
    Stratego.
-   Yet another reason is the performance of forking a process. Forking
    is much slower at Mac OS X (and Cygwin) then at a Linux system.

[]{#GNU_Linux_PowerPC} GNU/Linux / PowerPC
------------------------------------------

One of our master students (Dick Eimers) has installed Debian at a
PowerMac6,3 and I\'ve tried to build Stratego/XT on this machine. At
first this wasn\'t very succesful. I was using FSF\'s GCC 3.3.4 and this
resulted in the usual problems.

However, it works look a charm with GCC 3.4.1! Even more suprising to me
is the performance, which is excellent. The `jmp_buf` size at
Debian/PowerPC is much smaller than at Mac OS X!

      mbravenboer@mcflurry:~$ uname -a
      Linux mcflurry 2.4.25-powerpc #1 mer avr 14 15:38:38 CEST 2004 ppc GNU/Linux

      mbravenboer@mcflurry:~$ more /proc/cpuinfo
      processor       : 0
      cpu             : 7455, altivec supported
      clock           : 1249MHz
      revision        : 3.3 (pvr 8001 0303)
      bogomips        : 1245.18
      machine         : PowerMac6,3
      motherboard     : PowerMac6,3 MacRISC3 Power Macintosh
      board revision  : 00000001
      detected as     : 287 (Unknown Intrepid-based)
      pmac flags      : 00000000
      L2 cache        : 256K unified
      memory          : 512MB
      pmac-generation : NewWorld

      jmp_buf size: 364

`jmp_buf` size at same hardware, GCC 3.4.1 and running Mac OS X: 768

`jmp_buf` size at my SuSE 9.0 at Pentium M system is 156.

[]{#History_and_Future} History and Future
------------------------------------------

Mac OS X is support with a patched GCC from [StrategoXT
0.9.1](StrategoRelease093){.twikiLink}. This patch has been implemented
by [Eelco Dolstra](../Main/EelcoDolstra){.twikiLink}.

In Stratego/XT 0.17 we hope to remove nested functions in the C sources
produced by the Stratego Compiler (See issue
[STR-119](http://yellowgrass.org/STR-119)).

------------------------------------------------------------------------

[CategoryInstallation](CategoryInstallation){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
