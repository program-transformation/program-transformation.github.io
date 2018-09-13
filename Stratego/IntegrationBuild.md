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
    Page](http://www.program-transformation.org/edit/Stratego/IntegrationBuild?t=1536825368)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/IntegrationBuild)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/IntegrationBuild)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/IntegrationBuild?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/IntegrationBuild?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Stratego/IntegrationBuild?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/IntegrationBuild?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/IntegrationBuild?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/IntegrationBuild?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/IntegrationBuild?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/IntegrationBuild?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/IntegrationBuild)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/IntegrationBuild?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Stratego/IntegrationBuild?template=oopsmore&param1=1.6&param2=1.6)
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
Stratego/XT Packages Integration Build {#strategoxt-packages-integration-build .twikiTopicTitle}
======================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The Stratego/XT packages integration build provides a heavily tested
release of the latest version of Stratego/XT, its dependencies, and
packages based on Stratego/XT. The packages are guaranteed to work
together without any problems. The latest successful integration build
is available at:

-   <http://releases.strategoxt.org/strategoxt-packages/strategoxt-packages-stable/>

Installing more recent releases of individual packages (see [continuous
build](ContinuousBuild){.twikiLink}) might result in incompatible
combinations of packages, so this is discouraged.

### []{#How_to_install}[]{#How_to_install_} How to install?

**Nix Channel**. We advice to use the [Nix package
manager](http://nixos.org) for installing packages from our release
management system. To keep your installation up to date, we advice to
subscribe to the `strategoxt-packages` Nix channel, as explained on the
[release page of
strategoxt-packages](http://releases.strategoxt.org/strategoxt-packages/strategoxt-packages-stable/).

**Nix Package**. You can use the [Nix package manager](http://nixos.org)
to install packages (without subscribing to the `strategoxt-packages`
Nix channel) by clicking on the link for your platform of the package
that you want to install (see the table at the channel page). If your
browser asks what to do with this file, choose to open it using
`/nix/bin/nix-install-package`.

**Source**. The integration build provides links to the releases that
have been built and tested for this integration build. At the release
pages of the individual packages, you will find source distributions.

**RPM**. Many packages also provide RPMs. Similar to installation from
source, you can find RPMs at the release pages of the individual
packages.

**Binary Windows Archive**. Some packages provide support for native
Microsoft Windows. In this case the release page of the individual
package provides a link to a .zip file that you can extract to any
location in your file system. You don\'t need to install Cygwin.

#### []{#Detailed_instructions} Detailed instructions

See the [installation
instructions](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/installation.html)
if you are not familiar with the standard installation procedure of
source tarballs or RPMs.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
