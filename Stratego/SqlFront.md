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
    Page](http://www.program-transformation.org/edit/Stratego/SqlFront?t=1536825510)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SqlFront)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SqlFront)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SqlFront?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SqlFront?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    11](http://www.program-transformation.org/view/Stratego/SqlFront?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Stratego/SqlFront?rev1=1.11&rev2=1.10)
-   [Rev
    10](http://www.program-transformation.org/view/Stratego/SqlFront?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Stratego/SqlFront?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Stratego/SqlFront?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/SqlFront?rev1=1.9&rev2=1.8)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SqlFront)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SqlFront?template=oopsmore&param1=1.11&param2=1.11)
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
    \...](http://www.program-transformation.org/oops/Stratego/SqlFront?template=oopsmore&param1=1.11&param2=1.11)
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
SQL-front {#sql-front .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](SqlFront#Introduction)
-   [Download](SqlFront#Download)
    -   [Latest Unstable Release](SqlFront#Latest_Unstable_Release)
    -   [Installation](SqlFront#Installation)
-   [Project Info](SqlFront#Project_Info)
    -   [Issue Tracking](SqlFront#Issue_Tracking)
    -   [Contact and Mailing List](SqlFront#Contact_and_Mailing_List)
    -   [Source Repository](SqlFront#Source_Repository)
    -   [Team](SqlFront#Team)
    -   [License](SqlFront#License)
:::

[]{#Introduction} Introduction
------------------------------

SQL-front provides a syntax definition of a subset of SQL/92. You can
use SQL-front to parse SQL.

[]{#Download} Download
----------------------

### []{#Latest_Unstable_Release} Latest Unstable Release

The latest unstable release of SQL-front is available at:

-   <http://releases.strategoxt.org/sql-front-unstable-latest/>

### []{#Installation} Installation

Install the package with the usual sequence of commands:

    $ ./configure
    $ make
    $ make install

You might need to set your `PKG_CONFIG_PATH` if you did not install the
dependencies in a standard location. Configure will tell you to do this
if it cannot find aterm, sdf or strategoxt.

[]{#Project_Info} Project Info
------------------------------

### []{#Issue_Tracking} Issue Tracking

We use JIRA to keep track of issues. Please report any issues that you
encounter!

-   <http://yellowgrass.org/SQLFront>

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [stratego\@cs.uu.nl mailing
list](https://mail.cs.uu.nl/mailman/listinfo/stratego). Also, the
SQL-front developers are usually available on IRC at
[irc.freenode.net/stratego](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Source_Repository} Source Repository

The sources of Java-front are available from Subversion.

-   <https://svn.strategoxt.org/repos/StrategoXT/sql-front/trunk>

### []{#Team} Team

Contributors:

-   [Martin Bravenboer](http://martin.bravenboer.name) (lead developer)
-   [Eelco Dolstra](http://www.cs.uu.nl/people/eelco/)

Sponsors:

-   [Department of Information and Computing Sciences, University of
    Utrecht](http://www.cs.uu.nl)
-   [NWO Jacquard](http://www.jacquard.nl/) project
    [TraCE](http://www.cs.uu.nl/wiki/Trace/WebHome)

### []{#License} License

SQL-front is [LGPL](LGPL){.twikiLink} (GNU Lesser General Public
License) software.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
