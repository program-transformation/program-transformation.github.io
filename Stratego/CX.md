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
    Page](http://www.program-transformation.org/edit/Stratego/CX?t=1536825566)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/CX)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/CX)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/CX?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/CX?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/CX?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/CX)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/CX?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/CX?template=oopsmore&param1=1.1&param2=1.1)
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
CX {#cx .twikiTopicTitle}
==

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](CX#Introduction)
-   [Features](CX#Features)
-   [Download](CX#Download)
    -   [Latest Developments](CX#Latest_Developments)
    -   [Installation](CX#Installation)
-   [Project Info](CX#Project_Info)
    -   [Issue Tracking](CX#Issue_Tracking)
    -   [Contact and Mailing List](CX#Contact_and_Mailing_List)
    -   [Source Repository](CX#Source_Repository)
    -   [Team](CX#Team)
    -   [License](CX#License)
-   [Related Software](CX#Related_Software)
:::

[]{#Introduction} Introduction
------------------------------

CX is an aterm bridge for [CIL](http://manju.cs.berkeley.edu/cil/), an
existing C front-end implement in OCaml. The Stratego/XT-based package
CX uses this bridge to read C code. CX will become a full set of tools
for combining CIL and Stratego for the implementation of C
transformations and analysis. The main difference with other Stratego/XT
projects that provide support for C (Transformers) is that this uses an
existing C front-end and not an [SDF](SDF){.twikiLink}-based parser. The
advantage is that you get the solid support of the existing frontend.
CIL supports some C dialects as well. The disadvantage is that there is
no grammar from which you can derive useful things for use with
Stratego/XT.

[]{#Features} Features
----------------------

-   C to ATerm bridge based on CIL
-   Pretty-printer from CIL to C

[]{#Download} Download
----------------------

### []{#Latest_Developments} Latest Developments

Distributions (tarball, rpm, srpm) of the head revision are created
continuously:

-   <http://releases.strategoxt.org/cx-unstable-latest/>

The distributions contain the latest of the latest developments, but if
you really want to, the latest sources can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/cx/trunk

Before you can configure the package as described above you have to run
the `./bootstrap` script.

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

-   <http://yellowgrass.org/CX>

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [stratego\@cs.uu.nl mailing
list](https://mail.cs.uu.nl/mailman/listinfo/stratego). Also, the CX
developers are usually available on IRC at
[irc.freenode.net/stratego](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Source_Repository} Source Repository

The sources of CX are available from Subversion.

-   <https://svn.cs.uu.nl:12443/repos/StrategoXT/cx/trunk>

### []{#Team} Team

Contributors:

-   Mart Kolthof

### []{#License} License

CX is GPL (GNU General Public License) software.

[]{#Related_Software} Related Software
--------------------------------------

-   [Transformers](http://www.lrde.epita.fr/cgi-bin/twiki/view/Transformers/Transformers)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
