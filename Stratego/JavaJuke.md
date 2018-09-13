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
    Page](http://www.program-transformation.org/edit/Stratego/JavaJuke?t=1536825594)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/JavaJuke)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/JavaJuke)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/JavaJuke?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/JavaJuke?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Stratego/JavaJuke?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/JavaJuke?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/JavaJuke?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/JavaJuke?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/JavaJuke?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/JavaJuke?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/JavaJuke)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/JavaJuke?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Stratego/JavaJuke?template=oopsmore&param1=1.5&param2=1.5)
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
Java Juke {#java-juke .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Java_Swul_parts} Java-Swul parts
------------------------------------

The user interface of [JavaJuke](JavaJuke){.twikiLink} is build using
Java-Swul. The interface source is a mixture of using Swul to create
default Swing components and integrating custom created user interface
components as Java expressions.

-   A quick link to the complete Java-Swul source of the gui of
    [JavaJuke](JavaJuke){.twikiLink}:
    <https://svn.cs.uu.nl:12443/repos/JavaJuke/src/javajuke/gui/JukeBoxGUI.javaswul>

<!-- -->

-   An example how to use [Java-Swul](Java-Swul){.twikiLink} in your
    build proces. Apart from the standard tasks in Ant you can execute
    the swulc-preprocessor:

<!-- -->

    <apply executable="swulc" dest="${src}/javajuke/gui" verbose="true">
      <fileset dir="${src}/javajuke/gui" includes="*.javaswul"/>
      <mapper type="glob" from="*.javaswul" to="*.java"/>
      <arg value="-o"/>
      <targetfile/>
      <arg value="-i"/>
      <srcfile/>
    </apply>

[]{#Features} Features
----------------------

The player features:

-   an advanced searching field
-   presorting on artist, title and filesystem
-   dual songselections
-   a queue of songs to play
-   detachable control toolbar
-   shuffling
-   drag-n-drop functionality.
-   playing of entire grouped mp3\'s

The mp3 capabilities of [JavaJuke](JavaJuke){.twikiLink} are provided by
the [JLayer project](http://www.javazoom.net/javalayer/javalayer.html).

![JavaJuke-screenshot.png](http://www.stratego-language.org//pub/Stratego/JavaJuke/JavaJuke-screenshot.png)

[]{#Download} Download
----------------------

A runnable jar of this program can be downloaded:

<http://www.stratego-language.org//pub/Stratego/JavaJuke/javajuke.jar>

This file is generated by the ant build using java version 1.4.2\_03 on
january the 20th.

[]{#Source} Source
------------------

The complete source of this program can be found in our Subversion
repository on:

    svn checkout https://svn.cs.uu.nl:12443/repos/JavaJuke/

\-- [ReneDeGroot](../Main/ReneDeGroot){.twikiLink} - 08 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
