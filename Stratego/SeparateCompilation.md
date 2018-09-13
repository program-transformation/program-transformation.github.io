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
    Page](http://www.program-transformation.org/edit/Stratego/SeparateCompilation?t=1536825667)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SeparateCompilation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SeparateCompilation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SeparateCompilation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SeparateCompilation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/SeparateCompilation?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/SeparateCompilation?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/SeparateCompilation?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/SeparateCompilation?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/SeparateCompilation?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/SeparateCompilation?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SeparateCompilation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SeparateCompilation?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/SeparateCompilation?template=oopsmore&param1=1.4&param2=1.4)
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
Separate Compilation {#separate-compilation .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A pragmatic approach to separate compilation has been introduced in
[StrategoRelease094](StrategoRelease094){.twikiLink}. A module can be
compiled *as a library* which results in a single C program containing
all definitions of that module and imported modules together with a
Stratego module providing the \'signatures\' of the strategies in the
library. Programs can then import the external definitions instead of
the implementation. Concerning the problem of extending definitions (see
below): it is illegal to extend external definitions. Thus, strategies
imported from a library cannot be extended, which is usually what is
desired anyway.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 24 Dec 2003

------------------------------------------------------------------------

The expected advantage of separate compilation is increased compilation
speed. This is especially desirable for the [Stratego standard
library[^?^](http://www.program-transformation.org/edit/Stratego/StrategoStandardLibrary?topicparent=Stratego.SeparateCompilation)]{.twikiNewLink
style="background : #FFFFCE;"}, which now gets compiled over and over
again for every application.

The fundamental problem for a separate compilation scheme is the
extensibility of strategy definitions and rules. This can be solved by
introducing a notion of a final module, which forbids extension of
definitions by importing modules.

A disadvantage is that it is no longer possible to do global
optimizations, or that information should still be exported from
modules.

### []{#Pragmatics} Pragmatics

A make-like system is needed for finding out whether a compiled module
is up to date. This requires dependency analysis and version comparisons
between source and compiled objects. The compilation of individual
modules can also be delegated to the user, as it is in the case of C
programs, but that is not good for usability of the compiler.

When packing collections of modules into (object) libraries, the import
system should avoid importing modules twice. This can be solved by first
computing the entire import graph before doing any actual imports.

### []{#Non_Problems} Non Problems

The following problems have been solved in the new
[ImplementationScheme](ImplementationScheme){.twikiLink} that was
introduced in [StrategoRelease06](StrategoRelease06){.twikiLink}:

-   requires procedure call implementation

<!-- -->

-   calling convention for procedures (also needed for
    [ForeignFunctions[^?^](http://www.program-transformation.org/edit/Stratego/ForeignFunctions?topicparent=Stratego.SeparateCompilation)]{.twikiNewLink
    style="background : #FFFFCE;"})

<!-- -->

-   dealing with variable scope

### []{#Related_issues_and_ideas} Related issues and ideas

-   [FinalDefinitions](FinalDefinitions){.twikiLink}
-   Header files at Stratego level
-   Encapsulation / hiding
-   Stratego badly needs a module system that is not susceptible to
    namespace pollution.
-   Namespaces in Stratego + private strategies.
-   Separate compilation and loadable modules.
-   Allow for overriding of rule/strategy

------------------------------------------------------------------------

[ToDo](ToDo){.twikiLink} \|
[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.SeparateCompilation)]{.twikiNewLink
style="background : #FFFFCE;"} \|
[CompilerImprovements](CompilerImprovements){.twikiLink} \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Dec 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.SeparateCompilation moved from Stratego.SeparateSompilation on
09 Dec 2001 - 12:40 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Stratego/SeparateCompilation?newweb=Stratego&newtopic=SeparateSompilation&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
