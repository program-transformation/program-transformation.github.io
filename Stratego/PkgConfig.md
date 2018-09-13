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
    Page](http://www.program-transformation.org/edit/Stratego/PkgConfig?t=1536825539)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PkgConfig)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PkgConfig)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PkgConfig?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PkgConfig?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/PkgConfig?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PkgConfig)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PkgConfig?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/PkgConfig?template=oopsmore&param1=1.1&param2=1.1)
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
Pkg Config {#pkg-config .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Pkg_config} Pkg-config
--------------------------

In this release we have introduced pkg-config for locating packages and
their configuration. The use of pkg-config has several advantages:

-   Distributions of packages that have been created using a certain
    Stratego/XT are more likely to work on future versions of
    Stratego/XT. Thus, package don\'t have to be re-distributed if a new
    Stratego/XT comes out.

<!-- -->

-   Users of packages that use Stratego/XT don\'t need to configure this
    package with the location of Stratego/XT. Pkg-config is used to find
    the location of Stratego/XT on the system of the user.

<!-- -->

-   Internally, the installation of Stratego/XT is less complicated. The
    installation of packages in the directory `local-baseline` is no
    longer necessary.

<!-- -->

-   Users can use pkg-config to pass the right includes paths to the
    Stratego compiler.

### []{#For_Stratego_XT_Users} For Stratego/XT Users

#### []{#Installation} Installation

Stratego/XT users need to have pkg-config installed on their system
before they install Stratego/XT. Pkg-config 0.15 is widely deployed,
since it used by most GNOME packages, and should do the job. We don\'t
know what the exact minimal required version is.

You still need to configure Stratego/XT with the location the ATerm
library and the SDF2 Bundle (`--with-aterm`) and (`--with-sdf`). This
will be no longer necessary when future versions of the SDF2 Bundle and
the ATerm library support pkg-config. Internally, the `PKG_CONFIG_PATH`
is set and pkg-config is used to find the required packages.

#### []{#Compiling_your_Program} Compiling your Program

For compiling your own Stratego programs, you can now optionally use
pkg-config to find the flags that you need to pass to `strc`.

    $ pkg-config --variable=strcflags java-front
    -I /pkg/java-front/2005-03-30-14-06/share/sdf/java-front \
      -I /pkg/java-front/2005-03-30-14-06/share/java-front

In my `.bashrc` I\'ve defined an alias strcflags to make this common
command more compact:

    alias strcflags="pkg-config --variable=strcflags "

You can also specify multiple packages:

    $ strcflags java-front dryad
    -I /pkg/java-front/2005-03-30-14-06/share/sdf/java-front \
    -I /pkg/java-front/2005-03-30-14-06/share/java-front \
    -I /pkg/dryad/2005-04-04-15-24/share/dryad \
    -I /pkg/dryad/2005-04-04-15-24/share/sdf/dryad

Obviously, this is much easier then mentioning all the specific paths of
these packages.

### []{#For_Users_of_Packages_that_use_S} For Users of Packages that use Stratego/XT

If the developer of this package releases a new version, then this
package is more likely to work on future versions of Stratego/XT. You
don\'t need to configure the package with locations of `aterm`, `sdf`,
and `strategoxt`, since pkg-config is used to find them. Hence, the
package is easier to install.

If you install Stratego/XT in a non standard location, then you need to
set the PKG\_CONFIG\_PATH. See
[SomeTopic[^?^](http://www.program-transformation.org/edit/Stratego/SomeTopic?topicparent=Stratego.PkgConfig)]{.twikiNewLink
style="background : #FFFFCE;"}.

### []{#For_Developers_of_Packages_that}[]{#For_Developers_of_Packages_that_} For Developers of Packages that use Stratego/XT

You need pkg-config, preferebly 0.17.2, which is available in the Nix
Packages Collection. The Autoconf macro XT\_USE\_XT\_PACKAGES no longer
defines configure arguments, but uses pkg-config to find the location of
packages. The old style of explicit configuration is still available in
the macro `XT_EXPLICTLY_USE_XT_PACKAGES`. Please note that your package
is more likely to break on future Stratego/XT versions if you use this
macro.

### []{#For_Stratego_XT_Developers} For Stratego/XT Developers

You need pkg-config, preferebly 0.17.2, which is available in the Nix
Packages Collection. A Subversion checkout of Stratego/XT requires
configuration `--with-strategoxt` for the baseline Stratego/XT, i.e.
pkg-config is not used to find the baseline Stratego/XT, since this very
fragile. Internally, the PKG\_CONFIG\_PATH is set to the configuration
flags that you provide.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
