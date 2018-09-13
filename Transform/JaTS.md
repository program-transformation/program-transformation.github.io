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
    Page](http://www.program-transformation.org/edit/Transform/JaTS?t=1536826325)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/JaTS)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/JaTS)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/JaTS?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/JaTS?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/JaTS?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/JaTS?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/JaTS?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/JaTS?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/JaTS?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/JaTS?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/JaTS)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/JaTS?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/JaTS?template=oopsmore&param1=1.4&param2=1.4)
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
Ja TS {#ja-ts .twikiTopicTitle}
=====

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Transformation system for the Java programming language.

Program transformation is a powerful technique for supporting software
engineering activities: refactoring, formal software development, code
generation and language translation.

In fact, refactoring, the process of restructuring code with the purpose
of making it easier to understand and maintain without changing its
observable behavior, is strongly coupled with program transformation.
Refactorings can be specified as parameterized program transformations
that obey behavior-preserving preconditions. Nowadays, the use of
refactoring to increase quality is considered a very important
development practice. For instance, Extreme Programming , a approach for
software development, recommends the use of refactoring as a continuous
activity, intimately related to coding. Formal and rigorous software
development methods are strong candidates to the use of program
transformation as well, since refinement laws can be easily described as
program transformations satisfying preconditions that guarantee the
soundness of the refinement. This is the case for imperative languages,
as in the refinement calculus, but also for object oriented languages.
In both cases, algebraic laws for programming languages can be viewed
and implemented as program transformations.

Those applications of program transformation show its importance, but
its use in practical, large scale, projects is not possible without
automation. Tool support is vital to the application of program
transformations, in order to provide productivity and eliminate the
danger of introducing errors, when performing such a tedious and
demanding task. Several program transformation tools have been
implemented. Many of these are not language specific, being able to
transform programs from an arbitrary source language to an arbitrary
destination language. Although this may be an advantage, it complicates
the use of the tools, since they require two kinds of user: the
transformation engineer, who configures the tool (encodes the
transformations) and the programmer, who uses the tool for software
development (applies the transformations). This is usually necessary
because, in most cases, the language in which the transformations are
encoded is substantially different from the one to which they are
applied.

There are also language-specific tools for program transformation. Most
of these have the drawback of supporting only a fixed set of built-in
transformations. For instance, refactoring systems usually implement a
few simple refactorings that can be applied, but a programmer cannot add
a new refactoring to this tool, unless he has access to the source code
of the system. Formal software development systems are usually similar:
they support a set of built-in refinement laws that cannot be extended.

In order to avoid the drawbacks of the general purpose and
language-specific transformation tools, we present a language to specify
program transformations for the Java programming language. In this
language, transformations are specified using a superset of Java, making
it easier for programmers to specify the transformations they wish to
apply and thus eliminating the need for the transformation engineer.
Also, it takes the semantics of Java into account, making it possible to
implement transformations that could not be implemented if only the
syntax was taken into account. The language has been named
[JaTS](JaTS){.twikiLink}, an acronym for Java Transformation System, the
system that actually implements this language and applies
transformations to Java programs.

Related Papers

-   [A Language for Specifying Java
    Transformations](http://www.cin.ufpe.br/~phmb/papers/JaTSALinguagemSBLP2001.pdf)
-   [JaTS: A Java Transformation
    System](http://www.cin.ufpe.br/~phmb/papers/JaTSAFerramentaSBES2001.ps)
-   [Integrating code generation and
    refactoring](http://www.cin.ufpe.br/~phmb/papers/CoderECOOP2002.ps)

Related Links

-   [JaTS Project Home Page](http://www.cin.ufpe.br/~jats)
-   [Qualiti Coder](http://coder.qualiti.com/) : Through code generation
    and update, this tool offers automation in code lines production.
    [JaTS](JaTS){.twikiLink} is its nucleus and it is being developed by
    [Qualiti Software Processes](http://www.qualiti.com/)
-   [Software Productivity Group](http://www.cin.ufpe.br/spg)

\-- [AdelineSousa](../Main/AdelineSousa){.twikiLink} - 16 Jun 2004

\-- [MaratBoshernitsan](../Main/MaratBoshernitsan){.twikiLink} - 19 Apr
2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
