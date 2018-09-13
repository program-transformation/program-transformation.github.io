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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerExceptionTestSource?t=1536826464)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerExceptionTestSource)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerExceptionTestSource)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerExceptionTestSource?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerExceptionTestSource?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilerExceptionTestSource?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilerExceptionTestSource?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilerExceptionTestSource?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilerExceptionTestSource?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompilerExceptionTestSource?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerExceptionTestSource)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerExceptionTestSource?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerExceptionTestSource?template=oopsmore&param1=1.3&param2=1.3)
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
Decompiler Exception Test Source {#decompiler-exception-test-source .twikiTopicTitle}
================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This is the Jasmin (essentially Java \"assembly language\") source code
for the exceptions decompiler test. It is an attempt at the test program
from Figure 6 of the paper [Decompiling Java Bytecode: Problems, Traps
and Pitfalls](http://www.sable.mcgill.ca/publications/papers/#cc2002-2),
but since the results are so different to theirs, I must have failed to
reproduce their original example. I should be pretty close, though,
because the SourceTec decompiler produces results very similar to what
their paper claims Wingdis produces. The control flow for this program
is as follows:

![PitfallsFigure6.gif](../pub/Transform/DecompilerExceptionTestSource/PitfallsFigure6.gif){width="247"
height="341"}

The solid lines represent normal control flow, and the labelled dotted
lines represent execeptional control flow. The trick with this test is
that the two areas of protection overlap (one area, for exception
`RuntimeException`, covers blocks `b` and `c`, and the other area, for
exception `Exception`, covers blocks `c` and `d`). The correct way to
express this in Java is to split the two areas into three; one with
block `b` alone, one with block `c` alone (which requires two `catch`
statements), and one for block `d` alone.

I wrote this program as follows. First, I wrote a Java program that
comes close to the control flow required. I compiled this to bytecodes,
and used Soot (see <http://www.sable.mcgill.ca/soot/>) to convert this
to Jasmin. I then edited the Jasmin to have the control flow required,
and edited the labels to be more readable. I then \"assembled\" this
code with jasmin (a slightly modified version comes as part of Soot).

    .class  foo
    .super java/lang/Object

    .method  <init>()V
        .limit stack 1
        .limit locals 1
        aload_0
        invokespecial java/lang/Object/<init>()V
        return
    .end method

    .method public foo()V
    .catch java/lang/RuntimeException from label_b to after_c using catch_g
    .catch java/lang/RuntimeException from label_c to after_d using catch_e
        .limit stack 2
        .limit locals 1
        getstatic java/lang/System/out Ljava/io/PrintStream;
        ldc "a"
        invokevirtual java/io/PrintStream/println(Ljava/lang/String;)V
    label_b:
        getstatic java/lang/System/out Ljava/io/PrintStream;
        ldc "b"
        invokevirtual java/io/PrintStream/println(Ljava/lang/String;)V
    label_c:
        getstatic java/lang/System/out Ljava/io/PrintStream;
        ldc "c"
        invokevirtual java/io/PrintStream/println(Ljava/lang/String;)V
    after_c:
        goto label_d
    catch_g:
        astore_0
        getstatic java/lang/System/out Ljava/io/PrintStream;
        ldc "g"
        invokevirtual java/io/PrintStream/println(Ljava/lang/String;)V
        goto label_f
    label_d:
        getstatic java/lang/System/out Ljava/io/PrintStream;
        ldc "d"
        invokevirtual java/io/PrintStream/println(Ljava/lang/String;)V
    after_d:
        goto label_f
    catch_e:
        astore_0
        getstatic java/lang/System/out Ljava/io/PrintStream;
        ldc "e"
        invokevirtual java/io/PrintStream/println(Ljava/lang/String;)V
    label_f:
        getstatic java/lang/System/out Ljava/io/PrintStream;
        ldc "f"
        invokevirtual java/io/PrintStream/println(Ljava/lang/String;)V
        return
    .end method

    .method public static main()V
        .limit stack 2
        .limit locals 1
        new foo
        dup
        invokespecial foo/<init>()V
        astore_0
        return
    .end method

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 12 Feb 2003

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
