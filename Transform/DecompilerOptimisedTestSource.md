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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerOptimisedTestSource?t=1536826466)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerOptimisedTestSource)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerOptimisedTestSource)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerOptimisedTestSource?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerOptimisedTestSource?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilerOptimisedTestSource?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilerOptimisedTestSource?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilerOptimisedTestSource?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilerOptimisedTestSource?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompilerOptimisedTestSource?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerOptimisedTestSource)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerOptimisedTestSource?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerOptimisedTestSource?template=oopsmore&param1=1.3&param2=1.3)
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
Decompiler Optimised Test Source {#decompiler-optimised-test-source .twikiTopicTitle}
================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This is the Jasmin (essentially Java \"assembly language\" source code
for the optimised bytecode decompiler tests. It was created with

    soot -s -O Main

where `soot` is a simple script containing

    java -cp .:paths:to:soot:and:jasmin soot.Main $@=

Soot is a Java bytecode manipulation tool from Sable University; see
<http://www.sable.mcgill.ca/soot/>

------------------------------------------------------------------------

    .method public static f(S)V
        .limit stack 3
        .limit locals 2
        iload_0
        bipush 10
        if_icmple label0
        new Rectangle
        astore_1
        aload_1
        iload_0
        iload_0
        invokespecial Rectangle/<init>(SS)V
        aload_1
        invokevirtual Rectangle/isFat()Z
        istore_0
        aload_1
        astore_1
        goto label1
    label0:
        new Circle
        astore_1
        aload_1
        iload_0
        invokespecial Circle/<init>(I)V
        aload_1
        invokevirtual Circle/isFat()Z
        istore_0
        aload_1
        astore_1
    label1:
        iload_0
        ifne label2
        aload_1
        invokeinterface Drawable/draw()V 1
    label2:
        return
    .end method

    .method public static main([Ljava/lang/String;)V
        .limit stack 1
        .limit locals 1
        bipush 11
        invokestatic Main/f(S)V
        return
    .end method

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 12 Feb 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
