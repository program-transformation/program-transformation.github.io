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
    Page](http://www.program-transformation.org/edit/Stratego/UnbindVariablesOnBacktracking?t=1536825716)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/UnbindVariablesOnBacktracking)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/UnbindVariablesOnBacktracking)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/UnbindVariablesOnBacktracking?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/UnbindVariablesOnBacktracking?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/UnbindVariablesOnBacktracking?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/UnbindVariablesOnBacktracking?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/UnbindVariablesOnBacktracking?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/UnbindVariablesOnBacktracking)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/UnbindVariablesOnBacktracking?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/UnbindVariablesOnBacktracking?template=oopsmore&param1=1.2&param2=1.2)
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
Unbind Variables On Backtracking {#unbind-variables-on-backtracking .twikiTopicTitle}
================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

After a strategy fails, variables that have been bound in matches should
be unbound. This is not supported by the current compilation scheme. The
following example illustrates the problem. The strategy `f` should
behave the same as the choice between `g` and `h`.

    module unbind-on-backtrack 
    strategies  
      f = (?(x, y); ?(x, x) <+ ?(y, x)); ![y,x]  

      g = ?(x, y); ?(x, x); ![y,x] 
     
      h = ?(y, x); ![y,x]  

      main = 
        <g <+ h> ("a", "b") => ["a", "b"]
      ; <f> ("a", "b") => ["a", "b"]               

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 22 Nov 2001\

One way: only bind unbound variables when choice is committed: Consider

      ?F(x, y); s1 <+ s2

and assume that x is bound before invocation of this strategy and that y
is not (y value is looked for). transform this into

      {y: ?F(x, y); s1; split(id,!y)}; ?(_,y); Fst <+ s2

This has the same effect as the earlier expression (can this insight be
made more efficient? turned into primitive operations?)

Note: this assume one can determine statically which variables are
unbound when entering a choice. Although this scheme works when y is
bound, it might turn out very expensive, because a failing match to y is
discovered after doing s1.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 2000

Solution: Save (the status of) all variables that are bound in the left
branch of a choice and restore after failure. Shouldn\'t be too
difficult.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 22 Nov 2001\

------------------------------------------------------------------------

[CategoryBugs[^?^](http://www.program-transformation.org/edit/Stratego/CategoryBugs?topicparent=Stratego.UnbindVariablesOnBacktracking)]{.twikiNewLink
style="background : #FFFFCE;"}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
