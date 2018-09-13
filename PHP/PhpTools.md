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
    Page](http://www.program-transformation.org/edit/PHP/PhpTools?t=1536825870)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpTools)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpTools)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpTools?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpTools?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/PHP/PhpTools?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/PHP/PhpTools?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/PHP/PhpTools?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/PHP/PhpTools?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/PHP/PhpTools?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/PHP/PhpTools?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpTools)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpTools?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpTools?template=oopsmore&param1=1.8&param2=1.8)
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
PHP-tools {#php-tools .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Static analysis for PHP
:::

::: {.twikiToc}
-   [Introduction](PhpTools#Introduction)
-   [Download](PhpTools#Download)
    -   [Latest Developments](PhpTools#Latest_Developments)
    -   [Installation](PhpTools#Installation)
-   [Project Info](PhpTools#Project_Info)
    -   [Issue Tracking](PhpTools#Issue_Tracking)
    -   [Contact and Mailing List](PhpTools#Contact_and_Mailing_List)
    -   [Source Repository](PhpTools#Source_Repository)
    -   [Developer(s)](PhpTools#Developer_s)
    -   [License](PhpTools#License)
:::

[]{#Introduction} Introduction
------------------------------

Within the documentation of [PHP-front](PhpFront){.twikiLink} the
[TheExampleProject](TheExampleProject){.twikiLink} is used to explain
how you can setup your own project. This documentation uses PHP-Tools as
the running example. Although it is used in the documentation the
package actually builds and provides real-life tools.

PHP-Tools is growing to be a package with useful tools for analyzing
PHP-projects. All of the tools will be able to answer a single question.
The following list of tools is available:

-   defined-functions ; which functions are defined outside the scope of
    a class? (since revision 396)
-   input-vector ; Which entries in the input arrays are being accessed
    within the project?
-   test-migration ; Are there any static problems with migrating my
    code to PHP5? (since revision 406) ([More
    info](http://ericbouwers.blogspot.com/2007/09/little-migration-helper.html))
-   php-cyco ; What is the cyclomatic complexity of me PHP-script?
    (since revision 421) ([More
    info](http://ericbouwers.blogspot.com/2007/12/calculating-complexity-of-php.html))

Yes, this list is to be
[extended](http://bugs.strategoxt.org/secure/IssueNavigator.jspa?reset=true&&pid=10180&resolution=-1&component=10282&sorter/field=priority&sorter/order=DESC).

[]{#Download} Download
----------------------

### []{#Latest_Developments} Latest Developments

Distributions of the head revision are created continuously:

\* <http://hydra.nixos.org/jobset/psat/php-tools/channel/latest>

The distributions contain the latest of the latest developments, but if
you really want to, the latest sources can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/psat/php-tools/trunk

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

-   <http://bugs.strategoxt.org/browse/PSAT> (or
    [direct](https://bugs.cs.uu.nl/secure/IssueNavigator.jspa?reset=true&&pid=10180&resolution=-1&component=10282&sorter/field=priority&sorter/order=DESC))

### []{#Contact_and_Mailing_List} Contact and Mailing List

You can either ask question about the project on the
[MailingList](MailingList){.twikiLink} or swing by on \#stratego on
<irc://irc.freenote.net>.

### []{#Source_Repository} Source Repository

The sources of php-tools are available from Subversion.

-   <https://svn.strategoxt.org/repos/psat/php-tools/trunk>

### []{#Developer_s}[]{#Developer_s_} Developer(s)

-   [Eric Bouwers](http://ericbouwers.blogspot.com) (lead developer)

### []{#License} License

PHP-Tools is LGPL (GNU Lesser General Public License) software.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
