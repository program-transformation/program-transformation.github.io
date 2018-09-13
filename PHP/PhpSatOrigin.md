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
    Page](http://www.program-transformation.org/edit/PHP/PhpSatOrigin?t=1536825868)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpSatOrigin)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpSatOrigin)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpSatOrigin?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpSatOrigin?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/PHP/PhpSatOrigin?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/PHP/PhpSatOrigin?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/PHP/PhpSatOrigin?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/PHP/PhpSatOrigin?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/PHP/PhpSatOrigin?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpSatOrigin)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpSatOrigin?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpSatOrigin?template=oopsmore&param1=1.3&param2=1.3)
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
Php Sat Origin {#php-sat-origin .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Static analysis for PHP
:::

There where two sources that made the idea for PHP-Sat. The first source
of inspiration came from my work as a assistant at the course
[\"internet programmeren\" (Internet Programming)
(2005,2006)](http://www.cs.uu.nl/docs/vakken/inp/) at my [University
department](http://www.cs.uu.nl/). I noticed that a lot of students
where not aware of the security problems involved when programming PHP
for the web.

The other source of inspiration came from a
[practical](http://www.cs.uu.nl/wiki/Pt/AssignmentAbstractInterpretation)
assignment that I had to do for the course [Programming Transformation
(2006)](http://www.cs.uu.nl/wiki/Pt/WebHome). A part of this assignment
was about tracking knowledge about variables that possibly contain
null-pointers.

These two inspiration-sources lead me to the idea of a program that
would track the state of a variable, if it was tainted or not, and then
warn a user when this was used at the wrong places. This could be used
by students to check and improve there programs before they submit.

I wanted to work out this idea, but I had to get a job for the summer to
be able to pay my bills. A combination of these two was found in
Google\'s [Summer of Code](http://code.google.com/soc/) 2006. So I asked
the person in charge of the course, [Eelco Visser](../Main/EelcoVisser)
if this idea was any good. In a short talk at the elevators I told him
my idea and asked him about the Summer of Code. He was interested and
there was sure to be someone who could mentor me.

So I started writing on my proposal. I found out that the idea was not
really new because [Nenad
Jovanovic](http://www.seclab.tuwien.ac.at/people/enji/) was already
developing [Pixy](http://www.seclab.tuwien.ac.at/projects/pixy/). An
other project that was related is
[PHC](http://www.phpcompiler.org/index.html), the open source PHP
compiler. I still wanted to continue with my idea, the reasons for this
are all captured in my [SoC-proposal](SocApplication){.twikiLink}.

I had written this application and applied for the Summer of Code with
it. Since there where about 6000 applications, changes where not very
good. Especially because I wanted to work on a new project instead of an
existing one. When the accepted applications where announced there was a
bit of confusion. I had send in my proposal to both PHP and Google, but
PHP had moved it to Google. My proposal that was send to Google was not
accepted, but the one that was send to PHP and moved to Google was! I
was off course very happy, and started reading some related papers. I
was told that I would get a mentor from PHP, but there was no progress
on this subject for a week. I proposed to Google that they would accept
[Martin](../Main/MartinBravenboer) as my mentor. They agreed to this
very soon and the development could really get started.

The development of a good vulnerability detection strategy takes a lot
of time. During the development of this strategy Martin suggested to add
bug patterns to PHP-Sat. A bug pattern detects a pattern in source code
that could indicate a bug, a optimization possibility or a
style-violation. This would already make the tool useful when the
vulnerability detection strategy was not completely implemented.

More info about the name can be found on the
[name](PhpSatName){.twikiLink} page.

\-- [EricBouwers](../Main/EricBouwers){.twikiLink} - 09 Sep 2006\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
