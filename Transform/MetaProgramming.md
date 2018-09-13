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
    Page](http://www.program-transformation.org/edit/Transform/MetaProgramming?t=1536825737)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/MetaProgramming)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/MetaProgramming)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/MetaProgramming?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/MetaProgramming?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Transform/MetaProgramming?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/MetaProgramming?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/MetaProgramming?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/MetaProgramming?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/MetaProgramming?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/MetaProgramming?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/MetaProgramming)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/MetaProgramming?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Transform/MetaProgramming?template=oopsmore&param1=1.5&param2=1.5)
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
Meta Programming {#meta-programming .twikiTopicTitle}
================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Staged_Meta_Programming} Staged Meta Programming
----------------------------------------------------

Staged languages distinguish stages of execution. Many compile-time
meta-programming systems distinguish only a run-time and a compile-time.
[MetaML](MetaML){.twikiLink} does not restrict the number of stages.

-   [MetaML](MetaML){.twikiLink}

[]{#Template_Meta_Programming} Template Meta Programming
--------------------------------------------------------

-   [Template Haskell](TemplateHaskell){.twikiLink}
-   [C++ Templates](CppTemplates){.twikiLink}

[]{#Macro_Systems} Macro Systems
--------------------------------

Macros generate code. Macro systems that operate at the lexical level
are usually called lexical macros. Lexical macro systems are often
independent of specific programming language. Macro system that operate
on a structured representations of source code are called syntax macros.
Macro systems mainly vary in the what the macro is able to do with macro
arguments and how the macros are to be invoked. Some macro systems allow
the definition of a context-free syntax for the arguments of the macro.
Hygience macro systems avoid unintended capturing of identifiers that
are used in the context or in the macro definition.

-   [Lisp](LispLanguage){.twikiLink} Macros
-   [Scheme](SchemeLanguage){.twikiLink} R5RS Macros
-   Syntax macros in [Bigwig](Bigwig){.twikiLink}
-   [Maya](Maya){.twikiLink}

[]{#Aspect_Oriented_Programming} Aspect-Oriented Programming
------------------------------------------------------------

-   [AspectJ](AspectJ){.twikiLink}
-   [AspectL](http://common-lisp.net/project/aspectl/)

[]{#Quotation_and_Antiquotation} Quotation and Antiquotation
------------------------------------------------------------

-   [Camlp4](http://caml.inria.fr/camlp4/manual/index.html)
-   SML/NJ [Object Language Embedding with
    Quote/Antiquote](http://cm.bell-labs.com/cm/cs/what/smlnj/doc/quote.html)
-   [Isabelle\'s
    Logics](http://www.cl.cam.ac.uk/Research/HVG/Isabelle/logics.html)
-   [Programmable Syntax
    Macros](http://citeseer.nj.nec.com/weise93programmable.html)
-   [Meta Programming with Concrete Object
    Syntax](../Stratego/MetaProgrammingWithConcreteObjectSyntax){.twikiLink}

[]{#Systems} Systems
--------------------

-   [GRAMPS](GRAMPS){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
