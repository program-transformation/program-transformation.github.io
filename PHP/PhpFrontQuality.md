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
    Page](http://www.program-transformation.org/edit/PHP/PhpFrontQuality?t=1536825869)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpFrontQuality)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpFrontQuality)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpFrontQuality?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpFrontQuality?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/PHP/PhpFrontQuality?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/PHP/PhpFrontQuality?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/PHP/PhpFrontQuality?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/PHP/PhpFrontQuality?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/PHP/PhpFrontQuality?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/PHP/PhpFrontQuality?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpFrontQuality)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpFrontQuality?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpFrontQuality?template=oopsmore&param1=1.5&param2=1.5)
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
PHP-front Quality {#php-front-quality .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Static analysis for PHP
:::

### []{#Syntax_Definition} Syntax Definition

PHP-Front has an extensive test suite that is run on every build. The
grammar is tested by over six hunderd unit-tests that cover at least
every construct in the Yacc-file of the distribution. The parse-unit
test suites in the source distribution give an overview of these tests.
A test suite that ends with a 5 is tested with the SDF for version 5, a
4 indicates a test with the SDF for version 4.

### []{#Pretty_Printer} Pretty Printer

The pretty-printer has a separate test-suites which is also run on every
build. The parser and the pretty printer are also tested together using
the test-files of the source-distribution of PHP. Each test-file is
parsed, pretty-printed, parsed and pretty-printed again. The correctness
of this round-trip is tested by performing a diff between the two parsed
and the two pretty-printed files. You can see the results of this
round-trip in the [parsing and pretty-printing tests
page](http://hydra.nixos.org/jobset/psat/php-front-testing-unstable-latest/docs/report/).
Notice that there are two sad smileys on that page. Both versions
contain a file with a switch that closes the cases with the \';\'
character. This is parsed correctly, but pretty-printed as a \':\'. This
causes the diff to fail, notice that the pretty-printed versions are
completely the same.

### []{#Reflection} Reflection

Both versions of PHP have sections in the test-suites for reflection.
PHP5 has some more sections because of the reflection over interfaces.
There is a special testsuite for the inclusion of files. This
test-suites contains tests that checks the usage of the current- and
working-directory related to the inclusion of files.

### []{#Useful_Strategies} Useful Strategies

The other useful strategies that are available within PHP-Front are
tested with separate test-suites. There are special test-suites for the
printing of included files, the constant-propagation and the
php-specific simple strategies.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
