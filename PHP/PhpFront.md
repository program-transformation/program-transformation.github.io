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
    Page](http://www.program-transformation.org/edit/PHP/PhpFront?t=1536825509)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpFront)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpFront)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpFront?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpFront?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/PHP/PhpFront?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/PHP/PhpFront?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/PHP/PhpFront?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/PHP/PhpFront?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/PHP/PhpFront?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/PHP/PhpFront?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpFront)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpFront?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpFront?template=oopsmore&param1=1.7&param2=1.7)
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
About PHP-front {#about-php-front .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Static analysis for PHP
:::

::: {.twikiToc}
-   [Features](PhpFront#Features)
-   [Tools](PhpFront#Tools)
-   [Project Info](PhpFront#Project_Info)
-   [Projects that use PHP-Front](PhpFront#Projects_that_use_PHP_Front)
:::

[]{#Features} Features
----------------------

PHP-front is a package you can use to generate, analyse, or transform
PHP code. It contains a handcrafted SDF grammar for PHP, a handcrafted
pretty printer, an extensive library for reflecting over PHP code, and
support for evaluation of PHP.

Some of the unique features of PHP-front are:

-   Modular and extensible syntax definition for PHP for versions 4 and
    5
-   Option to preserve comments
-   Pretty printer
-   Automatic inclusion of files
-   PHP-specific, common traversals
-   Reflection support
-   Conversion of abstract syntax tree to XML possible

[]{#Tools} Tools
----------------

Tools that are included in the package are:

-   parse-php
-   parse-php4, parse-php5
-   pp-php
-   pp-php4, pp-php5
-   eval-php

[]{#Project_Info} Project Info
------------------------------

Contributors:

-   Eric Bouwers
-   Martin Bravenboer

Feedback and bug reports:

-   Armijn Hemel
-   Tim Hemel
-   Eelco Visser

Sponsors:

-   Google Summer of Code 2006

License:

-   PHP-Front is LGPL (GNU Lesser General Public License) software.

[]{#Projects_that_use_PHP_Front} Projects that use PHP-Front
------------------------------------------------------------

-   [PHP-sat](PhpSat){.twikiLink}
-   [PHP-tools](PhpTools){.twikiLink}
-   [StringBorg](../Stratego/StringBorg){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
