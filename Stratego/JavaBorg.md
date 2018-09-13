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
    Page](http://www.program-transformation.org/edit/Stratego/JavaBorg?t=1536825593)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/JavaBorg)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/JavaBorg)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/JavaBorg?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/JavaBorg?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    13](http://www.program-transformation.org/view/Stratego/JavaBorg?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Stratego/JavaBorg?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Stratego/JavaBorg?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Stratego/JavaBorg?rev1=1.12&rev2=1.11)
-   [Rev
    11](http://www.program-transformation.org/view/Stratego/JavaBorg?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Stratego/JavaBorg?rev1=1.11&rev2=1.10)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/JavaBorg)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/JavaBorg?template=oopsmore&param1=1.13&param2=1.13)
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
    \...](http://www.program-transformation.org/oops/Stratego/JavaBorg?template=oopsmore&param1=1.13&param2=1.13)
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
Java Borg {#java-borg .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Installation](JavaBorg#Installation)
    -   [RPM](JavaBorg#RPM)
    -   [Source Tarball](JavaBorg#Source_Tarball)
    -   [Subversion](JavaBorg#Subversion)
-   [More JavaBorg](JavaBorg#More_JavaBorg)
-   [Authors](JavaBorg#Authors)
:::

[JavaBorg](JavaBorg){.twikiLink} is an instance of
[MetaBorg](MetaBorg){.twikiLink}. Applications of
[JavaBorg](JavaBorg){.twikiLink} are collected in the JavaBorg package.

[]{#Installation} Installation
------------------------------

JavaBorg can be obtained directly from the Subversion repository, or by
installing an (unstable) release. You can also
[browse](https://svn.cs.uu.nl:12443/repos/StrategoXT/java-borg/trunk)
the code online if you just want to have a look at the implementation.
You need to install 5 packages:

-   [ATerm library](../Tools/ATermLibrary){.twikiLink}
-   [SDF2 Bundle](Sdf2Bundle){.twikiLink}
-   [StrategoXT](StrategoXT){.twikiLink}
-   [Java-front](JavaFront){.twikiLink}
-   [Java-borg](JavaBorg){.twikiLink}

JavaBorg distributions are created continuously by our
[Nix](http://www.cs.uu.nl/groups/ST/Trace/Nix)-based release management
system. RPM and tarball distributions are available at:

-   <http://releases.strategoxt.org/java-borg-unstable-latest>

### []{#RPM} RPM

The release page of the latest [JavaBorg](JavaBorg){.twikiLink} lists
all the RPMs you need to install.

-   <http://releases.strategoxt.org/java-borg-unstable-latest>

### []{#Source_Tarball} Source Tarball

You have to install these packages in this order.

-   [sdf2-bundle-2.2](../Sdf/Sdf2BundleRelease22){.twikiLink}
-   [strategoxt-0.13](StrategoRelease013){.twikiLink}
-   [java-front 0.6](JavaFrontRelease06){.twikiLink}
    -   Cygwin users: java-front does, for unkown reasons, currently not
        work at Cygwin.
-   [java-borg](http://releases.strategoxt.org/java-borg-unstable-latest/)

If you install all package in the same prefix, then no configuration is
required. This is highly recommended, since there is a lot of
configuration. If you really want to control this, then the
[installation instructions](InstallationInstructions012){.twikiLink}
describe the flags. If you *really* want to control the configuration,
then these are the possible flags:

Configuration of strategoxt:

-   `--with-xt=<dir>` or when using different prefixes for SDF and
    ATerm:
    -   `--with-sdf=<dir>`
    -   `--with-aterm=<dir>`

Configuration of java-front:

-   `--with-xt=<dir>` or when using different prefixes for StrategoXT,
    SDF and ATerm:
    -   `--with-strategoxt=<dir>`
    -   `--with-sdf=<dir>`
    -   `--with-aterm=<dir>`

Configuration of java-borg:

-   `--with-xt=<dir>` or when using different prefixes for StrategoXT,
    SDF and ATerm:
    -   `--with-strategoxt=<dir>`
    -   `--with-sdf=<dir>`
    -   `--with-aterm=<dir>`
-   `--with-java-front=<dir>`
-   Optional for running some of the examples:
    -   `--with-aterm-java` for the Java ATerm library, which is
        available at from the [CWI package
        base](http://www.cwi.nl/htbin/sen1/twiki/bin/view/SEN1/PackageBase).

### []{#Subversion} Subversion

[JavaBorg](JavaBorg){.twikiLink} Subversion repository:

-   <https://svn.cs.uu.nl:12443/repos/StrategoXT/java-borg/trunk>

[]{#More_JavaBorg} More JavaBorg
--------------------------------

[Java-Swul](Java-Swul){.twikiLink} was one of the languages collected in
the [JavaBorg](JavaBorg){.twikiLink} package. Currently it is a separate
package.

[]{#Authors} Authors
--------------------

[JavaBorg](JavaBorg){.twikiLink} is being developed by

-   [Martin Bravenboer](../Main/MartinBravenboer){.twikiLink}
-   [Eelco Visser](../Main/EelcoVisser){.twikiLink}
-   [Rene de Groot](../Main/ReneDeGroot){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
