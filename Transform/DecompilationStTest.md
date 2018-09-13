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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationStTest?t=1536826462)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationStTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationStTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationStTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationStTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/DecompilationStTest?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/DecompilationStTest?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/DecompilationStTest?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/DecompilationStTest?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/DecompilationStTest?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/DecompilationStTest?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationStTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationStTest?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationStTest?template=oopsmore&param1=1.7&param2=1.7)
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
Decompilation St Test {#decompilation-st-test .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#SourceTec_Java_Decompiler_Simple} SourceTec Java Decompiler Simple Tests
============================================================================

SourceTec, also known as Jasmine, is an old decompiler; in fact it\'s a
patch to Mocha, probably the very first Java decompiler. The version I
used is 1.10 (from the Readme file), though the decompiler output says
Version 1.0. It only works on Java 1.1 files; most Java programs are
Java 1.2 (Java 2) these days. I recompiled those tests that I could for
1.1 (using `-target 1.1`).

::: {.twikiToc}
-   [SourceTec Java Decompiler Simple
    Tests](DecompilationStTest#SourceTec_Java_Decompiler_Simple)
    -   [Fibo](DecompilationStTest#Fibo)
    -   [Casting](DecompilationStTest#Casting)
    -   [Inner classes](DecompilationStTest#Inner_classes)
    -   [Deuces Wild](DecompilationStTest#Deuces_Wild)
    -   [Sable Test Program](DecompilationStTest#Sable_Test_Program)
    -   [Optimised code.](DecompilationStTest#Optimised_code)
    -   [Simple control flow](DecompilationStTest#Simple_control_flow)
    -   [Exceptions](DecompilationStTest#Exceptions)
    -   [Life](DecompilationStTest#Life)
    -   [Conclusion](DecompilationStTest#Conclusion)
:::

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}.
Decompiled source from SourceTec:

    /* Decompiled by Jasmine from Fibo.class */
    /* Originally compiled from Fibo.java */

    import java.io.PrintStream;

    synchronized class Fibo
    {
        Fibo()
        {
        }
        private static int fib(int i)
        {
            if (i > 1)
                return fib(i - 1) + fib(i - 2);
            else
                return i;
        }
        public static void main(String astring[])
            throws Exception
        {
            int i = 0;
            try
            {
                i = Integer.parseInt(astring[0]);
            }
            catch (Exception e)
            {
                System.out.println("Input error");
                System.exit(1);
            }
            int j = fib(i);
            System.out.println("fibonacci(" + i + ") = " + j);
        }
    }

As you can see, the decompilation looks pretty good, but the
`synchronized` keyword is wrong and stops the output from recompiling.
(This would presumably not have happened with true Java 1.1 bytecode
files). When this word was removed, the output compiled and ran with no
further changes required.

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingTestSource](DecompilerCastingTestSource){.twikiLink}.
Here is the output from SourceTec:

    /* Decompiled by Jasmine from Casting.class */
    /* Originally compiled from Casting.java */

    import java.io.PrintStream;

    public synchronized class Casting
    {
        public Casting()
        {
        }

        public static void main(String astring[])
        {
            for (char ch = '\0'; ch < 128; ch = (char)(ch + 1))
                System.out.println("ascii " + ch + " character " + ch);
        }
    }

Again, the `synchronized` keyword had to be removed for it to recompile.
The cast is missing, so the program did not run correctly. With those
two changes (removed `synchronized`, added cast to integer), the program
was correct.

[]{#Inner_classes} Inner classes
--------------------------------

For source, see
[DecompilerInnerClassesTestSource](DecompilerInnerClassesTestSource){.twikiLink}.
When decompiled with SourceTec, the result is

    Ignoring class attribute InnerClasses
    10
    /* Decompiled by Jasmine from Usa.class */
    /* Originally compiled from Usa.java */

    public synchronized class Usa
    {
        public String name;

        public Usa()
        {
            name = "Detroit";
        }
    }

It does not understand inner classes. When I tried to decompile
`Usa$England.class`, the result was

    Ignoring field attribute Synthetic
    0
    Ignoring class attribute InnerClasses
    18
    /* Decompiled by Jasmine from Usa$England.class */
    /* Originally compiled from Usa.java */

    public synchronized class Usa$England
    {
        public String name;
        private final Usa this$0 = usa;

        public Usa$England(Usa usa)
        {
            name = "London";
        }
    }

[]{#Deuces_Wild} Deuces Wild
----------------------------

This is a 38K applet with two dimensional arrays of integers, some
floating point code, and so on. The SourceTec decompiler bombed out with
an array out of bounds exception.

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source, see
[DecompilerSableTestSource](DecompilerSableTestSource){.twikiLink}. Here
is the result for function `f` (as produced by SourceTec):

        public static void f(short s)
        {
            Object object;
            boolean flag;
            if (s > 10)
            {
                Rectangle rectangle = new Rectangle(s, s);
                flag = rectangle.isFat();
                object = rectangle;
            }
            else
            {
                Circle circle = new Circle(s);
                flag = circle.isFat();
                object = circle;
            }
            if (!flag)
                object.draw();
        }

It typed the variable, called `d` in the original source, as type
`Object`, and neglected to cast the variable in the call to `drawable`.
When the cast was added, `synchronized` was removed, and another cast
was added (not shown above), it compiled correctly.

[]{#Optimised_code}[]{#Optimised_code_} Optimised code.
-------------------------------------------------------

For source, see
[DecompilerOptimisedTestSource](DecompilerOptimisedTestSource){.twikiLink}.
This was the result from SourceTec for the method `f`:

        public static void f(short s)
        {
            Object object;
            if (s > 10)
            {
                Rectangle rectangle = new Rectangle;
                rectangle.<init>(s, s);
                s = rectangle.isFat();
                object = rectangle;
            }
            else
            {
                object = new Circle;
                object.<init>(s);
                s = object.isFat();
                object = object;
            }
            if (s == 0)
                object.draw();
        }

As you can see, it is confused with the two constructors, and the cast
for the call to `draw` is still missing. In addition, it is missing
another cast to `isFat` (in the `else` clause).

When the above problems were corrected (e.g.
`Rectangle rectangle = new Rectangle(i, i)`, there are still problems
because there is a boolean and a short sharing the same local variable
(`i` and `is_fat` in the original source, both `s` in the decompiled
output). In the end, quite a few changes were needed to allow the code
to compile.

It should be noted that in the [\"Decompiling Java Bytecode: Problems,
Traps and
Pitfalls\"](http://www.sable.mcgill.ca/publications/papers/#cc2002-2)
paper, they optimised the code differently; they report SourceTec (which
they label Jasmine) as emitting bytecodes (i.e. failed to decompile the
function at all).

[]{#Simple_control_flow} Simple control flow
--------------------------------------------

For source, see
[DecompilerControlFlowTestSource](DecompilerControlFlowTestSource){.twikiLink}.
Output from SourceTec was:

    Method foo: Flow analysis could not complete
        public int foo(int i, int j)
        {
            RuntimeException e;
            for (i = j++ / i; i < j; i = j++ / i) /* null body */ ;
            return j;
            pop e
            i = 10;
        }

The `try` and `catch` clauses are not generated, there is bytecode
(`pop`) in the output, and the result is generally quite wrong.

[]{#Exceptions} Exceptions
--------------------------

For source, see
[DecompilerExceptionTestSource](DecompilerExceptionTestSource){.twikiLink}.
Output from SourceTec was:

        public void foo()
        {
            System.out.println("a");
            try
            {
                System.out.println("b");
                try
                {
                    System.out.println("c");
                    System.out.println("d");
                }
                catch ()
                {
                    System.out.println("e");
                }
            }
            catch ()
            {
                System.out.println("g");
            }
            System.out.println("f");
        }

The exception variables are not declared, so the output will not even
compile. The exception path from `c` to `g` is missing.

[]{#Life} Life
--------------

This version of Conway\'s Game of Life was compiled from Ada 95 source
code. The top level class file is
<http://www.appletmagic.com/download/demo/LifeRect.html>. When
`LifeRect` was decompiled, it emitted these warnings:

    Method paint: Flow analysis could not complete
    Method run: Flow analysis could not complete

Similarly, 6 warnings were emitted for `LR_Colony`. These contained
bytecode-like code, such as:

            compare and if < goto 68
            dup 1 over 0
            expression 59

[]{#Conclusion} Conclusion
--------------------------

This decompiled is essentially obsolete. It performs adequately for
simple programs that happen to be in Java 1.1 format.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 11 Feb 2003

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
