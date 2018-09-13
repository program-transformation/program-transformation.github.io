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
    Page](http://www.program-transformation.org/edit/PHP/PhpFrontDocumentation?t=1536825869)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpFrontDocumentation)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpFrontDocumentation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpFrontDocumentation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpFrontDocumentation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/PHP/PhpFrontDocumentation?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/PHP/PhpFrontDocumentation?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/PHP/PhpFrontDocumentation?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/PHP/PhpFrontDocumentation?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/PHP/PhpFrontDocumentation?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/PHP/PhpFrontDocumentation?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpFrontDocumentation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpFrontDocumentation?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpFrontDocumentation?template=oopsmore&param1=1.10&param2=1.10)
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
PHP-front Documentation {#php-front-documentation .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Static analysis for PHP
:::

### []{#Syntax_definition} Syntax definition

The syntax definition can be browsed online:

-   [PHP4 syntax
    definition](http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt//php-front-syn-docs-stable-latest/docs/html/languages/php/version4/Main.sdf.html)
-   [PHP5 syntax
    definition](http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt//php-front-syn-docs-stable-latest/docs/html/languages/php/version5/Main.sdf.html)

The syntax definition of the PHP versions identify which constructs
there are and which productions are allowed.

### []{#API_documentation} API documentation

The PHP-front library contains many useful strategies, there is
documentation for most of the strategies:

-   [API
    documentation](http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt//php-front-lib-docs-stable-latest/docs/)

### []{#Pretty_printer} Pretty printer

A short explanation of the rules for the pretty printer can be found
here:

-   [PrettyPrintRules](PrettyPrintRules){.twikiLink}

### []{#Projects_based_on_PHP_front} Projects based on PHP-front

These two guides should help you with starting your own project based on
PHP-Front:

-   [TheEmptyModule](TheEmptyModule){.twikiLink}
-   [TheExampleProject](TheExampleProject){.twikiLink}

### []{#Development} Development

If you want to extend/adapt/improve PHP-front, please look at the
[generic development
instructions](GenericDevelopmentInstructions){.twikiLink} in order to
set up your workbench.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
