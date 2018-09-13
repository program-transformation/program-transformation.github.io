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
    Page](http://www.program-transformation.org/edit/PHP/ConstPropStatus?t=1536826875)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/ConstPropStatus)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/ConstPropStatus)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/ConstPropStatus?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/ConstPropStatus?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/PHP/ConstPropStatus?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/ConstPropStatus)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/ConstPropStatus?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/PHP/ConstPropStatus?template=oopsmore&param1=1.1&param2=1.1)
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
Const Prop Status {#const-prop-status .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Static analysis for PHP
:::

PHP-Sat offers the functionality to automatically analyze files which
are included with the `require_*=/=include_*` functions of PHP.

Many projects use some kind of `include $prefix.'filename'.$postfix;`
syntax to make sure that their code can run under multiple
configurations. To make sure that these projects can also be analyzed by
PHP-Sat we have (partially) included constant-propagation to statically
determine which files are included.

Currently, the constant propagation is capable of correctly propagating
values through:

-   Operator-expressions
-   Control-flow statements

This means PHP-Sat offers inclusion support for procedural scripts
without function calls.

In the future the inclusion-support will be extended to support:

-   Function calls
-   Object creations

as far as static analyzes allows these constructs.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
