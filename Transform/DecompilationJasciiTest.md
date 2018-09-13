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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationJasciiTest?t=1536826459)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationJasciiTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationJasciiTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationJasciiTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationJasciiTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/Transform/DecompilationJasciiTest?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Transform/DecompilationJasciiTest?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Transform/DecompilationJasciiTest?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Transform/DecompilationJasciiTest?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Transform/DecompilationJasciiTest?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Transform/DecompilationJasciiTest?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationJasciiTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationJasciiTest?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationJasciiTest?template=oopsmore&param1=1.10&param2=1.10)
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
Decompilation Jascii Test {#decompilation-jascii-test .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#jAscii_Java_Decompiler_Simple_Te} jAscii Java Decompiler Simple Tests
=========================================================================

NOTE: Jascii seems to have gone out of business at the end of 2003.

I tested jAscii 1.0.20 from <http://www.jascii.com>.

::: {.twikiToc}
-   [jAscii Java Decompiler Simple
    Tests](DecompilationJasciiTest#jAscii_Java_Decompiler_Simple_Te)
    -   [Fibo](DecompilationJasciiTest#Fibo)
    -   [Casting](DecompilationJasciiTest#Casting)
    -   [Inner classes](DecompilationJasciiTest#Inner_classes)
    -   [Deuces Wild](DecompilationJasciiTest#Deuces_Wild)
    -   [Sable Test Program](DecompilationJasciiTest#Sable_Test_Program)
    -   [Optimised code](DecompilationJasciiTest#Optimised_code)
    -   [Simple control
        flow](DecompilationJasciiTest#Simple_control_flow)
    -   [Exceptions](DecompilationJasciiTest#Exceptions)
    -   [Life](DecompilationJasciiTest#Life)
    -   [Conclusion](DecompilationJasciiTest#Conclusion)
:::

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}.
Decompiled source from jAscii:

    //Decompiled by jAscii v1.0.20. Copyright 2001 D&C Software Solutions Inc.
    //jAscii home page: http://www.jascii.com
    //Decompiled from Fibo.class
    //Original Source File Name: Fibo.java
    import java.io.PrintStream;

    class Fibo
    {
        Fibo()
        {
        }
        private static int fib(int i)
        {
            if (i > 1)
            {
                return fib(i - 1) + fib(i - 2);
            }
            else
            {
                return i;
            }
        }
        public static void main(String as[])
            throws Exception
        {
            int i = 0;
            try
            {
                i = Integer.parseInt(as[0]);
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

As you can see, the decompilation is almost identical to the original
source. The output compiled and ran perfectly with no changes required.

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingTestSource](DecompilerCastingTestSource){.twikiLink}.
Here is the output from jAscii:

    //Decompiled by jAscii v1.0.20. Copyright 2001 D&C Software Solutions Inc.
    import java.io.PrintStream;

    public class Casting
    {
        public Casting()
        {
        }
        public static void main(String as[])
        {
            for (char ch = '\0'; ch < 128; ch = (char)(ch + 1))
                System.out.println("ascii " + ch + " character " + ch);
        }
    } 

As before, there is a cast missing. No modifications were needed to
recompile it; when the cast was inserted, the program ran correctly.

[]{#Inner_classes} Inner classes
--------------------------------

For source, see
[DecompilerInnerClassesTestSource](DecompilerInnerClassesTestSource){.twikiLink}.
When decompiled with jAscii, the result is

    //Decompiled by jAscii v1.0.20. Copyright 2001 D&C Software Solutions Inc.
    import java.io.PrintStream;
    public class Usa
    {
        public String name;
        public class England
        {
            public String name;
            public class Ireland
            {
                public String name;
                public Ireland()
                {
                    name = "Dublin";
                }
                public void print_names()
                {
                    System.out.println(name);
                }
            }
            public England()
            {
                name = "London";
            }
        }
        public Usa()
        {
            name = "Detroit";
        }
    }

It reproduced the inner classes correctly, although the initialisations
were moved to the constructors.

[]{#Deuces_Wild} Deuces Wild
----------------------------

This is a 38K applet with two dimensional arrays of integers, some
floating point code, and so on. It decompiled in about 8 seconds, with
one error. In one `for` loop, a pair of braces was missing. The body of
the loop had only one statement (a do while loop) and a declaration;
perhaps the declaration was added after the loop was designated as not
needing braces. When the braces were added, it recompiled and ran
perfectly with no modifications. The arrays of strings are initialised
fairly naturally, e.g.

    String[] cardrank;
    ...
    cardrank = { "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine",
    "Ten", "Jack", "Queen", "King", "Ace" };

The initialisation was placed into the constructor method. It would have
been nice to break the long strings onto several lines of less than 80
columns.

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source, see
[DecompilerSableTestSource](DecompilerSableTestSource){.twikiLink}. Here
is the result for function `f` (as produced by jAscii):

        public static void f(short st)
        {
            Object object;
            boolean flag;
            if (st > 10)
            {
                Rectangle rectangle = new Rectangle(st, st);
                flag = rectangle.isFat();
                object = rectangle;
            }
            else
            {
                Circle circle = new Circle(st);
                flag = circle.isFat();
                object = circle;
            }
            if (!flag)
            {
                ((Drawable)(object)).draw();
            }
        }

As you can see, it took the lazy option and declared the variable
originally called `d` to be of type `Object`, and correctly cast the
object as required. However, it neglected to cast 11 from int to short
in the call to `f()`.

[]{#Optimised_code} Optimised code
----------------------------------

For source, see
[DecompilerOptimisedTestSource](DecompilerOptimisedTestSource){.twikiLink}.
This was the result from jAscii for the method `f`:

        public static void f(short st)
        {
            Object object;
            if (st > 10)
            {
                Rectangle rectangle = new Rectangle;
                rectangle.<init>(st, st);
                st = rectangle.isFat();
                object = rectangle;
            }
            else
            {
                object = new Circle;
                ((Circle)(object)).<init>(st);
                st = ((Circle)(object)).isFat();
                object = object;
            }
            if (st == 0)
            {
                ((Drawable)(object)).draw();
            }
        }

As you can see, it is confused with the two constructors.

When the above problems were corrected (e.g.
`Rectangle rectangle = new Rectangle(st, st)`, there is still the
problem of the boolean and the short sharing the same variable. When a
boolean was declared, and another cast added (not shown above), the code
finally compiled.

[]{#Simple_control_flow} Simple control flow
--------------------------------------------

For source, see
[DecompilerControlFlowTestSource](DecompilerControlFlowTestSource){.twikiLink}.
jAscii produces:

        public int foo(int i, int j)
        {
            RuntimeException e;
            pop e
            for (i = 10; i < j; i = j++ / i);
            return j;
        }

This result is strangely similar to that of SourceTec, and is completely
wrong. For example, `i` should only be set to 10 if an exception occurs.
Also obviously, `pop` is not valid Java.

[]{#Exceptions} Exceptions
--------------------------

For source, see
[DecompilerExceptionTestSource](DecompilerExceptionTestSource){.twikiLink}.
Here is jAscii\'s output:

        public void foo()
        {
            System.out.println("a");
            System.out.println("b");
            System.out.println("c");
            pop this
            System.out.println("g");
            System.out.println("d");
            pop this
            System.out.println("e");
            System.out.println("f");
            return;
        }

jAscii has given up on the exception handling altogether. The output is
obviously not correct, and will not compile.

[]{#Life} Life
--------------

This version of Conway\'s Game of Life was compiled from Ada 95 source
code. The applet is from
<http://www.appletmagic.com/download/demo/LifeRect.html>. With both
classes that I tried to decompile (`LifeRect` and `LR_Colony`), jAscii
complained that it was not able to complete its flow analysis, and
emitted bytecodes (e.g. `pop`, `expression`) into the output (so it did
not recompile). It did not bomb out during decompilation.

[]{#Conclusion} Conclusion
--------------------------

jAscii does not behave significantly better than some of the free
decompilers. In fact, its behaviour is similar to that of the SourceTec
decompiler, which is derived from the original Java decompiler, Mocha
(except that jAscii handles Java 2 classfiles, and inner classes).

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 10 Feb 2003

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
