::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
[![PHP-SatLogo](../pub/PHP/PhpSatLogo/PHP-SAT-LOGO-100px.jpg)](WebHome){.twikiLink}

**[PHP-sat](PhpSat){.twikiLink}**

-   [Download](PhpSatReleases){.twikiLink}
-   [Documentation](PhpSatDocumentation){.twikiLink}
-   [Bugpatterns](PhpSatBugPatterns){.twikiLink}
-   [Quality](PhpSatQuality){.twikiLink}
-   [Origin](PhpSatOrigin){.twikiLink}
-   [Name](PhpSatName){.twikiLink}

**[PHP-front](PhpFront){.twikiLink}**

-   [Download](PhpFrontReleases){.twikiLink}
-   [Documentation](PhpFrontDocumentation){.twikiLink}
-   [Quality](PhpFrontQuality){.twikiLink}
-   [Origin](PhpFrontOrigin){.twikiLink}

**[PHP-tools](PhpTools){.twikiLink}**

**[Support](PhpSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Issues](http://bugs.strategoxt.org/browse/PSAT)

**[Developers](PhpSatDevelopers){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/psat/)
-   [Continuous Builds](ContinuousBuilds){.twikiLink}
-   [Blog](http://ericbouwers.blogspot.com/)

**[The logo](PhpSatLogo){.twikiLink}**

**[Thanks](ThankYou){.twikiLink}**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/PHP/GenericDevelopmentInstructions?t=1536826876)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/GenericDevelopmentInstructions)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/GenericDevelopmentInstructions)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/GenericDevelopmentInstructions?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/GenericDevelopmentInstructions?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/PHP/GenericDevelopmentInstructions?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/PHP/GenericDevelopmentInstructions?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/PHP/GenericDevelopmentInstructions?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/PHP/GenericDevelopmentInstructions?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/PHP/GenericDevelopmentInstructions?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/PHP/GenericDevelopmentInstructions?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/GenericDevelopmentInstructions)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/GenericDevelopmentInstructions?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/PHP/GenericDevelopmentInstructions?template=oopsmore&param1=1.7&param2=1.7)
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
Generic Development Instructions {#generic-development-instructions .twikiTopicTitle}
================================

::: {.twikiWebTitle}
Static analysis for PHP
:::

This page describes how you can set up your development environment for
PHP-Sat/PHP-Front. Most of the information is located elsewhere, if a
link is dead please let us know.\
This configuration is the same configuration as the one that I am
personally using.

::: {.twikiToc}
-   [Installing Nix](GenericDevelopmentInstructions#Installing_Nix)
-   [Installing
    Stratego](GenericDevelopmentInstructions#Installing_Stratego)
-   [Installing Autoconf and
    Libtool](GenericDevelopmentInstructions#Installing_Autoconf_and_Libtool)
-   [Installing the
    repositories](GenericDevelopmentInstructions#Installing_the_repositories)
-   [Setting up your
    editor](GenericDevelopmentInstructions#Setting_up_your_editor)
-   [Have fun](GenericDevelopmentInstructions#Have_fun)
:::

[]{#Installing_Nix} Installing Nix
----------------------------------

Information about installing NIX is available
[here](http://hydra.nixos.org/job/nix/trunk/tarball/latest/download-by-type/doc/manual).\
Note that the manual installation of nix-packages goes more smoothly if
you set the
[permissions](http://hydra.nixos.org/build/118743/download/1/manual/#id262663)
in the right way.

[]{#Installing_Stratego} Installing Stratego
--------------------------------------------

The simplest way to install everything you need is to use
[this](http://hydra.nixos.org/jobset/nixpkgs/trunk/channel/latest) and
[this](http://hydra.nixos.org/project/strategoxt/channel/latest)
nix-channel.

    $ nix-channel --add http://hydra.nixos.org/jobset/nixpkgs/trunk/channel/latest
    $ nix-channel --add http://hydra.nixos.org/project/strategoxt/channel/latest
    $ nix-channel --update

You can use this command to install all dependencies:

    $ nix-env -i aterm-2.5 sdf2-bundle strategoxt strategoxt-utils stratego-shell

Note that the stratego-libraries are not installed, they are for other
platforms. And this one to update everything:

    $ nix-channel --update 
    $ nix-env -u '*'

[]{#Installing_Autoconf_and_Libtool} Installing Autoconf and Libtool
--------------------------------------------------------------------

In order to build from source you need to have both the
[Autoconf](http://www.gnu.org/software/autoconf/) and
[libtool](http://www.gnu.org/software/libtool/) tools installed. If you
do not have a copy of them available, you can either install these from
the release page of these tools, or through nix:

    $ nix-env -i autoconf libtool 

[]{#Installing_the_repositories} Installing the repositories
------------------------------------------------------------

*The \'php-\*\' stands for both \'php-front and php-sat\'*

The first thing that has to be done is the correct setting of the
PKG\_CONFIG\_PATH-variable.

    $ export PKG_CONFIG_PATH=~/.nix-profile/lib/pkgconfig

When this is not done the configure script will not find the ATerm, SDF
or StrategoXT-files.

The rest of the repository installation is straight-forward, just use
the following sequence of commands in the location of your choice.\
(The \<repository\> is <https://svn.strategoxt.org/repos>)

    $ svn checkout <repository>/psat/php-*/trunk ./php-*/
    $ cd php-*
    $ ./bootstrap
    $ ./configure --enable-bootstrap 
    $ make
    $ make check
    $ make install

This sequence gets the latests source-code, configures (the
*\--enable-bootstrap* is required!) and builds, checks and installs
everything.

[]{#Setting_up_your_editor} Setting up your editor
--------------------------------------------------

There are several editor plug-ins for stratego, you can find them
[here](../Stratego/AdditionalPackageDownload#Editor_Plugins_for_Stratego).

There are also highlighters available for
[Context](http://www.context.cx/). There is one for
[SDF](http://soc.bouwers.info/SDF.chl) and one for
[testsuites](http://soc.bouwers.info/Testsuite.chl).

[]{#Have_fun} Have fun
----------------------

Your development environment is ready. If you make anything useful
please let us know, happy coding!\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
