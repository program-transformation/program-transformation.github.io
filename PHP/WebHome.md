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
    Page](http://www.program-transformation.org/edit/PHP/WebHome?t=1536825867)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/WebHome)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/WebHome)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/WebHome?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/WebHome?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/PHP/WebHome?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/PHP/WebHome?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/PHP/WebHome?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/PHP/WebHome?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/PHP/WebHome?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/PHP/WebHome?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/WebHome)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/WebHome?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/PHP/WebHome?template=oopsmore&param1=1.9&param2=1.9)
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
PHP-SAT.org {#php-sat.org .twikiTopicTitle}
===========

::: {.twikiWebTitle}
Static analysis for PHP
:::

PHP-Sat is a [Static
Analysis](http://en.wikipedia.org/wiki/Static_code_analysis) tool that
can be used to check for common mistakes in PHP source code. One of the
key-features of PHP-Sat is the automatic detection of different kind of
vulnerabilities, allowing you to check your source code for certain
security breaches.

Each static check within PHP-Sat is described by a
[bug-pattern](PhpSatBugPatterns){.twikiLink} which explains why the
pattern is recognized and what one can do to fix it. There are checks
for area\'s such as correctness, style and security. A
[bug-pattern](PhpSatBugPatterns){.twikiLink} is not necessarily bad in
all cases, although the security check(s) probably are, but we leave it
to the programmer to make this decision.

PHP-Sat is based on PHP-Front, a library that provides support for
generating, transforming or analyzing PHP code. It includes a
handcrafted SDF grammar for PHP, Stratego signatures generated from this
grammar and a handcrafted pretty printer.

The packages also provides support for automatic inclusion of files that
are [included](http://www.php.net/include) or
[required](http://www.php.net/require). The names of the files that are
included can optionally be resolved (to some extend) through [constant
propagation](http://en.wikipedia.org/wiki/Constant_propagation).
PHP-Front also supports PHP-specific traversals and reflection over
included files, functions and classes.

Check out the different sections to read about all the unique features
of both projects.\
If you are experiencing problems, have a suggestion/question or want to
share the name of your cat, please do not hesitate to contact us.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
