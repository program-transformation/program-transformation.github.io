::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/ObjectOrientedFramework?t=1536826522)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ObjectOrientedFramework)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ObjectOrientedFramework)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ObjectOrientedFramework?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ObjectOrientedFramework?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/Transform/ObjectOrientedFramework?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Transform/ObjectOrientedFramework?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Transform/ObjectOrientedFramework?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Transform/ObjectOrientedFramework?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Transform/ObjectOrientedFramework?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Transform/ObjectOrientedFramework?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ObjectOrientedFramework)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ObjectOrientedFramework?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/Transform/ObjectOrientedFramework?template=oopsmore&param1=1.10&param2=1.10)
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
Object Oriented Framework {#object-oriented-framework .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

A framework is a *set of classes that embodies an abstract design for
solutions to a family of related problems*
([RalphJohnson](RalphJohnson){.twikiLink} and B. Foote, Journal of
Object-Oriented Programming 1(2), 1988).

You can specialize and/or instantiate these classes to implement an
application or subsystem. Typical issues:

-   Frameworks adopt an *inverse control flow*, sometimes called the
    *Holywood Principle* (don\'t call us, we\'ll call you): in contrast
    with a library, the methods you define to use the framework get
    called by the framework (for example through call backs or
    inheritance).
-   Design patterns can be used to document the structure of frameworks
    \-- for example IBM\'s San Francisco relies on the
    [ModelViewControler[^?^](http://www.program-transformation.org/edit/Transform/ModelViewControler?topicparent=Transform.ObjectOrientedFramework)]{.twikiNewLink
    style="background : #FFFFCE;"} pattern.
-   The interface between the framework and the application-specific
    parts built on top of it is realized as a set of extension points,
    or *hot spots*.

------------------------------------------------------------------------

Resources

-   The frameworks homepage at
    <http://www.ipd.hk-r.se/michaelm/fwpages/frameworks.html>
-   The [OOPSLA](OOPSLA){.twikiLink} conferences
-   The series of three books edited by Mohammed Fayad \-- see
    <http://www.cse.unl.edu/~fayad/> published by Addison Wesley.
-   The Framework Editor Fred from the University of Helsinki,
    <http://practise.cs.tut.fi/fred/>

------------------------------------------------------------------------

A well known industrial framework is IBM\'s San Francisco

-   see <http://www-4.ibm.com/software/ad/sanfrancisco/library/>
-   and
    <http://www-4.ibm.com/software/ad/sanfrancisco/library/concepts.html>
    for an introduction.

------------------------------------------------------------------------

The relationship between frameworks and
[DomainSpecificLanguages](DomainSpecificLanguages){.twikiLink} is
explored in:

-   [DonRoberts](DonRoberts){.twikiLink} and
    [RalphJohnson](RalphJohnson){.twikiLink}. Evolve frameworks into
    domain-specific languages. In 3rd International Conference on
    Pattern Languages, Allerton Park, Ill., September 1996. \-- see
    <http://citeseer.nj.nec.com/47194.html>,
    <http://citeseer.nj.nec.com/roberts96evolving.html>
-   [ArieVanDeursen](ArieVanDeursen){.twikiLink}. Domain-Specific
    Languages versus Object-Oriented Frameworks: A Financial Engineering
    Case Study. In Proceedings Smalltalk and Java in Industry and
    Academia, pages 35-39. Ilmenau Technical University, 1997.

Both are discussed in the
[DSLAnnotatedBibliography](DSLAnnotatedBibliography){.twikiLink} as
well.

------------------------------------------------------------------------

[CategoryArchitecture](CategoryArchitecture){.twikiLink} \|
Contributions by [ArieVanDeursen](ArieVanDeursen){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.ObjectOrientedFramework moved from
Transform.ObjectOrientedFrameworks on 13 Dec 2001 - 23:33 by
[ArieVanDeursen](../Main/ArieVanDeursen){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/ObjectOrientedFramework?newweb=Transform&newtopic=ObjectOrientedFrameworks&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
