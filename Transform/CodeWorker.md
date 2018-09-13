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
    Page](http://www.program-transformation.org/edit/Transform/CodeWorker?t=1536826443)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/CodeWorker)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/CodeWorker)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/CodeWorker?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/CodeWorker?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/CodeWorker?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/CodeWorker?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/CodeWorker?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/CodeWorker)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/CodeWorker?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/CodeWorker?template=oopsmore&param1=1.2&param2=1.2)
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
Code Worker {#code-worker .twikiTopicTitle}
===========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This tool is a scripting language (distributed under LGPL at
<http://www.codeworker.org>) dedicated to automate the development
process, from requirements specification to IT system development. It is
mainly used for building
[SoftwareGenerators](SoftwareGenerators){.twikiLink} intended to produce
[SoftwareProductLines](SoftwareProductLine){.twikiLink}.

The scripting language adapts its syntax to the subject it has to
handle:

-   an extended-BNF syntax (declarative part of the language) for
    recognizing the format of the specifications to parse, so as to
    define
    [DomainSpecificLanguages](DomainSpecificLanguages){.twikiLink},
-   a procedural language for manipulating easily parse trees (the only
    structured type admitted by [CodeWorker](CodeWorker){.twikiLink}),
    strings, files and directories,
-   a template-based syntax (imperative part) like in PHP or JSP, which
    facilitates the writing of template-based code generation.

Thanks to this syntax adaptation, the scripting language is able to
easily:

-   acquire any kind of specification of the IT system to produce
    (people often prefers [XML](XML){.twikiLink}, but it isn\'t
    necessary : do easily your own adapted data format),
-   generate source code in a classical way (as Rational ROSE), managing
    preserved areas of text that accept hand-typed code,
-   expand a source file like the class-wizard of Visual C++ (generated
    text is inserted at specified markups in the source code),
-   translate from a format to another ([LaTeX](LaTeX){.twikiLink} to
    [HTML](HTML){.twikiLink}, [XSL](XSL){.twikiLink} to
    [CodeWorker](CodeWorker){.twikiLink}, \... no limit to
    source-to-source translation),
-   transform a source file (to instrument a source file with profiling
    features, \...
    [ProgramTransformation](ProgramTransformation){.twikiLink}).

These tasks are executed in a straightforward process, with no binding
to an external programming language and with no translation of
requirements specification.

\-- [CedricLemaire](../Main/CedricLemaire){.twikiLink} - 31 Jul 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
