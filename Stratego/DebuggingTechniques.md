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
    Page](http://www.program-transformation.org/edit/Stratego/DebuggingTechniques?t=1536825574)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/DebuggingTechniques)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/DebuggingTechniques)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/DebuggingTechniques?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/DebuggingTechniques?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Stratego/DebuggingTechniques?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/DebuggingTechniques?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/DebuggingTechniques?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/DebuggingTechniques?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/DebuggingTechniques?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/DebuggingTechniques?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/DebuggingTechniques)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/DebuggingTechniques?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Stratego/DebuggingTechniques?template=oopsmore&param1=1.6&param2=1.6)
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
Debugging Techniques {#debugging-techniques .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Here are some debugging techniques

-   Reduce the specification and the input to localize the error

### []{#Format_Checking} Format Checking

-   Use a [FormatChecker](FormatChecker){.twikiLink} to verify the
    results of transformations

### []{#Unit_Testing} Unit Testing

-   Write a unit test using
    [StrategoUnit[^?^](http://www.program-transformation.org/edit/Stratego/StrategoUnit?topicparent=Stratego.DebuggingTechniques)]{.twikiNewLink
    style="background : #FFFFCE;"}

### []{#Debug} Debug

-   Print intermediate results using `debug`

<!-- -->

-   Use the debug strategy **with an argument**. It turns out that the
    debug strategy will accept a string prefaced by an exclamation mark,
    thus: debug(!\"after doing something or other: \") If you do this,
    it will print the current aterm as usual, but first it will print
    the string, so that you know where in the program it is.

### []{#Tracing} Tracing

-   Use the tracing facilities of the
    [StrategoCompiler](StrategoCompiler){.twikiLink}; See
    [StrategoDebug](StrategoDebug){.twikiLink}

### []{#Pitfalls} Pitfalls

-   Compare your code with the list of [PitFalls](PitFalls){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
