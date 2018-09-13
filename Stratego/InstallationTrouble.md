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
    Page](http://www.program-transformation.org/edit/Stratego/InstallationTrouble?t=1536825593)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/InstallationTrouble)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/InstallationTrouble)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/InstallationTrouble?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/InstallationTrouble?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/Stratego/InstallationTrouble?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Stratego/InstallationTrouble?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Stratego/InstallationTrouble?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/InstallationTrouble?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Stratego/InstallationTrouble?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/InstallationTrouble?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/InstallationTrouble)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/InstallationTrouble?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/Stratego/InstallationTrouble?template=oopsmore&param1=1.10&param2=1.10)
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
Installation Trouble {#installation-trouble .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

This page discusses common problems (or non-problems) with the
installation of Stratego on certain platforms.

------------------------------------------------------------------------

### []{#ATerm_Installation} ATerm Installation

(for Stratego/XT 0.14 and earlier)

I ran into a little trouble installing the most recent version of
Stratego, and I\'ve included the output which includes the error
message. This probably isn\'t terribly informative, but in case it\'s of
any use, I thought I\'d send it to you. I went ahead and installed an
earlier version instead and had no trouble doing so.

       /usr/bin/ld: cannot find -lATerm-gcc

This looks as if you didn\'t configure the
[ATermLibrary](../Tools/ATermLibrary){.twikiLink} with the `--with-all`
(or at least `--with-gcc`) flag or did not install it or did not
configure the Stratego installation with the right path to the aterm
library. Please check whether libATerm-gcc.a is installed in ATerm
prefix/lib.

------------------------------------------------------------------------

### []{#Athlon} Athlon

Stratego programs sometimes show random failure on Athlon machines. This
appears to be due to a combination of faulty motherboards in combination
with an old Linux kernel (before 2.4.16). It has nothing to do with the
Stratego compiler. Source:
[WesselDankers](../Main/WesselDankers){.twikiLink}.

------------------------------------------------------------------------

### []{#Mac_OS_X} Mac OS X

Stratego 0.6 and later versions did not work on early versions of Mac OS
X due to a big in the GCC compiler on the PowerPC. This issue has been
fixed in recent versions of Mac OS X (which you are probably running: we
are talking about ancient versions here). See also [MacOS X
Support](MacOSXSupport){.twikiLink}.

------------------------------------------------------------------------

\[From here this page is out of date, but some items still apply. Needs
refactoring \-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}
- 03 Jul 2003\]

------------------------------------------------------------------------

### []{#Cygwin} Cygwin

It seems that the problems with installation on Windows with Cygwin were
caused by the case-insensitiveness of Windows. This has been solved in
[StrategoRelease071](StrategoRelease071){.twikiLink}.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 21 Jun 2002

Dit heeft waarschijnlijk te maken met de afhandeleing van newlines en
cariage returns. Jurgen heeft hier aan gewerkt. Het probleem is dat
onder Cigwin files standard in text mode geopend worden waardoor er een
verkeerde translatie plaatsvindt: \\n =\> \\r\\n. Jurgen heeft dit
gefixt volgens mij in een recentere versie van de atermen door files
altijd expliciet in binary mode te openen.

Misschien weet hij een workaround voor dit probleem anders moeten we
maar proberen over te stappen op versie 1.6.4 van de atermen. \-\--
[MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink}

The gist of the above: installation of the
[ATermLibrary](../Tools/ATermLibrary){.twikiLink} on Cygwin runs into
trouble with end of line treatment. This appears to be solved with later
versions of the library (starting at 1.6.4).

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 30 Nov 2001\

------------------------------------------------------------------------

### []{#Irix} Irix

Tried bootstrapping 0.6.3, using aterm 1.6.3 on irix-mips-6.5 just now.

I used the gcc-3.0.1 compiler, freshly compiled for the occasion.

To get aterm to build, I had to reduce CFLAGS\_GCC from -O4 to -O2, lest
the gcc compiler crash on compilation of bafio.c

Building stratego got me this far:

    gmake[3]: Entering directory
    `/mnt/mldwork/work/karltrk/stratego-0.6.3/sc/spec/syn'
    Makefile:408: no file name for `include'
    /work/karltrk/apps/bin/sc -I ./../sig -i pack-stratego
    ### cannot find term Cons(...(2)) at 104d8b70 in hashtable at pos 45342,
    header = 3880

This seems consistent with a bug in aterm, as I had a similar problem
before on linux.

Any ideas on how to take this further ? Is it a known problem, or should
I just break out the jolt cola and prepare for a long night debugging ?

\-- [KarlTrygveKalleberg](../Main/KarlTrygveKalleberg){.twikiLink} - 14
Dec 2001

The gcc people have been able to reproduce this bug with -O2 also, you
might have better luck turning off all optimisation. Eelco, have you
heard anything more regarding this bug? I got a mail a week or two ago
saying they had merge my bug report with yours.

I\'ve had no luck compiling Stratego with gcc-3.0 on Irix, and compiling
with 2.95.x just hangs.

\-- [OttoSkroveBagge](../Main/OttoSkroveBagge){.twikiLink} - 14 Dec 2001

------------------------------------------------------------------------

### []{#0_7beta2_on_non_Intel_platforms} 0.7beta2 on non-Intel platforms

Stratego 0.7beta2 doesn\'t work on some platforms at the moment. The
bootstrapped compiler works correctly, except that the `s2c` stage (the
translation to abstract C code) generates corrupt output. This has been
observed on `mips-*-linux` and `sparc-sun-solaris2.6`. Cause: unknown.

\-- [EelcoDolstra](../Main/EelcoDolstra){.twikiLink} - 26 Feb 2002

------------------------------------------------------------------------

[CategoryInstallation](CategoryInstallation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
