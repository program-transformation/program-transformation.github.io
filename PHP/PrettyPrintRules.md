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
    Page](http://www.program-transformation.org/edit/PHP/PrettyPrintRules?t=1536826877)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PrettyPrintRules)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PrettyPrintRules)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PrettyPrintRules?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PrettyPrintRules?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/PHP/PrettyPrintRules?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/PHP/PrettyPrintRules?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/PHP/PrettyPrintRules?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PrettyPrintRules)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PrettyPrintRules?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/PHP/PrettyPrintRules?template=oopsmore&param1=1.2&param2=1.2)
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
Pretty Print Rules {#pretty-print-rules .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Static analysis for PHP
:::

The pretty printer that comes with PHP is designed to pretty print an
AST-representation of a PHP-program according to a set of rules. It is
not designed to return the exact same document that was parsed.

The following rules are used for pretty printing:

-   Expressions are printed on a single line.
-   Indentation is done for all nestings of statements, 2 spaces per
    nesting.
-   Control structures have a space between the keyword and the opening
    parenthesis.
-   Curly braces are printed if they appear in the source.
-   The opening curly brace of a statement is printed on the same line
    as the control structure.
-   The closing curly brace of a statement is printed on its own line,
    on the start of the indentation.
-   Function calls do not have a space between the name and the opening
    parenthesis.
-   Parameters to a function are separated by a space.
-   The include\_\* and require\_\* expressions do not have parentheses
    around their argument.

Notice that most of the rules follow the [PEAR
coding-standard](http://pear.php.net/manual/en/standards.php).\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
