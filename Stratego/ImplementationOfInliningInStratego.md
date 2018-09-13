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
    Page](http://www.program-transformation.org/edit/Stratego/ImplementationOfInliningInStratego?t=1536825428)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ImplementationOfInliningInStratego)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ImplementationOfInliningInStratego)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ImplementationOfInliningInStratego?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ImplementationOfInliningInStratego?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ImplementationOfInliningInStratego?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ImplementationOfInliningInStratego)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ImplementationOfInliningInStratego?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/ImplementationOfInliningInStratego?template=oopsmore&param1=1.1&param2=1.1)
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
Implementation Of Inlining In Stratego {#implementation-of-inlining-in-stratego .twikiTopicTitle}
======================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

by [ArneDeBruijn](../Transform/ArneDeBruijn){.twikiLink}

August 10, 2001 INF/SCR-01-11 Master thesis, Institute of Information
and Computing Sciences, Universiteit Utrecht

**Abstract**

All modern compilers provide inlining, an optimization which replaces a
func- tion call by the function body. Implementations of inlining are
usually focused on speci¯c source languages or on speci¯c algorithms to
decide which functions should be inlined. We describe the implementation
of a general inlining im- plementation in the program transformation
language Stratego. This inliner should be usable for di®erent source
languages and decision algorithms. The implementation separates the
analysis and transformation of the program, the traversal of the program
and the decision when to do inlining. In addition, the implementation of
several other optimizations that are enabled by inlining is discussed in
the context of the highly optimizable Pan language.

**Available**

-   <http://www.cs.uu.nl/people/visser/ftp/Bru01.pdf>

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
