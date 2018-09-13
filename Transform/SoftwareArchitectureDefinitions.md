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
    Page](http://www.program-transformation.org/edit/Transform/SoftwareArchitectureDefinitions?t=1536826567)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/SoftwareArchitectureDefinitions)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/SoftwareArchitectureDefinitions)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/SoftwareArchitectureDefinitions?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/SoftwareArchitectureDefinitions?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/SoftwareArchitectureDefinitions?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/SoftwareArchitectureDefinitions?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/SoftwareArchitectureDefinitions?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/SoftwareArchitectureDefinitions?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/SoftwareArchitectureDefinitions?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/SoftwareArchitectureDefinitions?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/SoftwareArchitectureDefinitions)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/SoftwareArchitectureDefinitions?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/SoftwareArchitectureDefinitions?template=oopsmore&param1=1.4&param2=1.4)
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
Software Architecture Definitions {#software-architecture-definitions .twikiTopicTitle}
=================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Definitions of Software Architecture.**

There are many definitions of what
[SoftwareArchitecture](SoftwareArchitecture){.twikiLink} is: an overview
of these is given at
<http://www.sei.cmu.edu/architecture/definitions.html>, to which you can
even add your own favorite definition.

------------------------------------------------------------------------

The [IEEE](IEEE){.twikiLink} defines software architecture as

-   *the fundamental organization of a system embodied in its
    components, their relationships to each other and to the environment
    and the principles guiding its design and evolution.* \-- see
    <http://www.pithecanthropus.com/~awg/p1471_faq_rev2.html>

------------------------------------------------------------------------

Conceptually that definition of sw arch is ok, but practically it
doesn\'t provide any concrete guidelines for the process of describing a
swarchitecture. I usually prefer to use the definition that we
elaboratedduring an European project (ARES) and it\'s reported in the
book \"Software Architecture for Product Families\"
<http://www.amazon.com/exec/obidos/ASIN/0201699672/ref=ase_re/002-9221677-3311232>

The definition emphasizes the purpose of a sw arch that is to satisfy
functional and quality requirements of a system:

-   *Software architecture is a set of concepts and design decisions
    about structure and texture of software that must be made prior to
    concurrent engineering to enable effective satisfaction of
    architecturally significant, explicit functional and quality
    requirements, and implicit requirements of the problem and the
    solution domains.*

\--
[ClaudioRiva[^?^](http://www.program-transformation.org/edit/Main/ClaudioRiva?topicparent=Transform.SoftwareArchitectureDefinitions)]{.twikiNewLink
style="background : #FFFFCE;"}

*I should probably read the book, but*

-   *what is the texture of software?*
-   *Doesn\'t \"architecturally significant\" introduce a cycle?*

\--ArieVanDeursen

------------------------------------------------------------------------

*Software Architecture in Practice* by Bass, Clements and Kazman
(Addison Wesley, 1998), pp 23-24, defines architecture as follows:

-   The software architecture of a program or computing system is the
    structure or structures of the system, which comprise software
    components, the externally visible properties of those components,
    and the relationships among them.

*What I like about this defintition is that it includes the notion of
**architectural structure**, and that one system can consists of
multiple structures. In other words, no one structure can claim to be
**the** architecture* \-- [ArieVanDeursen](ArieVanDeursen){.twikiLink}.

------------------------------------------------------------------------

In their book on the
[UnifiedProcess[^?^](http://www.program-transformation.org/edit/Transform/UnifiedProcess?topicparent=Transform.SoftwareArchitectureDefinitions)]{.twikiNewLink
style="background : #FFFFCE;"}, Jacobson and friends also emphasize that
architecture *is a set of design decisions*. In addition to structure,
architecture in their view is also concerned with usage, functionality,
performance, resilience, reuse, comprehensibility, economomc and
technological constrains and trade-offs, and aesthetics (The Unified
Software Development Process, p. 61 / 443) \--
[ArieVanDeursen](ArieVanDeursen){.twikiLink}

------------------------------------------------------------------------

[CategoryArchitecture](CategoryArchitecture){.twikiLink} \| Contibutions
by [ArieVanDeursen](ArieVanDeursen){.twikiLink},
[RainerKoschke](RainerKoschke){.twikiLink},
[ClaudioRiva[^?^](http://www.program-transformation.org/edit/Main/ClaudioRiva?topicparent=Transform.SoftwareArchitectureDefinitions)]{.twikiNewLink
style="background : #FFFFCE;"}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
