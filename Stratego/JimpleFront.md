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
    Page](http://www.program-transformation.org/edit/Stratego/JimpleFront?t=1536825469)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/JimpleFront)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/JimpleFront)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/JimpleFront?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/JimpleFront?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Stratego/JimpleFront?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/JimpleFront?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/JimpleFront?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/JimpleFront?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/JimpleFront?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/JimpleFront?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/JimpleFront)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/JimpleFront?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Stratego/JimpleFront?template=oopsmore&param1=1.6&param2=1.6)
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
Jimple-front {#jimple-front .twikiTopicTitle}
============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](JimpleFront#Introduction)
-   [Download](JimpleFront#Download)
-   [Project Info](JimpleFront#Project_Info)
    -   [Contact and Mailing List](JimpleFront#Contact_and_Mailing_List)
    -   [Source Repository](JimpleFront#Source_Repository)
    -   [Team](JimpleFront#Team)
    -   [License](JimpleFront#License)
:::

[]{#Introduction} Introduction
------------------------------

Jimple-front defines the syntax of Jimple, the typed 3-address
representation of Java bytecode of the [Soot Java optimization
framework](http://www.sable.mcgill.ca/soot/). This representation is
suitable for program optimization and analysis. You can use Jimple-front
to parse Jimple. A pretty-printer for Jimple is under development.

You can
[browse](http://releases.strategoxt.org/docs/syntax/jimple-front/stable/docs/html/languages/jimple/Main.sdf.html)
the Jimple-front syntax definition for Jimple online.

[]{#Download} Download
----------------------

The latest unstable release of Jimple-front is available at:

-   <http://releases.strategoxt.org/jimple-front/unstable/>

Install the package with the usual sequence of commands:

    $ ./configure
    $ make
    $ make install

You might need to set your `PKG_CONFIG_PATH` if you did not install the
dependencies in a standard location. Configure will tell you to do this
if it cannot find aterm, sdf or strategoxt.

[]{#Project_Info} Project Info
------------------------------

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [stratego\@cs.uu.nl mailing
list](https://mail.cs.uu.nl/mailman/listinfo/stratego). Also, the
Jimple-front developers are usually available on IRC at
[irc.freenode.net/stratego](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Source_Repository} Source Repository

The sources of Java-front are available from Subversion.

-   <https://svn.strategoxt.org/repos/StrategoXT/sootxt/jimple-front/trunk>

### []{#Team} Team

Contributors:

-   [Martin Bravenboer](http://martin.bravenboer.name)
-   [Karl Trygve Kalleberg](http://www.ii.uib.no/~karltk/)

### []{#License} License

Jimple-front is licensed under the MIT license (see LICENSE in the
distribution)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.JimpleFront moved from Stratego.Jimple-front on 15 Mar 2008 -
17:29 by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Stratego/JimpleFront?newweb=Stratego&newtopic=Jimple-front&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
