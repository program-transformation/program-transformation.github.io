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
    Page](http://www.program-transformation.org/edit/Stratego/MicrosoftWindowsSupport?t=1536825600)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/MicrosoftWindowsSupport)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/MicrosoftWindowsSupport)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/MicrosoftWindowsSupport?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/MicrosoftWindowsSupport?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    14](http://www.program-transformation.org/view/Stratego/MicrosoftWindowsSupport?rev=1.14)
    [(diff 13)](http://www.program-transformation.org/rdiff/Stratego/MicrosoftWindowsSupport?rev1=1.14&rev2=1.13)
-   [Rev
    13](http://www.program-transformation.org/view/Stratego/MicrosoftWindowsSupport?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Stratego/MicrosoftWindowsSupport?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Stratego/MicrosoftWindowsSupport?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Stratego/MicrosoftWindowsSupport?rev1=1.12&rev2=1.11)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/MicrosoftWindowsSupport)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/MicrosoftWindowsSupport?template=oopsmore&param1=1.14&param2=1.14)
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
    \...](http://www.program-transformation.org/oops/Stratego/MicrosoftWindowsSupport?template=oopsmore&param1=1.14&param2=1.14)
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
Microsoft Windows Support {#microsoft-windows-support .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#StrategoXT} StrategoXT
--------------------------

On Microsoft Windows [StrategoXT](StrategoXT){.twikiLink} requires
Cygwin.

In [StrategoXT 0.9.4](StrategoRelease094){.twikiLink} all serious
problems on Microsoft Windows/Cygwin are solved. Standard tarball
distributions now can be installed without applying any patches. No
modifications of the srts are required and memory usage has been reduced
considerably. The solution to the issue was an optimization of the
choice implementation. The Stratego Runtime now allocates the jmp\_buf
storage on the heap and increases the size of the storage when
necessary. This has been implemented by [Eelco
Dolstra](../Main/EelcoDolstra){.twikiLink}.

Microsoft Windows+Cygwin support is not yet verified in the [daily
build](ContinuousBuild){.twikiLink}.

[]{#ATerm_library} ATerm library
--------------------------------

-   Installation of the ATerm library 2.0.x is no problem if configured
    \--with-gcc.

[]{#SGLR} SGLR
--------------

-   Installation of toolbus-lib, pt-support and [SGLR](SGLR){.twikiLink}
    is no problem.
-   check succeeds.

[]{#PGEN} PGEN
--------------

-   asf-support 1.0: no problem
-   asc-support 1.6: no problem
-   sdf-support 1.0: no problem
-   pgen 1.6: no problem (sdf2table is a shell-script)

------------------------------------------------------------------------

The following information does not concern the latest sources. It is a
log of the problems we encountered in the past.

------------------------------------------------------------------------

The [Stratego Run Time System](StrategoRunTimeSystem){.twikiLink} ( SRTS
) installs fine, but bootstrapped C sources compiled with the runtime
will cause a segementation fault on any invocation of a procedure in the
SRTS.

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 17 May
2003

Cygwin doesn\'t like this:

srts/src/stratego-choice.c :

      #define JMPBUFS 1638400
      jmp_buf jmpbufs[JMPBUFS];

The number of JMPBUFS is too large. Currently I\'m using 563840 for
testing purposes, but this might be a problem in heavy Stratego programs
(abox2text for example).

Does anybody know what might be the reasoning behind disallowing such
large arrays on Microsoft Windows/Cygwin?

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 19 May
2003

More complex Stratego program run if compiled with the adapted SRTS.
implode-asfix has been compiled to an .exe. The first step towards
[Microsoft Windows Support](MicrosoftWindowsSupport){.twikiLink} is a
binary distribution of sdf2. See [this
message](https://mail.cs.uu.nl/pipermail/stratego-dev/2003q2/000346.html)
on the [mailing list](MailingList){.twikiLink}.

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 19 May
2003

[StrategoXT 0.9.1](StrategoRelease091){.twikiLink} compiles on cygwin,
after changing the above (stratego-choice.c) and the removal of the
asource tool. Problem that occurs now is that in the
[XTC](XTC){.twikiLink} repository tools occur as follows:
(Tool(\"meta-explode.exe\"),\[(\"0.9.1\",\"/opt/strategoxt/bin/meta-explode.exe\")\]),
so with the extensions of executables.

\-- [RobVermaas](../Main/RobVermaas){.twikiLink} - 12 Jun 2003

bootstrap scripts (or shell scripts without an extension in general)
need to have a \'\#!\' as first characters to be executable on cygwin.

\-- [RobVermaas](../Main/RobVermaas){.twikiLink} - 16 Jun 2003

[XTC](XTC){.twikiLink} tools are registered properly now. Current
[LatestSources[^?^](http://www.program-transformation.org/edit/Stratego/LatestSources?topicparent=Stratego.MicrosoftWindowsSupport)]{.twikiNewLink
style="background : #FFFFCE;"} compile on cygwin, but only if you have
the right permissions (it fails at boxenv, when running \'latex
boxenv.ins\').

Don\'t be surprised if memory-usage goes up to 800 MB sometimes. We
should do somthing about this.

\-- [RobVermaas](../Main/RobVermaas){.twikiLink} - 16 Jun 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
