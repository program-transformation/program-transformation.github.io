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
    Page](http://www.program-transformation.org/edit/Transform/GenerativeCoreConcepts?t=1536826490)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/GenerativeCoreConcepts)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/GenerativeCoreConcepts)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/GenerativeCoreConcepts?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/GenerativeCoreConcepts?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Transform/GenerativeCoreConcepts?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/GenerativeCoreConcepts?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/GenerativeCoreConcepts?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/GenerativeCoreConcepts?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/GenerativeCoreConcepts?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/GenerativeCoreConcepts?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/GenerativeCoreConcepts)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/GenerativeCoreConcepts?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Transform/GenerativeCoreConcepts?template=oopsmore&param1=1.6&param2=1.6)
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
Generative Core Concepts {#generative-core-concepts .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Generative_Domain_Model} Generative Domain Model
----------------------------------------------------

The key to automating the assembly of software systems is a generative
domain model (GDM) that consists of a problem space, a solution space,
and the configuration knowledge mapping between them (see [Fig.
GDM](GenerativeCoreConcepts#GDMFigAnchor){.twikiAnchorLink}). The
solution space comprises the implementation components and the common
system family architecture, defining all valid combinations of the
implementation components. Typically, the implementation components are
designed for maximum combinability, minimum redundancy, and maximized
reuse. The problem space, on the other hand, consists of the
application-oriented concepts and features that application engineers
use to express their needs. This space is implemented as a
domain-specific language ([DSL](DSL){.twikiLink}). Because of the
different goals, the structure of the problem space and the structure of
the solution space will be different, and they usually cannot be aligned
without sacrificing simplicity and domain-specificity in the problem
space or reuse and flexibility in the solution space. The configuration
knowledge specifies illegal feature combinations, default settings,
default dependencies (some defaults may be computed based on some other
features), construction rules (combinations of certain features
translate into certain combinations of implementation components), and
optimizations. The configuration knowledge may be implemented using
different forms of metaprogramming, e.g., dynamic reflection, object
factories, and program generators. The automatically created products
may also contain non-software artifacts, such as test plans, manuals,
tutorials, maintenance guidelines, etc. \--
[KrzysztofCzarnecki](../Main/KrzysztofCzarnecki){.twikiLink} - 28 Nov
2002

[]{#GDMFigAnchor}

-   Fig. GDM: Elements of a generative domain model: \[from the
    [GenerativeProgrammingBook](GenerativeProgrammingBook){.twikiLink}\]\
    ![gdm.gif](../pub/Transform/GenerativeCoreConcepts/gdm.gif){width="533"
    height="269"}

[]{#Network_of_Domains} Network of Domains
------------------------------------------

One important observation about a GDM is that it can be viewed
recursively, i.e., someone\'s problem space may be someone else\'s
solution space. Furthermore, one [DSL](DSL){.twikiLink} may be
implemented using many [DSLs](DSLs){.twikiLink} from other domains. In
general, we get a network of domains that may also contain cycles (see
[Fig. DN](GenerativeCoreConcepts#DNFigAnchor){.twikiAnchorLink}). This
concept was introduced by [JimNeighbors](JimNeighbors){.twikiLink}. \--
[KrzysztofCzarnecki](../Main/KrzysztofCzarnecki){.twikiLink} - 28 Nov
2002

[]{#DNFigAnchor}

-   Fig. DN: Example of a network of domains:\
    ![network.gif](../pub/Transform/GenerativeCoreConcepts/network.gif){width="476"
    height="374"}

[]{#Technology_Projections} Technology Projections
--------------------------------------------------

Each of the elements of a generative domain model can be implemented
using different technologies, which gives rise to different technology
projections (see [Fig.
TP](GenerativeCoreConcepts#TPFigAnchor){.twikiAnchorLink}):

-   Components can be implemented using, e.g., generic components (such
    as in the STL), component models (e.g.,
    [JavaBeans[^?^](http://www.program-transformation.org/edit/Transform/JavaBeans?topicparent=Transform.GenerativeCoreConcepts)]{.twikiNewLink
    style="background : #FFFFCE;"},
    [ActiveX[^?^](http://www.program-transformation.org/edit/Transform/ActiveX?topicparent=Transform.GenerativeCoreConcepts)]{.twikiNewLink
    style="background : #FFFFCE;"}, or CORBA), or aspect-oriented
    programming approaches.
-   Generators can be implemented using preprocessors (e.g., template
    processors), application generators, built-in metaprogramming
    capabilities of a language (e.g., template metaprogramming in C++),
    or extendible programming systems.
-   [DSLs](DSLs){.twikiLink} can be implemented using new textual or
    graphical languages (or language extensions), programming
    language-specific features, or interactive wizards.

\-- [KrzysztofCzarnecki](../Main/KrzysztofCzarnecki){.twikiLink} - 28
Nov 2002

[]{#TPFigAnchor}

-   Fig. TP: Technology projections:\
    ![techprojections.gif](../pub/Transform/GenerativeCoreConcepts/techprojections.gif){width="523"
    height="375"}

[]{#Drawing_the_Map} Drawing the Map
------------------------------------

[Fig. GM](GenerativeCoreConcepts#GMFigAnchor){.twikiAnchorLink}
classifies a number of fields by relating them to the elements of a
generative domain model. (this figure was taken from the report on the
[ECOOP](ECOOP){.twikiLink}\'01 workshop on Generative Programming).
Components, architectures, and generic programming are primarily related
to the solution space. Aspect-oriented programming provides more
powerful encapsulation mechanisms than traditional component
technologies. In particular, it allows us to replace many \"little,
scattered components\" (such as those needed for logging or
synchronization) and the configuration knowledge related to these
components by well encapsulated aspectual modules. However, we still
need to configure aspects and other components to implement abstract
features such as performance properties. Therefore, aspect-oriented
programming technologies such as [AspectJ](AspectJ){.twikiLink} cover
the solution space and only a part of the configuration knowledge. But
aspects can be also found in the problem space, esp. in the context of
[DSLs](DSLs){.twikiLink} used to described different aspects of a single
system (the original workshop figure did not have this \"aspect-oriented
[DSLs](DSLs){.twikiLink}\" entry). The problem space and the front part
of the configuration knowledge are addressed by areas such as
[DSLs](DSLs){.twikiLink}, feature modeling, and feature interactions.
Finally, system family and product line engineering span across the
entire generative domain model because they provide the overall
structure of the development process (including
[DomainEngineering](DomainEngineering){.twikiLink} and
[ApplicationEngineering[^?^](http://www.program-transformation.org/edit/Transform/ApplicationEngineering?topicparent=Transform.GenerativeCoreConcepts)]{.twikiNewLink
style="background : #FFFFCE;"}). \--
[KrzysztofCzarnecki](../Main/KrzysztofCzarnecki){.twikiLink} - 28 Nov
2002

[]{#GMFigAnchor}

-   Fig. GM: The map:\
    ![map.gif](../pub/Transform/GenerativeCoreConcepts/map.gif){width="547"
    height="313"}

------------------------------------------------------------------------

[CategoryGenerativeProgrammingWiki](CategoryGenerativeProgrammingWiki){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
