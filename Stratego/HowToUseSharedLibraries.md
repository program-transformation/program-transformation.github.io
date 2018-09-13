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
    Page](http://www.program-transformation.org/edit/Stratego/HowToUseSharedLibraries?t=1536825587)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/HowToUseSharedLibraries)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/HowToUseSharedLibraries)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/HowToUseSharedLibraries?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/HowToUseSharedLibraries?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/HowToUseSharedLibraries?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/HowToUseSharedLibraries?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/HowToUseSharedLibraries?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/HowToUseSharedLibraries?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/HowToUseSharedLibraries?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/HowToUseSharedLibraries)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/HowToUseSharedLibraries?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/HowToUseSharedLibraries?template=oopsmore&param1=1.3&param2=1.3)
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
How To Use Shared Libraries {#how-to-use-shared-libraries .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

From [StrategoXT 0.11](StrategoRelease011){.twikiLink} the Stratego
Runtime creates libraries using Libtool. This means that both static and
shared libraries are constructed (on platforms that support shared
libraries). In general, linkers prefer shared libraries over static
libraries, thus Stratego programs will be linked with shared libraries.

This introduces the usual advantages and disadvantages of shared
libraries. For example, an advantage is that executables are smaller and
the code of the runtime is shared. The main disadvantage is that the
libraries need the be found when the executable is invoked. This is a
common problem for all packages that are using shared libraries.

Some methods to avoid the disadvantages are:

-   Use Libtool for linking in your package that uses StrategoXT.
    Libtool will add the directories of dynamic libraries to the search
    path of the executables. This solves the problem of run-time lookup
    of a shared library that is not installed in a default directory for
    libraries at your system. To use Libtool in your package, just add
    AC\_PROG\_LIBTOOL to your `configure.in` (or `configure.ac`).

<!-- -->

-   If programs are not linked in this way, then the user can set the
    `LD_LIBRARY_PATH` to include the location of the Stratego runtime
    libraries in the StrategoXT installation.

<!-- -->

-   If you just hate dynamic libraries, then you can configure
    StrategoXT with the standard Libtool option `--disable-shared`:
    `./configure ... --disable-shared`. This will only construct static
    libraries. All your programs (also in your own packages) will now
    use static linking, since there no shared libraries available.

<!-- -->

-   If your [StrategoXT](StrategoXT){.twikiLink} installation contains
    shared libraries, but you don\'t want the programs in your package
    to use them, then you can enforce static linking by passing the
    `-static` option to the configure of your package: `LDFLAGS`:
    `./configure ... LDFLAGS=-static`.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
