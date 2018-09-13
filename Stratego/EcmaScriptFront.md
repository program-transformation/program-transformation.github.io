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
    Page](http://www.program-transformation.org/edit/Stratego/EcmaScriptFront?t=1536825577)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/EcmaScriptFront)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/EcmaScriptFront)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/EcmaScriptFront?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/EcmaScriptFront?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/EcmaScriptFront?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/EcmaScriptFront?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/EcmaScriptFront?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/EcmaScriptFront?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/EcmaScriptFront?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/EcmaScriptFront?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/EcmaScriptFront)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/EcmaScriptFront?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/EcmaScriptFront?template=oopsmore&param1=1.4&param2=1.4)
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
ECMAScript-front {#ecmascript-front .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Features](EcmaScriptFront#Features)
-   [Download](EcmaScriptFront#Download)
    -   [Stable Releases](EcmaScriptFront#Stable_Releases)
    -   [Latest Developments](EcmaScriptFront#Latest_Developments)
    -   [Installation](EcmaScriptFront#Installation)
-   [Project Info](EcmaScriptFront#Project_Info)
    -   [Issue Tracking](EcmaScriptFront#Issue_Tracking)
    -   [People](EcmaScriptFront#People)
    -   [Source Repository](EcmaScriptFront#Source_Repository)
    -   [Build Status](EcmaScriptFront#Build_Status)
:::

[]{#Features} Features
----------------------

[ECMAScript-front](EcmaScriptFront){.twikiLink} is a package you can use
to generate or transform [ECMAScript](EcmaScript){.twikiLink} Edition 4
(also known as
[JavaScript[^?^](http://www.program-transformation.org/edit/Stratego/JavaScript?topicparent=Stratego.EcmaScriptFront)]{.twikiNewLink
style="background : #FFFFCE;"}) code.

[]{#Download} Download
----------------------

### []{#Stable_Releases} Stable Releases

Currently, no stable releases are available.

### []{#Latest_Developments} Latest Developments

Distributions (tarball, rpm, srpm) of the head revision are created
continuously:

-   <http://hydra.nixos.org/jobset/strategoxt/ecmascript-front-trunk>

The distributions contain the latest of the latest developments, but if
you really want to, the latest sources can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/ecmascript/ecmascript-front/trunk

Before you can configure the package as described above you have to run
the `./bootstrap` script.

### []{#Installation} Installation

ECMAScript-front requires:

-   [Latest unstable release of
    sdf2-bundle](http://releases.strategoxt.org/sdf2-bundle-unstable-latest/)
-   [Latest unstable release of
    strategoxt](http://releases.strategoxt.org/strategoxt-unstable-latest/)

Install ECMAScript-front package with the usual sequence of commands:

    $ ./configure
    $ make
    $ make install

You might need to set your `PKG_CONFIG_PATH` if you did not install the
dependencies in a standard location. Configure will tell you to do this
if it cannot find aterm, sdf, or strategoxt.

[]{#Project_Info} Project Info
------------------------------

### []{#Issue_Tracking} Issue Tracking

We use JIRA to keep track of issues. Please report any issues that you
encounter!

-   <http://yellowgrass.org/ES>

### []{#People} People

Contributors:

-   [Martin Bravenboer](http://www.cs.uu.nl/people/martin/)
-   [Dave Herman](http://calculist.blogspot.com/)

### []{#Source_Repository} Source Repository

The sources are available from Subversion:

-   <https://svn.strategoxt.org/repos/ecmascript/ecmascript-front/>

### []{#Build_Status} Build Status

You can track the status of automatic builds at:

-   <http://nix.cs.uu.nl/dist/stratego/full-status-ecmascript-front.html>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
