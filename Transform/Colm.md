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
    Page](http://www.program-transformation.org/edit/Transform/Colm?t=1536826318)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/Colm)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/Colm)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/Colm?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/Colm?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/Colm?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/Colm)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/Colm?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/Colm?template=oopsmore&param1=1.1&param2=1.1)
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
Colm {#colm .twikiTopicTitle}
====

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Colm_COmputer_Language_Manipulat} Colm: COmputer Language Manipulation
--------------------------------------------------------------------------

**Homepage:** <http://www.complang.org/colm/>

Colm is a programming language designed for the analysis and
transformation of computer languages. Colm is a program transformation
language, influenced primarily by [TXL](TXL){.twikiLink}. A
transformation language has a type system based on formal languages.
Rather than define classes or data structures, one defines grammars. A
parser is constructed automatically from the grammar and is used for two
purposes: to parse the input language and to parse the structural
patterns in the program that performs the analysis. In this setting
grammar-based parsing is critical because it guarantees that both the
input and the structural patterns are parsed into trees from the same
set of types, allowing comparison.

Colm\'s first contribution lies in the parsing method. Colm\'s parsing
engine is generalized, but it also allows for the construction of
arbitrary global data structures that can be queried during parsing. In
other generalized methods construction of global data requires some very
careful consideration because of inherent concurrency in the parsing
method. It is such a tricky task that it is often avoided altogether and
the problem is deferred to a post-parse disambiguation of the parse
forest. Using Colm it is possible to get the correct parse tree on the
first pass. Colm eliminates the need to reason about concurrent updates
to global data or to acquire many possible parse trees only to throw
away the incorrect ones.

Colm\'s second main contribution is in its syntax and control
structures, which are designed to mimic those in open-source scripting
languages such as Ruby and Python, and thus make source transformation
more familiar and accessible to ordinary programmers.

------------------------------------------------------------------------

[CategorySystem](CategorySystem){.twikiLink} \|
[TransformationSystems](TransformationSystems){.twikiLink} \|
Contributions by [JamesCordy](JamesCordy){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
