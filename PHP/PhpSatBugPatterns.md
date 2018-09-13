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
    Page](http://www.program-transformation.org/edit/PHP/PhpSatBugPatterns?t=1536825868)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpSatBugPatterns)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpSatBugPatterns)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpSatBugPatterns?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpSatBugPatterns?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/PHP/PhpSatBugPatterns?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/PHP/PhpSatBugPatterns?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/PHP/PhpSatBugPatterns?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/PHP/PhpSatBugPatterns?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/PHP/PhpSatBugPatterns?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/PHP/PhpSatBugPatterns?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpSatBugPatterns)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpSatBugPatterns?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpSatBugPatterns?template=oopsmore&param1=1.5&param2=1.5)
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
Php Sat Bug Patterns {#php-sat-bug-patterns .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Static analysis for PHP
:::

::: {.twikiToc}
-   [What is a bug-pattern?](PhpSatBugPatterns#What_is_a_bug_pattern)
-   [Descriptions](PhpSatBugPatterns#Descriptions)
    -   [Correctness](PhpSatBugPatterns#Correctness)
    -   [Exposing Info](PhpSatBugPatterns#Exposing_Info)
    -   [Optimization](PhpSatBugPatterns#Optimization)
    -   [Style](PhpSatBugPatterns#Style)
    -   [Malicious Code
        Vulnerability](PhpSatBugPatterns#Malicious_Code_Vulnerability)
-   [Results](PhpSatBugPatterns#Results)
    -   [Interpretation](PhpSatBugPatterns#Interpretation)
:::

[]{#What_is_a_bug_pattern}[]{#What_is_a_bug_pattern_} What is a bug-pattern?
----------------------------------------------------------------------------

Let us start with a definition:

      A bug-pattern describes a common mistake at the application level.

So each bug-pattern describes a pattern that is correct according to the
grammar of PHP, but holds a mistake that is *probably* not intended by
the programmer. The patterns are based on the documentation of PHP, past
experience and common sense. Notice that the patterns holds information
about *possible* mistakes, the programmer has to decide whether the
pattern is an actual mistake in the specific situation.

[]{#Descriptions} Descriptions
------------------------------

Each pattern is described according to this structure:

    [Code]
      Number of the pattern, First capitals of the category followed by a three-digit number.

    [Affected versions]
      PHP versions that are affected by this pattern.

    [Example]
      Code example that shows the pattern in a generalized way.
      
    [Usage]
      The situations in which this pattern can arise.
      
    [Why]
      Explanation of the mistake in this pattern.

    [Solution]
      How the pattern can be eliminated. 

The bug-patterns are divided into the following categories:

-   Correctness
-   Exposing Info
-   Optimization
-   Style
-   Malicious Code Vulnerability

There is no nicely formatted descriptions of the patterns (yet), but
there is documentation about the patterns in the
[SVN-repository](https://svn.strategoxt.org/repos/psat/php-sat/trunk/doc/).
Some of the patterns are not implemented, see this
[issue-list](http://bugs.strategoxt.org/secure/IssueNavigator.jspa?reset=true&&query=bugpattern&summary=true&description=true&body=true)
for the status of these patterns. If you have a pattern that can is
useful, please [share your
idea](http://bugs.strategoxt.org/secure/CreateIssue!default.jspa)!

### []{#Correctness} Correctness

[These
patterns](https://svn.strategoxt.org/repos/psat/php-sat/trunk/doc/correctness/)
describe a situation that is incorrect according to type-casting,
control-flow or the PHP documentation.

### []{#Exposing_Info} Exposing Info

[These
patterns](https://svn.strategoxt.org/repos/psat/php-sat/trunk/doc/exposing_info/)
describe a situation where information can leak from your application to
the outside world. This is a mistake in general because it reveals
information to attackers.

### []{#Optimization} Optimization

[These
patterns](https://svn.strategoxt.org/repos/psat/php-sat/trunk/doc/optimization/)
indicate places where you can gain a (microscopic) performance boost.
None of the patterns will double the speed of your application at once,
but together they help you to get the best out of your server resources.

### []{#Style} Style

[These
patterns](https://svn.strategoxt.org/repos/psat/php-sat/trunk/doc/style/)
flag situations that violate a certain style-guide. Notice that they are
subjective, but they also have a non-arbitrary reason to flag the
situation.

### []{#Malicious_Code_Vulnerability} Malicious Code Vulnerability

This category consists of only one bug-pattern
[MCV000](PhpSatMCV000){.twikiLink}. This pattern flags parameters that
do not meet the pre-condition of the called function. This pattern finds
pieces of code that might have security issues, please take a good look
at the code before ignoring the pattern.

[]{#Results} Results
--------------------

Within normal mode the output of PHP-Sat looks like this: Pattern
\[number\] found in file \[file-name\] on line \[line-number\].

However, if you pass the `--extended-ouput` option to PHP-Sat the
generated files will contain special code blocks that look like this:

      /**
       * PHP-SAT check (Category name)
       * Pattern ID : Pattern code
       * Description: Short description / pattern name
       */

### []{#Interpretation} Interpretation

The patterns that PHP-Sat flags are common mistakes, but not necessarily
bad in your situation. You have to decide for yourself whether or not
you want to adjust your code. We just want to provide you with more
information to make the right decision, we know you can do it!\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
