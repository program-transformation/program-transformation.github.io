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
    Page](http://www.program-transformation.org/edit/Stratego/ErrorReporting?t=1536825578)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ErrorReporting)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ErrorReporting)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ErrorReporting?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ErrorReporting?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ErrorReporting?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ErrorReporting?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ErrorReporting?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ErrorReporting)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ErrorReporting?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/ErrorReporting?template=oopsmore&param1=1.2&param2=1.2)
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
Error Reporting {#error-reporting .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Ideas for improving the error reporting of the
[StrategoCompiler](StrategoCompiler){.twikiLink}. Feel free to add more
ideas.

-   check import graph: operators used in a module should be visible
    through its imports

<!-- -->

-   Warn in case of overloaded rule or strategy names (optionally)

<!-- -->

-   store line numbers of rules and definitions and use in error
    messages

<!-- -->

-   list origin when reporting \"error: operator s1/0 undefined\"
    -   could be done by first making a list/table of all available
        definitions and checking it after computing the calls from a
        rule or definition

<!-- -->

-   dealing with shared libraries; Merijn writes:

<!-- -->

-   -   doe configure \--disable-shared (de allerlaatste versie van
        aterm doet dat automatisch al). Hiermee wordt de generatie van
        shared libraries voorkomen
    -   of, link sc met de -static optie om geen gebruik te aken van
        shared libraries
    -   of, laat LD\_LIBRARY\_PATH wijzen naar /lib. Hierdoor kan de
        dynamic linker de shared libraries vinden.

<!-- -->

-   sc : commandline interface \* - -c flag for sc: only compile to C
    code \* - document the interface in tutorial and manual page (?)

<!-- -->

-   silent rewriting mode: no success or failure message or profiling
    information

<!-- -->

-   infallible rules that give runtime errors with linenumbers if they
    do fail

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Dec 2001\

Short of a type system for Stratego, and an accompanying type-checker,
many additional static checks would be helpful to the programmer. For
instance, mistakes in arities of strategies and strategy variables could
be caught and reported as such by the compiler, instead of leading to C
compilation or linking errors.

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} &
[JoostVisser](../Main/JoostVisser){.twikiLink} in Proceedings of
[SecondStrategoUsersDay](SecondStrategoUsersDay){.twikiLink}

------------------------------------------------------------------------

[ToDo](ToDo){.twikiLink} \|
[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.ErrorReporting)]{.twikiNewLink
style="background : #FFFFCE;"} \|
[CompilerImprovements](CompilerImprovements){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
