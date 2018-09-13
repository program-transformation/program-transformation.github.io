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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoProfile?t=1536825678)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoProfile)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoProfile)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoProfile?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoProfile?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoProfile?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoProfile?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoProfile?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoProfile)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoProfile?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoProfile?template=oopsmore&param1=1.2&param2=1.2)
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
Stratego Profile {#stratego-profile .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Although the traversal strategy that is used can have great impact on
the performance of Stratego programs, there is no mechanism (except for
time measurements) to compare the use of different strategies.
Additional statistics, like statistics about the number of rewrites for
instance, would be of great help.

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} &
[JoostVisser](../Main/JoostVisser){.twikiLink} in Proceedings of the
[SecondStrategoUsersDay](SecondStrategoUsersDay){.twikiLink}

With the new [ImplementationScheme](ImplementationScheme){.twikiLink}
introduced in [StrategoRelease06](StrategoRelease06){.twikiLink} it has
become interesting to use the standard C profiling tools. Since each
strategy operator is mapped onto a C function (modulo inlining) the
profiles give quite accurate information on where a program spends its
time. For this purpose compile your Stratego program with the extra
command-line options

       sc -i file -CL -g -CI -g

Of course it might still be interesting to have profiles with knowledge
about strategies.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 16 Jan 2002

------------------------------------------------------------------------

[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.StrategoProfile)]{.twikiNewLink
style="background : #FFFFCE;"} \| [ToDo](ToDo){.twikiLink} \|
[CompilerImprovements](CompilerImprovements){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
