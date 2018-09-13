::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/LanguageIndependentTraversalsForProgramTransformation?t=1536825424)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/LanguageIndependentTraversalsForProgramTransformation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/LanguageIndependentTraversalsForProgramTransformation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/LanguageIndependentTraversalsForProgramTransformation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/LanguageIndependentTraversalsForProgramTransformation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/LanguageIndependentTraversalsForProgramTransformation?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/LanguageIndependentTraversalsForProgramTransformation?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/LanguageIndependentTraversalsForProgramTransformation?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/LanguageIndependentTraversalsForProgramTransformation?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/LanguageIndependentTraversalsForProgramTransformation?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/LanguageIndependentTraversalsForProgramTransformation?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/LanguageIndependentTraversalsForProgramTransformation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/LanguageIndependentTraversalsForProgramTransformation?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/LanguageIndependentTraversalsForProgramTransformation?template=oopsmore&param1=1.4&param2=1.4)
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
Language Independent Traversals For Program Transformation {#language-independent-traversals-for-program-transformation .twikiTopicTitle}
==========================================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Language Independent Traversals for Program Transformation.
[EelcoVisser](EelcoVisser){.twikiLink}. Workshop on
[GenericProgramming](../Transform/GenericProgramming){.twikiLink}
([WGP](../Transform/WGP){.twikiLink}\'00), July 2000. Ponte de Lima,
Portugal. [ps.gz](http://www.cs.uu.nl/people/visser/ftp/Vis00.ps.gz)

**Abstract**

Many language processing operations have a generic underlying algorithm.
However, these generic algorithms either have to be implemented
specifically for the language under consideration or the language needs
to be encoded in a generic format that the generic algorithm works on.
Stratego is a language for program transformation that supports both
specific and generic views of data types.

A Stratego program defines a transformation on first-order ground terms.
Transformation rules define single transformation steps. Transformation
rules are combined into transformation *strategies* by means of
combinators that determine where and in what order rules are applied.
These combinators include: primitives for traversal to the direct
subterms of a node, allowing the definition of many kinds of full term
traversals; full control over recursion in traversals; patterns as
first-class citizens; generic term construction and deconstruction.

These features create a setting in which it is possible to combine
generic traversal with data type specific pattern matching, and
separating logic (transformation, pattern matching) from control
(traversal). This makes it possible to give language independent
descriptions of language processing operations that can be instantiated
to a specific language by providing the patterns of the relevant
constructs. These generic algorithms only touch relevant constructors
and do not need to know the entire datatype, making the algorithms
insensitive to changes in the abstract syntax that do not affect the
constructors relevant to the operation.

Stratego is currently implemented by compilation to C code. All
constructs of the language are implemented directly, i.e., the compiled
program is as large as the specification, in contrast to approaches that
rely on preprocessing or program generation which may have a scaling
problem when dealing with large languages.

The approach to generic programming in Stratego is illustrated by means
of several examples including free variable extraction, bound variable
renaming, substitution and syntactic unification.

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink} \| \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 14 May 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
