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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease016M1Issues?t=1536825681)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease016M1Issues)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease016M1Issues)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease016M1Issues?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease016M1Issues?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease016M1Issues?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease016M1Issues)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease016M1Issues?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease016M1Issues?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego Release 016 M1 Issues {#stratego-release-016-m1-issues .twikiTopicTitle}
==============================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Release Notes - Stratego/XT - Version 0.16M1 (bugs in 0.15)

[]{#Bug} Bug
------------

-   \[[STR-85](https://bugs.cs.uu.nl/browse/STR-85)\] - Sloppy
    variable-scope in let-strategies
-   \[[STR-145](https://bugs.cs.uu.nl/browse/STR-145)\] - Shared
    libraries are not shared at Cygwin: static linking is used.
-   \[[STR-301](https://bugs.cs.uu.nl/browse/STR-301)\] - Check
    implementation of quoted constructors
-   \[[STR-326](https://bugs.cs.uu.nl/browse/STR-326)\] - File foo not
    removed during configure
-   \[[STR-327](https://bugs.cs.uu.nl/browse/STR-327)\] -
    XT\_CHECK\_STRATEGOXT\_UTILS should use pkgconfig.
-   \[[STR-329](https://bugs.cs.uu.nl/browse/STR-329)\] - use-def
    complains about unbound variables
-   \[[STR-331](https://bugs.cs.uu.nl/browse/STR-331)\] -
    stratego-warning: missing build operator
-   \[[STR-335](https://bugs.cs.uu.nl/browse/STR-335)\] - Typing bug
    with 0.15 strc
-   \[[STR-338](https://bugs.cs.uu.nl/browse/STR-338)\] - strc prints
    \"SSL\_printnl: argument not a list\" to stderr for unclear reasons.
-   \[[STR-343](https://bugs.cs.uu.nl/browse/STR-343)\] - Linking
    problem for identity Stratego program at Mac OS X
-   \[[STR-344](https://bugs.cs.uu.nl/browse/STR-344)\] - Stratego
    libraries should declare interlibrary dependencies
-   \[[STR-382](https://bugs.cs.uu.nl/browse/STR-382)\] - rm-annotations
    does not remove annotations

[]{#New_Feature} New Feature
----------------------------

-   \[[STR-320](https://bugs.cs.uu.nl/browse/STR-320)\] - Option for
    preferring .str files over .rtree files
-   \[[STR-325](https://bugs.cs.uu.nl/browse/STR-325)\] - Overlay bodies
    should be pure term expressions
-   \[[STR-345](https://bugs.cs.uu.nl/browse/STR-345)\] - stratego
    runtime libraries must be self-contained
-   \[[STR-346](https://bugs.cs.uu.nl/browse/STR-346)\] - Calling
    strategies by their name
-   \[[STR-351](https://bugs.cs.uu.nl/browse/STR-351)\] - checksum
-   \[[STR-361](https://bugs.cs.uu.nl/browse/STR-361)\] - autoxt:
    introduce support for pkg\_STRCFLAGS variables
-   \[[STR-371](https://bugs.cs.uu.nl/browse/STR-371)\] - \--statistics
    option
-   \[[STR-375](https://bugs.cs.uu.nl/browse/STR-375)\] - Support
    dynamic linking on Cygwin
-   \[[STR-383](https://bugs.cs.uu.nl/browse/STR-383)\] - standalone
    strc: don\'t use a search path for libraries

[]{#Task} Task
--------------

-   \[[STR-243](https://bugs.cs.uu.nl/browse/STR-243)\] - Restructure
    the native C code of the SSL
-   \[[STR-292](https://bugs.cs.uu.nl/browse/STR-292)\] - Check native
    code of strateg-lib for comparison to ATempty
-   \[[STR-306](https://bugs.cs.uu.nl/browse/STR-306)\] - Adapt
    pretty-printer to Stratego-Sugar syntax
-   \[[STR-315](https://bugs.cs.uu.nl/browse/STR-315)\] - Merge
    improvements to strc with strc-core
-   \[[STR-376](https://bugs.cs.uu.nl/browse/STR-376)\] - Replace prims
    for annotation manipulation by annotation match and build operations
-   \[[STR-377](https://bugs.cs.uu.nl/browse/STR-377)\] - Merge
    stratego-runtime and stratego-runtime-choice
-   \[[STR-378](https://bugs.cs.uu.nl/browse/STR-378)\] - strc \--help:
    svn revision is 0 is tarball and buildfarm.
-   \[[STR-379](https://bugs.cs.uu.nl/browse/STR-379)\] - Fix
    compilation issues on Fedor Core 3 in data2xml-doc
-   \[[STR-380](https://bugs.cs.uu.nl/browse/STR-380)\] - Remove code
    from srts that is defined only for bootstrap reasons.
-   \[[STR-396](https://bugs.cs.uu.nl/browse/STR-396)\] - Inlude manual
    pages from Stratego/XT manual in Stratego/XT distribution

[]{#Improvement} Improvement
----------------------------

-   \[[STR-328](https://bugs.cs.uu.nl/browse/STR-328)\] - strc
    \--version should provide SVN revision number
-   \[[STR-332](https://bugs.cs.uu.nl/browse/STR-332)\] - strc: \--keep
    only keeps intermediate file if format checker fails
-   \[[STR-347](https://bugs.cs.uu.nl/browse/STR-347)\] - Configuration:
    support combined explicit and implicit configuration
-   \[[STR-350](https://bugs.cs.uu.nl/browse/STR-350)\] - Don\'t install
    the internal autoxt macros
-   \[[STR-352](https://bugs.cs.uu.nl/browse/STR-352)\] - Rewrite
    tool-doc to desugaring instead of overlays
-   \[[STR-370](https://bugs.cs.uu.nl/browse/STR-370)\] - Introduce
    STRCFLAGS. SCFLAGS is obsolete but supported.
-   \[[STR-374](https://bugs.cs.uu.nl/browse/STR-374)\] - Logging should
    not always print the current term
-   \[[STR-384](https://bugs.cs.uu.nl/browse/STR-384)\] - stratego-lib
    testsuite should use libraries in prefix.
-   \[[STR-390](https://bugs.cs.uu.nl/browse/STR-390)\] - Support make
    check on Cygwin
-   \[[STR-391](https://bugs.cs.uu.nl/browse/STR-391)\] - Support make
    check on Darwin
-   \[[STR-392](https://bugs.cs.uu.nl/browse/STR-392)\] -
    Check-constructor: pretty-print Stratego AST in error message.
-   \[[STR-401](https://bugs.cs.uu.nl/browse/STR-401)\] - Remove
    pkgconfig file of sdf2-bundle from strategoxt

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
