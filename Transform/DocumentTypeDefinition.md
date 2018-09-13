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
    Page](http://www.program-transformation.org/edit/Transform/DocumentTypeDefinition?t=1536826227)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DocumentTypeDefinition)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DocumentTypeDefinition)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DocumentTypeDefinition?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DocumentTypeDefinition?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/DocumentTypeDefinition?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DocumentTypeDefinition)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DocumentTypeDefinition?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/DocumentTypeDefinition?template=oopsmore&param1=1.1&param2=1.1)
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
Document Type Definition {#document-type-definition .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[DocumentTypeDefinition](DocumentTypeDefinition){.twikiLink} (DTD) is
the original [SchemaLanguageForXML](SchemaLanguageForXML){.twikiLink}
and is in fact part of the [XML](XML){.twikiLink} standard.

DTD is a
[LocalTreeGrammar[^?^](http://www.program-transformation.org/edit/Transform/LocalTreeGrammar?topicparent=Transform.DocumentTypeDefinition)]{.twikiNewLink
style="background : #FFFFCE;"}. This means that the same terminal
(production label) cannot be used for different non-terminals. DTD
enforces this by making non-terminals and terminals equivalent: it is
not possible to specify non-terminals. Because of this tree-locality
property it is straightforward to create an interpretation of an
[XML](XML){.twikiLink} document against a DTD: there is one to one
mapping from the [XML](XML){.twikiLink} tags to production rules and
thus to non-terminals.

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 30 May
2002\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
