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
    Page](http://www.program-transformation.org/edit/Stratego/ReportingBugs?t=1536825663)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ReportingBugs)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ReportingBugs)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ReportingBugs?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ReportingBugs?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ReportingBugs?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ReportingBugs?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ReportingBugs?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ReportingBugs?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ReportingBugs?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ReportingBugs)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ReportingBugs?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/ReportingBugs?template=oopsmore&param1=1.3&param2=1.3)
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
Reporting Bugs {#reporting-bugs .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#JIRA_Issue_Tracking_System} JIRA Issue Tracking System
----------------------------------------------------------

In March 2004, we have adopted JIRA as an issue tracking system for
[StrategoXT](StrategoXT){.twikiLink} and related projects.

### []{#Where_to_report_issues}[]{#Where_to_report_issues_} Where to report issues?

Our JIRA installation is public and everyone can submit issues. Please
report issues directly to the JIRA issue tracking system from now on.
New issues reported in JIRA will be sent automatically to the
stratego-bugs [MailingList](MailingList){.twikiLink} for notification.
However, the issue in JIRA is the preferred place too for
followup-comments. Of course you are welcome to discuss issues at the
stratego-dev [MailingList](MailingList){.twikiLink} first.

-   <http://yellowgrass.org/STR>

### []{#How_to_specify_issues}[]{#How_to_specify_issues_} How to specify issues?

A bug report should contain a description of the bug and preferably a
small Stratego module that reproduces the bug. If possible the module
should be organized with the
[StrategoUnit[^?^](http://www.program-transformation.org/edit/Stratego/StrategoUnit?topicparent=Stratego.ReportingBugs)]{.twikiNewLink
style="background : #FFFFCE;"} testing framework such that it can be
used in regression testing.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 12 Nov 2002

### []{#How_to_use_JIRA}[]{#How_to_use_JIRA_} How to use JIRA?

**As an anonymous visitor**: Our JIRA installation is *public*, so
reporting issues and browsing through and viewing existing issues is
possible right away.

**As a registered user**: If you create an account, and use JIRA as a
registered user, you also have the option to *watch issues*: get
notified of all changes to an issue, even if you\'re not the reporter or
assignee.

\-- [ArthurVanDam](../Main/ArthurVanDam){.twikiLink} - 26 Mar 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
