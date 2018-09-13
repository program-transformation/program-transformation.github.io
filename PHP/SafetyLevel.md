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
    Page](http://www.program-transformation.org/edit/PHP/SafetyLevel?t=1536826881)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/SafetyLevel)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/SafetyLevel)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/SafetyLevel?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/SafetyLevel?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/PHP/SafetyLevel?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/SafetyLevel)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/SafetyLevel?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/PHP/SafetyLevel?template=oopsmore&param1=1.1&param2=1.1)
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
Safety Level {#safety-level .twikiTopicTitle}
============

::: {.twikiWebTitle}
Static analysis for PHP
:::

Safety levels are used to represent the level of security a variable has
within the security analysis.

The set of safety levels is finite and has a partial order by \<=. The
order is reflexive, transitive and antisymetric.

The levels are not given a number, but a name. This allows for further
extension in the future. Safety levels that are ranked higher are safer.

  [Name(s)](SafetyLevel@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Explenation](SafetyLevel@sortcol=1&table=1&up=0#sorted_table "Sort by this column")
  ---------------------------------------------------------------------------------- --------------------------------------------------------------------------------------
  safe                                                                               Safe/Unknown (default value for variables), upper bound
  integer-type, null-type, object-type, array-type, float-type                       Specific types
  string-from-list, matched-string                                                   String is matched to a certain value.
  formatted-string, encoded-string                                                   String is formatted in a special way (e.g. dates, hashed)
  escaped-html, escaped-shell, escaped-slashes                                       String has no un-escaped character sequences
  raw-input                                                                          Raw input that is not to be trusted
  unsafe                                                                             Lower bound

\-- [EricBouwers](../Main/EricBouwers){.twikiLink} - 29 Dec 2006\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
