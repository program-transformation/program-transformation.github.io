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
    Page](http://www.program-transformation.org/edit/Stratego/Java-Swul?t=1536825593)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/Java-Swul)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/Java-Swul)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/Java-Swul?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/Java-Swul?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/Stratego/Java-Swul?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Stratego/Java-Swul?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Stratego/Java-Swul?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/Java-Swul?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Stratego/Java-Swul?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/Java-Swul?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/Java-Swul)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/Java-Swul?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/Stratego/Java-Swul?template=oopsmore&param1=1.10&param2=1.10)
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
Java-Swul {#java-swul .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Introduction} Introduction
------------------------------

Java-Swul is a domain-specific language (DSL) for creating Java SWING
user interfaces. The Java-Swul language is embedded in Java. In this
fasion it provides a concrete syntax for creating SWING objects.

The Java-Swul package enables you to transform Java code with embedded
Java-Swul code to Java code. In this tranformation the Java-Swul is
assimilated into the surrounding Java. Giving you the power of Java with
an easy and straightforward way to create user interfaces.

The Swul part of the name comes from **SW**ING **u**serinterface
**l**anguage and combined with Java makes Java-Swul. It was first
contrived when developing the [MetaBorg](MetaBorg){.twikiLink} method.

[]{#Usage} Usage
----------------

### []{#Read_more_about_usage} Read more about usage

-   Some [JavaSwulExamples](JavaSwulExamples){.twikiLink} are viewable
    online.
-   A real application called [JavaJuke](JavaJuke){.twikiLink}, a mp3
    jukebox with a Java-Swul programmed interface and ant-build.
-   Read the the [Java-Swul
    article](http://www.stratego-language.org//pub/Stratego/Java-Swul/swul-article.pdf).

[]{#How_to_get_it} How to get it
--------------------------------

Java-Swul can be installed from source or from a package.

-   [Source](https://svn.cs.uu.nl:12443/repos/StrategoXT/java-swul/trunk)
    can be found in our Subversion server
-   [Binaries](http://releases.strategoxt.org/java-swul-0.1pre9927/) are
    build by our buildsystem

Java-Swul requires the following packages:

-   [StrategoXT](StrategoXT){.twikiLink}, a recent version, currently
    [strategoxt-0.14](http://releases.strategoxt.org/strategoxt-0.14/)
-   [Java-front](JavaFront){.twikiLink}, also a very recent version,
    currently
    [java-front-0.7pre9851](http://releases.strategoxt.org/java-front-0.7pre9851/)
-   [ATerm library](../Tools/ATermLibrary){.twikiLink}, the stable
    release will do, currently
    [aterm-2.3.1](http://releases.strategoxt.org/aterm-2.3.1/)
-   [SDF2 Bundle](Sdf2Bundle){.twikiLink}, the stable release will do,
    currently
    [sdf2-bundle-2.3](http://releases.strategoxt.org/sdf2-bundle-2.3/)

### []{#Some_pointers_on_source_compilat} Some pointers on source compilation

After a checkout from our Subversion server for a source compilation and
installation:

-   `./bootstrap`

When building Java-Swul from source the following configure parameters
might be needed:

-   `./configure`
    -   `--prefix=<dir>`
    -   `--with-strategoxt=<dir>`
    -   `--with-java-front=<dir>`
    -   `--with-aterm=<dir>`
    -   `--with-sdf=<dir>`

Or when pkg-config is available:

-   `./configure`
    -   `--prefix=<dir>`

After which a normal build and install can be done:

-   `make`
-   `make install`

[]{#Related_software} Related software
--------------------------------------

-   Java-Swul was grown out of [JavaBorg](JavaBorg){.twikiLink}
-   [JavaFront](JavaFront){.twikiLink} is used to extend Java

\-- [ReneDeGroot](../Main/ReneDeGroot){.twikiLink} - 3 Jan 2005\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
