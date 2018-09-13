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
    Page](http://www.program-transformation.org/edit/Transform/ReusableGrammars?t=1536826548)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ReusableGrammars)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ReusableGrammars)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ReusableGrammars?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ReusableGrammars?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/ReusableGrammars?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/ReusableGrammars?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/ReusableGrammars?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/ReusableGrammars?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/ReusableGrammars?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/ReusableGrammars?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ReusableGrammars)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ReusableGrammars?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/ReusableGrammars?template=oopsmore&param1=1.4&param2=1.4)
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
Reusable Grammars {#reusable-grammars .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

A parser is an essential component of a
[TransformationSystem](TransformationSystem){.twikiLink}. It is often a
considerable investment to develop a good syntax definition for use in a
transformation system. To ease the development of transformation systems
it is helpful to develop grammars, syntax definitions, or parsers that
can be reused accross projects. This page is intended to collect
information on availability of reusable grammars and discuss issues in
making grammars reusable. \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 20 Oct 2001

------------------------------------------------------------------------

**Collections**

The following sites offer collections of reusable grammars. Please add
links to other sites.

-   The [SDF2](../Sdf/WebHome){.twikiLink}
    [GrammarBase](../Sdf/GrammarBase){.twikiLink}
-   Grammars homepage at VU: <http://www.cs.vu.nl/grammars/>
-   The [JavaCC](JavaCC){.twikiLink} grammar collection:
    <http://www.cobase.cs.ucla.edu/pub/javacc/>

------------------------------------------------------------------------

Reusing grammars across parser generators

A reusable syntax definition is not of much use when it is not written
for your favourite programming language. To make syntax definitions even
more reusable it useful to have migration tools that can be used to
translate a syntax definition from one formalism to another.

The Tools.XT transformation toolset provides tools for
[GrammarRecovery[^?^](http://www.program-transformation.org/edit/Transform/GrammarRecovery?topicparent=Transform.ReusableGrammars)]{.twikiNewLink
style="background : #FFFFCE;"}, e.g., translating YACC grammars to
[SDFII](SDFII){.twikiLink}, and
[SyntaxImprovement[^?^](http://www.program-transformation.org/edit/Transform/SyntaxImprovement?topicparent=Transform.ReusableGrammars)]{.twikiNewLink
style="background : #FFFFCE;"}.

------------------------------------------------------------------------

I bumbed into an article by [ChrisVerhoef](ChrisVerhoef){.twikiLink} and
[RalfLaemmel](RalfLaemmel){.twikiLink} the other day in which they
describe how to extract a usable grammar from the Cobol standard \--
just appeared in Software Practice and Experience. \--
[ArieVanDeusren[^?^](http://www.program-transformation.org/edit/Transform/ArieVanDeusren?topicparent=Transform.ReusableGrammars)]{.twikiNewLink
style="background : #FFFFCE;"}; 20 Oct 2001.

------------------------------------------------------------------------

[CategorySyntax](CategorySyntax){.twikiLink} \| Contributions by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
