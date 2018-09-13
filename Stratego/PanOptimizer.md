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
    Page](http://www.program-transformation.org/edit/Stratego/PanOptimizer?t=1536825467)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PanOptimizer)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PanOptimizer)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PanOptimizer?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PanOptimizer?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/PanOptimizer?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/PanOptimizer?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/PanOptimizer?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PanOptimizer)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PanOptimizer?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/PanOptimizer?template=oopsmore&param1=1.2&param2=1.2)
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
Pan Optimizer {#pan-optimizer .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

An optimizer for the [PanLanguage](../Transform/PanLanguage){.twikiLink}
was implemented in Stratego as part of a research on
[InliningStrategies](../Transform/InliningStrategies){.twikiLink}. It
performs the following optimizations:

-   [FunctionInlining[^?^](http://www.program-transformation.org/edit/Transform/FunctionInlining?topicparent=Stratego.PanOptimizer)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ConstantFolding[^?^](http://www.program-transformation.org/edit/Transform/ConstantFolding?topicparent=Stratego.PanOptimizer)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [CommonSubexpressionElimination[^?^](http://www.program-transformation.org/edit/Transform/CommonSubexpressionElimination?topicparent=Stratego.PanOptimizer)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [CodeMotion[^?^](http://www.program-transformation.org/edit/Transform/CodeMotion?topicparent=Stratego.PanOptimizer)]{.twikiNewLink
    style="background : #FFFFCE;"}

The optimizer uses the frontend from the compiler for the
[TigerLanguage[^?^](http://www.program-transformation.org/edit/Hpc/TigerLanguage?topicparent=Stratego.PanOptimizer)]{.twikiNewLink
style="background : #FFFFCE;"}, which means Pan programs must be written
in Tiger.

A master thesis which discusses this implementation is available. It has
the following abstract.

All modern compilers provide inlining, an optimization which replaces a
function call by the function body. Implementations of inlining are
usually focused on specific algorithms to decide which functions should
be inlined or specific source languages. This report instead describes
the implementation of a general inlining implementation in the program
transformation language Stratego. This inliner should be usable for
different source languages and decision algorithms. The implementation
separates the analysis and transformation of the program, the traversal
of the program and the decision when to do inlining. In addition, the
implementation of several other optimizations that are enabled by
inlining is discussed in the context of the highly optimizable Pan
language.\
[]{#TopicEnd}
:::

::: {.twikiAttachments}
  [I](PanOptimizer@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Attachment](../TWiki/FileAttachment){.twikiLink} [![sort](../pub/TWiki/TablePlugin/diamond.gif)](PanOptimizer@sortcol=1&table=1&up=0#sorted_table "Sort by this column")   [Action](PanOptimizer@sortcol=2&table=1&up=0#sorted_table "Sort by this column")                                                                                                [Size](PanOptimizer@sortcol=3&table=1&up=0#sorted_table "Sort by this column") [Date](PanOptimizer@sortcol=4&table=1&up=0#sorted_table "Sort by this column")   [Who](PanOptimizer@sortcol=5&table=1&up=0#sorted_table "Sort by this column")   [Comment](PanOptimizer@sortcol=6&table=1&up=0#sorted_table "Sort by this column")
  ----------------------------------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------- -------------------------------------------------------------------------------- ------------------------------------------------------------------------------- -----------------------------------------------------------------------------------
  ![](../pub/icn/else.gif){width="16" height="16"}                              [doc.ps.gz](http://www.program-transformation.org/pub/Stratego/PanOptimizer/doc.ps.gz)                                                                                      [manage](http://www.program-transformation.org/attach/Stratego/PanOptimizer?filename=doc.ps.gz&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                        392.7 K 13 Jul 2001 - 13:23                                                              [ArneDeBruijn](../Main/ArneDeBruijn){.twikiLink}                                Thesis on Pan optimizer
  ![](../pub/icn/else.gif){width="16" height="16"}                              [pan-tiger-0.15.tar.gz](http://www.program-transformation.org/pub/Stratego/PanOptimizer/pan-tiger-0.15.tar.gz)                                                              [manage](http://www.program-transformation.org/attach/Stratego/PanOptimizer?filename=pan-tiger-0.15.tar.gz&revInfo=1 "change, update, previous revisions, move, delete...")                                                                            126.2 K 13 Jul 2001 - 13:26                                                              [ArneDeBruijn](../Main/ArneDeBruijn){.twikiLink}                                Pan Tiger 0.15
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
