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
    Page](http://www.program-transformation.org/edit/Transform/XrayArchitectureRecovery?t=1536826410)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/XrayArchitectureRecovery)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/XrayArchitectureRecovery)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/XrayArchitectureRecovery?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/XrayArchitectureRecovery?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/XrayArchitectureRecovery?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/XrayArchitectureRecovery?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/XrayArchitectureRecovery?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/XrayArchitectureRecovery)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/XrayArchitectureRecovery?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/XrayArchitectureRecovery?template=oopsmore&param1=1.2&param2=1.2)
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
Xray Architecture Recovery {#xray-architecture-recovery .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The design and evaluation of appropriate
[SoftwareArchitectures](SoftwareArchitecture){.twikiLink} is key to the
effective development, management, evolution, and reuse of software
systems. However, current software engineering practice has generally
led to architectural designs that are informal, ad hoc, and difficult to
analyse and maintain. One consequence is that most existing systems have
little or no documented architectural information, and the information
that does exist is often an inaccurate representation of the implemented
architecture. All too often, architectural information about an
unfamiliar system needs to be extracted directly from the implemented
software artifacts. This is a very demanding process commonly referred
to as [ArchitectureExtraction](ArchitectureExtraction){.twikiLink}.
Although architecture recovery can be significantly facilitated with the
help of current [ReverseEngineering](ReverseEngineering){.twikiLink}
techniques and tools, many issues remain to be properly addressed,
particularly regarding recovery of the runtime abstractions (client,
servers, communication protocols, etc.) that are typical to the design
of distributed systems.

X-ray is a static reverse engineering approach to aid programmers in
recovering the runtime architecture of existing distributed systems.
X-ray comprises three domain-based static analysis techniques developed
to facilitate the identification of implemented executable components
and their potential runtime interconnections. The first
technique\-\--component module classification\-\--is used to identify
which compilation modules of the source constitute the code for each
implemented executable component. The second technique\-\--syntactic
pattern matching\-\--is used to help in the identification of code
constructs that might implement potential runtime interaction features.
The third and last technique\-\--structural reachability analysis\-\--is
used to facilitate association of features identified via the syntactic
pattern matching technique, to individual components. These three
techniques are supported by a proof-of-concept recovery prototype that
integrates several new and \`\`off-the-shelf\'\' tools.

To highlight the benefits of X-ray, the dissertation presents a detailed
account of two successful applications of the prototype to help recover
a static approximation of the runtime architecture of publicly available
distributed systems, including a 160,000 line distributed programming
environment.

Nabor das Chagas Mendonça

<http://www.doc.ic.ac.uk/~ndcm/>

N. C. Mendonça and J. Kramer. An approach for recovering distributed
system architectures. *[Automated Software
Engineering](AutomatedSoftwareEngineering){.twikiLink}* 8(3/4):311-354,
2001.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
