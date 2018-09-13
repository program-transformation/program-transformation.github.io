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
    Page](http://www.program-transformation.org/edit/Transform/JakartaToolSuite?t=1536826501)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/JakartaToolSuite)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/JakartaToolSuite)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/JakartaToolSuite?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/JakartaToolSuite?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/JakartaToolSuite?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/JakartaToolSuite)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/JakartaToolSuite?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/JakartaToolSuite?template=oopsmore&param1=1.1&param2=1.1)
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
Jakarta Tool Suite {#jakarta-tool-suite .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Bali} Bali
--------------

Bali generate from a single grammar specification:

-   lexical analyzer (JLex)
-   parser ([CUP](CUP){.twikiLink})
-   class hierarchies for tree nodes, including unparsing methods
    (pretty printer)

[]{#Jak_language} Jak language
------------------------------

The Jak language extends the Java Language with support for the
implementation of meta-programs for the Java language. Jak for this
purpose embeds the concrete syntax of Java in Java. These concrete
syntax fragments are parsed at compile time to an SST (Surface Syntax
Tree, comparable to a parse tree). By invoking the typecheck method an
SST can be turned into an Abstract Syntax Tree. This happends at
run-time. The SST can be pretty-printed by invoking the print method on
an SST node.

[]{#Resources} Resources
------------------------

Website with Software and Publications:

-   <http://www.cs.utexas.edu/users/schwartz/software.html>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
