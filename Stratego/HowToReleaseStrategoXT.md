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
    Page](http://www.program-transformation.org/edit/Stratego/HowToReleaseStrategoXT?t=1536825539)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/HowToReleaseStrategoXT)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/HowToReleaseStrategoXT)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/HowToReleaseStrategoXT?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/HowToReleaseStrategoXT?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Stratego/HowToReleaseStrategoXT?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/HowToReleaseStrategoXT?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/HowToReleaseStrategoXT?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/HowToReleaseStrategoXT?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/HowToReleaseStrategoXT?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/HowToReleaseStrategoXT?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/HowToReleaseStrategoXT)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/HowToReleaseStrategoXT?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Stratego/HowToReleaseStrategoXT?template=oopsmore&param1=1.7&param2=1.7)
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
How To Release Stratego XT {#how-to-release-stratego-xt .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

This is a to do list for creating a new release of
[StrategoXT](StrategoXT){.twikiLink}.

[]{#Make_sure_trunk_is_ok} Make sure trunk is ok
------------------------------------------------

-   The trunk revision must build at all machines of the buildfarm,
    Cygwin and Mac OS X.

<!-- -->

-   Write news in `news-archive/NEWS-0.XX`. Also add this file to
    `EXTRA_DIST` in Makefile.am
    -   Collect news items from
        [svnlog](http://catamaran.labs.cs.uu.nl/svnlog/StrategoXT/) and
        JIRA issues.

[]{#Make_a_branch} Make a branch
--------------------------------

-   Make a branch of the trunk

<!-- -->

-   Comment the `XT_PRE_RELEASE` macro in configure.ac

[]{#Make_distributions} Make distributions
------------------------------------------

-   Add a job for this branch to the configuration of the Nix buildfarm.
    This involves adding a build job in `jobs.conf` and creating a new
    attribute in the Nix expression `strategoxt..nix`.

<!-- -->

-   Download tarballs, RPM, and SRPM from the Nix releases server to the
    ftp of Stratego.

<!-- -->

-   Create binaries for Cygwin and Mac OS X, upload to ftp of Stratego.

<!-- -->

-   Create a tag of the branch for this Stratego release.

[]{#Announce_the_release} Announce the release
----------------------------------------------

-   Update the Stratego Wiki:
    -   Create a topic StrategoRelease0XX with URLs and the news.
    -   Create a topic StrategoRelease0XXIssues with the JIRA release
        notes.
    -   Point to this new release in
        [StrategoDownload](StrategoDownload){.twikiLink}
    -   Update the [WebLeftBar](WebLeftBar){.twikiLink} topic to the new
        release
    -   Add a short news item to [WebNews](WebNews){.twikiLink}

<!-- -->

-   Remove Wiki markup from the news file and send this to
    `stratego-announce@cs.uu.nl`

[]{#Continue_with_next_release} Continue with next release
----------------------------------------------------------

-   Set the current version of [StrategoXT](StrategoXT){.twikiLink}
    \'released\' in JIRA

<!-- -->

-   Trunk: increase the version numbers in all `configure.ac` files.

<!-- -->

-   After a major release: remove obsolete strategies from the Stratego
    library

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
