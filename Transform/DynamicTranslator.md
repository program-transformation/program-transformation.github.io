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
    Page](http://www.program-transformation.org/edit/Transform/DynamicTranslator?t=1536825811)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DynamicTranslator)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DynamicTranslator)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DynamicTranslator?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DynamicTranslator?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/DynamicTranslator?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DynamicTranslator)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DynamicTranslator?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/DynamicTranslator?template=oopsmore&param1=1.1&param2=1.1)
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
Dynamic Translator {#dynamic-translator .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

A translator which performs its transformations *as the program is
running*. Because the user is waiting for the program to actually run
while the translation is happening, many expensive optimizations such as
[CommonSubexpressionElimination[^?^](http://www.program-transformation.org/edit/Transform/CommonSubexpressionElimination?topicparent=Transform.DynamicTranslator)]{.twikiNewLink
style="background : #FFFFCE;"} can\'t be performed, or at least are
postponed until the translator is very sure that the returns will be
realised.

However, the translator is very aware of where the hot spots are in the
program, and what frequently calls what. It turns out that code
placement is the most effective optimization for dynamic translators.

Despite the lack of traditional optimizations, dynamic translators are
capable of comparable performance compared with
[StaticTranslators](StaticTranslator){.twikiLink}.

Examples include Java and other JITs
([JustInTime](JustInTime){.twikiLink} dynamic compilers, which translate
from some [VirtualMachine](VirtualMachine){.twikiLink} representation
such as Java [ByteCodes](ByteCodes){.twikiLink} to native instructions),
[DynamicOptimizers[^?^](http://www.program-transformation.org/edit/Transform/DynamicOptimizers?topicparent=Transform.DynamicTranslator)]{.twikiNewLink
style="background : #FFFFCE;"} such as [Hewlett
Packard](http://www.hp.com)\'s
[Dynamo](http://www.hpl.hp.com/cambridge/projects/Dynamo), and dynamic
binary translators (see
[BinaryTranslation](BinaryTranslation){.twikiLink}).

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 01 Dec 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
