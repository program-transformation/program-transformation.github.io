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
    Page](http://www.program-transformation.org/edit/PHP/PhpFrontReleases?t=1536825869)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpFrontReleases)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpFrontReleases)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpFrontReleases?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpFrontReleases?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/PHP/PhpFrontReleases?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/PHP/PhpFrontReleases?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/PHP/PhpFrontReleases?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/PHP/PhpFrontReleases?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/PHP/PhpFrontReleases?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/PHP/PhpFrontReleases?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpFrontReleases)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpFrontReleases?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpFrontReleases?template=oopsmore&param1=1.10&param2=1.10)
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
Download PHP-front {#download-php-front .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Static analysis for PHP
:::

### []{#Stable_Releases} Stable Releases

There is no stable release of PHP-Front (yet). Check the [road
map](http://bugs.strategoxt.org/browse/PSAT?report=com.atlassian.jira.plugin.system.project:roadmap-panel)
for the current status of the 0.1 release.

### []{#Latest_Developments} Latest Developments

Distributions of the head revision are created continuously and are
available from:

-   <http://hydra.nixos.org/jobset/psat/php-front/channel/latest>

### []{#Subversion} Subversion

The latest distributions contain the latest of the latest developments,
but if you really want to, the latest sources can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/psat/php-front/trunk

Before you can configure the package using
`./configure --enable-bootstrap` you have to run the `./bootstrap`
script.

[]{#Installation_Instructions} Installation Instructions
--------------------------------------------------------

### []{#Dependencies} Dependencies

PHP-front requires a recent distribution of
[Stratego/XT](http://www.strategoxt.org). The exact version of
Stratego/XT that is guaranteed to work is linked to from the PHP-front
release page.

### []{#Linux_Mac_OS_X} Linux, Mac OS X

In order to get the project running on your favorite OS you can use the
standard set of installation commands:

    $ ./configure
    $ make
    $ make install

You might need to set your `PKG_CONFIG_PATH` if you did not install the
dependencies in a standard location. Configure will tell you to do this
if it cannot find aterm, sdf or strategoxt.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
