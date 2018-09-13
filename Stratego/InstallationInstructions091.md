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
    Page](http://www.program-transformation.org/edit/Stratego/InstallationInstructions091?t=1536825591)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/InstallationInstructions091)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/InstallationInstructions091)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/InstallationInstructions091?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/InstallationInstructions091?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/InstallationInstructions091?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/InstallationInstructions091?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/InstallationInstructions091?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/InstallationInstructions091?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/InstallationInstructions091?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/InstallationInstructions091?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/InstallationInstructions091)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/InstallationInstructions091?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/InstallationInstructions091?template=oopsmore&param1=1.4&param2=1.4)
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
Installation Instructions 091 {#installation-instructions-091 .twikiTopicTitle}
=============================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Download
    distribution](InstallationInstructions091#Download_distribution)
-   [Using source
    tarballs](InstallationInstructions091#Using_source_tarballs)
    -   [Download and install
        dependencies](InstallationInstructions091#Download_and_install_dependencie)
    -   [Installation of
        StrategoXT](InstallationInstructions091#Installation_of_StrategoXT)
-   [Related topics](InstallationInstructions091#Related_topics)
:::

[]{#Download_distribution} Download distribution
------------------------------------------------

First download [Stratego XT 0.9.1](StrategoRelease091){.twikiLink}. The
instructions on this page assume that you have downloaded a
distribution. See the [Latest
Sources[^?^](http://www.program-transformation.org/edit/Stratego/LatestSources?topicparent=Stratego.InstallationInstructions091)]{.twikiNewLink
style="background : #FFFFCE;"} topic for instructions on how to prepare
the sources you\'ve checked out from the Subversion repository.

[]{#Using_source_tarballs} Using source tarballs
------------------------------------------------

Use the instructions in this section if you want to install
[StrategoXT](StrategoXT){.twikiLink} using source tarballs (`.tar.gz`).

### []{#Download_and_install_dependencie} Download and install dependencies

[StrategoXT](StrategoXT){.twikiLink} is built using the
[ATermLibrary](ATermLibrary){.twikiLink},
[SGLR](../Sdf/SGLR){.twikiLink}, [PGEN](../Sdf/PGEN){.twikiLink}, and
optionally the Nancy [Choice Point
Library[^?^](http://www.program-transformation.org/edit/Stratego/ChoicePointLibrary?topicparent=Stratego.InstallationInstructions091)]{.twikiNewLink
style="background : #FFFFCE;"} (CPL) (with some adaptations for
Stratego). [SGLR](../Sdf/SGLR){.twikiLink} and
[PGEN](../Sdf/PGEN){.twikiLink} are available as part of the sdf2 bundle
of tools for the [SDF](SDF){.twikiLink} syntax definition formalism.

-   [aterm-1.6.7.tar.gz](ftp://ftp.stratego-language.org/pub/stratego/aterm/aterm-1.6.7.tar.gz)
-   [sdf2-1.5.tar.gz](ftp://ftp.stratego-language.org/pub/stratego/sdf2/sdf2-1.5.tar.gz)
-   [cpl-stratego-0.4.tar.gz](ftp://ftp.stratego-language.org/pub/stratego/stratego/cpl-stratego-0.4.tar.gz)

Using more recents versions of these packages is at your own risk, but
should work.

The following sequence of commands takes care of building and installing
the aterm and sdf2 bundle from source:

       DIR=/usr/local

       tar zxf aterm-1.6.7.tar.gz
       cd aterm-1.6.7
       ./configure --prefix=$DIR --with-gcc
       make
       make install
       cd ..

       tar zxf sdf2-1.5.tar.gz
       cd sdf2-1.5
       ./configure --prefix=$DIR --with-aterm=$DIR
       make install
       cd ..

sdf2-1.5 cannot be build without being installed at the same time.
Therefore you must build and install it at the same time (see also a
note in the section on the installation of
[StrategoXT](StrategoXT){.twikiLink})

Optionally you can install the choice point library:

       tar zxf cpl-stratego-0.4.tar.gz
       cd cpl-stratego-0.4
       ./configure --prefix=$DIR 
       make
       make install
       cd ..

### []{#Installation_of_StrategoXT} Installation of [StrategoXT](StrategoXT){.twikiLink}

Unpack and configure [StrategoXT](StrategoXT){.twikiLink} with the
following commands:

       tar zxf strategoxt-0.9.1.tar.gz
       cd strategoxt-0.9.1
       ./configure --prefix=$DIR --with-aterm=$DIR --with-sdf=$DIR

If you intend to modify the sources of
[StrategoXT](StrategoXT){.twikiLink}, you might want to set the prefix
(`DIR`) to the local directory ( `` `pwd` `` ) or at least a directory
where you have write permissions such that it is easy to re-install the
compiler.

To use the [Choice Point
Library[^?^](http://www.program-transformation.org/edit/Stratego/ChoicePointLibrary?topicparent=Stratego.InstallationInstructions091)]{.twikiNewLink
style="background : #FFFFCE;"} configure
[StrategoXT](StrategoXT){.twikiLink} as follows:

       ./configure --prefix=$DIR --with-aterm=$DIR --with-sdf=$DIR --with-cpl=$DIR 

For installation proceed as follows

       make install

Please note that doing a separate `make` is useless: unfortunately
[StrategoXT](StrategoXT){.twikiLink} currently cannot be built without
being installed at the same time.

[]{#Related_topics} Related topics
----------------------------------

-   known [Installation troubles](InstallationTrouble){.twikiLink} on
    operating systems.
-   an overview of reported successful
    [configurations](StrategoConfigurations){.twikiLink}
-   [Category installation](CategoryInstallation){.twikiLink} for all
    topics related to the installation of Stratego

------------------------------------------------------------------------

[CategoryInstallation](CategoryInstallation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
