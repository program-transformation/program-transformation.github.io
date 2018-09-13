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
    Page](http://www.program-transformation.org/edit/PHP/PhpSatQuality?t=1536825868)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpSatQuality)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpSatQuality)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpSatQuality?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpSatQuality?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/PHP/PhpSatQuality?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/PHP/PhpSatQuality?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/PHP/PhpSatQuality?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/PHP/PhpSatQuality?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/PHP/PhpSatQuality?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/PHP/PhpSatQuality?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpSatQuality)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpSatQuality?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpSatQuality?template=oopsmore&param1=1.4&param2=1.4)
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
Php Sat Quality {#php-sat-quality .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Static analysis for PHP
:::

[]{#Bugpatterns} Bugpatterns
----------------------------

Each bugpattern category within PHP-Sat has his own testsuite. Each
bugpattern has is own section within the testsuite to test different
properties of the bugpattern. If you find cases that are not handled
correctly, please let us know and we will add the appropriate tests and
solution. These testsuites are run on every build to ensure that nothing
breaks after changing the code.

[]{#Syntax_Definition} Syntax Definition
----------------------------------------

PHP-Sat has his own configuration file and this file has special syntax.
This syntax is tested by an extensive testsuite that contains unit-tests
for the configuration language. These tests include tests for the
grammar of the configuration file, but also tests for the priorities of
combinators. The tests are run on every build to ensure that everything
still works.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
