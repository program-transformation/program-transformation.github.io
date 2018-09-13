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
    Page](http://www.program-transformation.org/edit/Transform/KHEPERA?t=1536826327)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/KHEPERA)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/KHEPERA)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/KHEPERA?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/KHEPERA?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/KHEPERA?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/KHEPERA)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/KHEPERA?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/KHEPERA?template=oopsmore&param1=1.1&param2=1.1)
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
KHEPERA {#khepera .twikiTopicTitle}
=======

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**The Khepera Transformation System**

*A system for [DSL](DSL){.twikiLink} implementation by source-to-source
transformation*

Khepera is a tool kit for rapid implementation and long-term maintenance
of domain-specific languages via source-to-source transformation,
separated into three phases: parsing, AST transformation, and
pretty-printing.

*Transformation language*

For the implementation of AST transformations, the Khepera system offers
a special \`little language\' that is compiled into C code. This
transformation language allows transformation rules to be specified that
perform conditional pattern-matches on trees. A special construct for
iterating over children is provided, as well as a construct for escaping
to C.

*Homepage*

<http://www.cs.unc.edu/~faith/khepera.html>\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
