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
    Page](http://www.program-transformation.org/edit/Stratego/DeadVariableElimination?t=1536825574)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/DeadVariableElimination)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/DeadVariableElimination)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/DeadVariableElimination?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/DeadVariableElimination?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/DeadVariableElimination?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/DeadVariableElimination)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/DeadVariableElimination?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/DeadVariableElimination?template=oopsmore&param1=1.1&param2=1.1)
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
Dead Variable Elimination {#dead-variable-elimination .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The `dead-var-elim` component of the [Stratego
optimizer](StrategoOptimizer){.twikiLink} eliminates variables from a
strategy expression if they are not used in a build. For example, in the
expression

      { x, y, z :
        ?F(x, y)
        ; !y
        ; ?G(z)
        ; !H(z, z)
      }

the variable `z` is used in the final build (not dead), and `y` is used
in the build needed for the match with `G` (not dead). However, `x` is
dead since it does not contribute to the final result. Dead variable
elimination removes dead variables by

-   eliminating them from the scope, and
-   replacing occurrences in matches with a wildcard

Thus, the example reduces to

      { y, z :
        ?F(_, y)
        ; !y
        ; ?G(z)
        ; !H(z, z)
      }

Variable only matches (`?x`) with dead variables are turned into
wildcard matches (`?_`) and can be cleaned up by a subsequent
simplification.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Aug 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
