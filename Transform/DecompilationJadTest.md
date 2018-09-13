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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationJadTest?t=1536826459)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationJadTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationJadTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationJadTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationJadTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    14](http://www.program-transformation.org/view/Transform/DecompilationJadTest?rev=1.14)
    [(diff 13)](http://www.program-transformation.org/rdiff/Transform/DecompilationJadTest?rev1=1.14&rev2=1.13)
-   [Rev
    13](http://www.program-transformation.org/view/Transform/DecompilationJadTest?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Transform/DecompilationJadTest?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Transform/DecompilationJadTest?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Transform/DecompilationJadTest?rev1=1.12&rev2=1.11)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationJadTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationJadTest?template=oopsmore&param1=1.14&param2=1.14)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationJadTest?template=oopsmore&param1=1.14&param2=1.14)
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
Decompilation Jad Test {#decompilation-jad-test .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Jad_Java_Decompiler_Simple_Tests} Jad Java Decompiler Simple Tests
======================================================================

::: {.twikiToc}
-   [Jad Java Decompiler Simple
    Tests](DecompilationJadTest#Jad_Java_Decompiler_Simple_Tests)
    -   [Fibo](DecompilationJadTest#Fibo)
    -   [Casting](DecompilationJadTest#Casting)
    -   [Inner classes](DecompilationJadTest#Inner_classes)
    -   [Deuces Wild](DecompilationJadTest#Deuces_Wild)
    -   [Sable Test Program](DecompilationJadTest#Sable_Test_Program)
    -   [Optimised code](DecompilationJadTest#Optimised_code)
    -   [Simple control flow](DecompilationJadTest#Simple_control_flow)
    -   [Exceptions](DecompilationJadTest#Exceptions)
    -   [Life](DecompilationJadTest#Life)
    -   [Conclusion](DecompilationJadTest#Conclusion)
:::

This page performs some tests on JAD version 1.5.8e. Output has been
trimmed slightly for ease of comparison to the original source.

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}.
Decompiled output from Jad:

    // Decompiled by Jad v1.5.8e. Copyright 2001 Pavel Kouznetsov.
    import java.io.PrintStream;

    class Fibo
    {
        Fibo()
        {
        }

        private static int fib(int i)
        {
            if(i > 1)
                return fib(i - 1) + fib(i - 2);
            else
                return i;
        }

        public static void main(String args[])
            throws Exception
        {
            int i = 0;
            try
            {
                i = Integer.parseInt(args[0]);
            }
            catch(Exception exception)
            {
                System.out.println("Input error");
                System.exit(1);
            }
            int j = fib(i);
            System.out.println("fibonacci(" + i + ") = " + j);
        }
    }

As you can see, the decompilation is almost identical to the source.

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingTestSource](DecompilerCastingTestSource){.twikiLink}.
Here is the output from Jad:

    // Decompiled by Jad v1.5.8e. Copyright 2001 Pavel Kouznetsov.
    import java.io.PrintStream;
    public class Casting
    {
        public Casting()
        {
        }

        public static void main(String args[])
        {
            for(char c = '\0'; c < 128; c++)
                System.out.println("ascii " + (int)c + " character " + c);
        }
    }

As you can see, it\'s readable, similar to the original, and is correct.
No modifications were needed to recompile it.

[]{#Inner_classes} Inner classes
--------------------------------

For source, see
[DecompilerInnerClassesTestSource](DecompilerInnerClassesTestSource){.twikiLink}.
When decompiled with Jad, the result is

    // Decompiled by Jad v1.5.8e. Copyright 2001 Pavel Kouznetsov.
    import java.io.PrintStream;
    public class Usa
    {
        public class England
        {
            public class Ireland
            {
                public void print_names()
                {
                    System.out.println(name);
                }
                public String name;
                public Ireland()
                {
                    name = "Dublin";
                }
            }
            public String name;
            public England()
            {
                name = "London";
            }
        }
        public Usa()
        {
            name = "Detroit";
        }
        public String name;
    }

I\'m no inner classes expert, but this looks right to me, even though it
looks different to the original source code.

[]{#Deuces_Wild} Deuces Wild
----------------------------

This is a 38K applet with two dimensional arrays of integers, some
floating point code, and so on. It decompiled in about 0.8 seconds, with
no errors, and recompiled and ran perfectly with no modifications. The
data members appear at the end of the class definition, which I find a
little irritating. The arrays of strings are initialised fairly
naturally, e.g.

        String cardrank[] = {
            "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine",
    "Ten", "Jack",
            "Queen", "King", "Ace"
        };
        String cardsuit[] = {
            "clubs", "diamonds", "hearts", "spades"
        };

However, the string before this one also had ten strings on one line,
producing a line that had well over a hundred columns. This is a very
minor issue.

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source, see
[DecompilerSableTestSource](DecompilerSableTestSource){.twikiLink}. Here
is the result for function `f` (as produced by Jad):

        public static void f(short word0)
        {
            Object obj;
            boolean flag;
            if(word0 > 10)
            {
                Rectangle rectangle = new Rectangle(word0, word0);
                flag = rectangle.isFat();
                obj = rectangle;
            } else
            {
                Circle circle = new Circle(word0);
                flag = circle.isFat();
                obj = circle;
            }
            if(!flag)
                ((Drawable) (obj)).draw();
        }

It decided to type the reference that was `d` in the original source as
type `Object` (name `obj` ). This is not ideal, since it requires a cast
when used. The cast was at least correctly inserted. Other decompilers
such as Jode and Dava can correctly type the \" `d` \" variable as type
`Drawable` . It produced correct code which compiled without
modification.

[]{#Optimised_code} Optimised code
----------------------------------

For source, see
[DecompilerOptimisedTestSource](DecompilerOptimisedTestSource){.twikiLink}.
This was the result from Jad for the method `f` :

        public static void f(short word0)
        {
            Object obj;
            if(word0 > 10)
            {
                obj = JVM INSTR new #37  <Class Rectangle>;
                ((Rectangle) (obj)).Rectangle(word0, word0);
                word0 = ((Rectangle) (obj)).isFat();
                obj = obj;
            } else
            {
                obj = JVM INSTR new #15  <Class Circle>;
                ((Circle) (obj)).Circle(word0);
                word0 = ((Circle) (obj)).isFat();
                obj = obj;
            }
            if(word0 == 0)
                ((Drawable) (obj)).draw();
        }

As you can see, it is confused with the two constructors. The fix is
moderately obvious; there is no chance that the error will slip by the
java compiler, at least.

[]{#Simple_control_flow} Simple control flow
--------------------------------------------

For source, see
[DecompilerControlFlowTestSource](DecompilerControlFlowTestSource){.twikiLink}.
Jad produces:

        public int foo(int i, int j)
        {
            while(true)
                try
                {
                    while(i < j)
                        i = j++ / i;
                    break MISSING_BLOCK_LABEL_28;
                }
                catch(RuntimeException runtimeexception)
                {
                    i = 10;
                }
            return j;
        }

This result does not compile, and is missing several statements.

[]{#Exceptions} Exceptions
--------------------------

For source, see
[DecompilerExceptionTestSource](DecompilerExceptionTestSource){.twikiLink}.
Here is Jad\'s output:

        public void foo()
        {
            System.out.println("a");
            System.out.println("b");
            System.out.println("c");
            break MISSING_BLOCK_LABEL_39;
            this;
            System.out.println("g");
            break MISSING_BLOCK_LABEL_59;
            System.out.println("d");
            break MISSING_BLOCK_LABEL_59;
            this;
            System.out.println("e");
            System.out.println("f");
            return;
        }

JAD has completely given up on any exception handling. Interestingly, in
the paper mentioned above, Jad is reported as having one `try` and
`catch` clause. Obviously, this output is nowhere near correct, and will
not even compile.

[]{#Life} Life
--------------

This applet is originally compiled in Ada 95. The applet is at
<http://www.appletmagic.com/download/demo/LifeRect.html>. When Jad was
run on this file, it admitted that it could not completely decompile
method `run`. It failed this relatively easy control flow code:

            if(false) goto _L2; else goto _L1
    _L1:
            int I = 1;
    _L3:
            double d;
            ...
            I++;
            if(I > 180) goto _L2; else goto _L3
    _L2:

which Jode correctly decompiled as follows:

        if (true) {
            int I = 1;
            do {
            double d = ...
            I++;
            } while (I <= 180);
        }

Granted, the `if (true)` is strange, but should not throw a decompiler.
Similar problems occured with other classes of this applet.

[]{#Conclusion} Conclusion
--------------------------

This is a good decompiler: extremely fast, reasonable output quality. It
does have a problem with some optimised code, as shown above, but most
of the time it\'s easy to correct. None of the decompilers I have tested
so far (8 in total) has passed all the tests. JODE, Dava, and Jad are
the top three.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
