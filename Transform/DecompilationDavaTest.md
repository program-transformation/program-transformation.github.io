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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationDavaTest?t=1536826457)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationDavaTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationDavaTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationDavaTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationDavaTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Transform/DecompilationDavaTest?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/DecompilationDavaTest?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/DecompilationDavaTest?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/DecompilationDavaTest?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/DecompilationDavaTest?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DecompilationDavaTest?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationDavaTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationDavaTest?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationDavaTest?template=oopsmore&param1=1.6&param2=1.6)
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
Decompilation Dava Test {#decompilation-dava-test .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Dava_Java_Decompiler_Tests} Dava Java Decompiler Tests
==========================================================

These tests were performed on the Dava decompiler which comes with Soot
2.0.1. The author stated in early 2003 that there is a newer version,
but it just needs to be merged with a recent version of Soot. It
doesn\'t seem to be forthcoming. A few of the tests were re-run with
Soot 2.1.0 (released Dec 2003); no differences were found compared with
2.0.1.

::: {.twikiToc}
-   [Dava Java Decompiler
    Tests](DecompilationDavaTest#Dava_Java_Decompiler_Tests)
    -   [Fibo](DecompilationDavaTest#Fibo)
    -   [Casting](DecompilationDavaTest#Casting)
    -   [Inner classes](DecompilationDavaTest#Inner_classes)
    -   [Deuces Wild](DecompilationDavaTest#Deuces_Wild)
    -   [Sable test program](DecompilationDavaTest#Sable_test_program)
    -   [Optimised bytecode](DecompilationDavaTest#Optimised_bytecode)
    -   [Simple control flow](DecompilationDavaTest#Simple_control_flow)
    -   [Exceptions](DecompilationDavaTest#Exceptions)
    -   [Life](DecompilationDavaTest#Life)
:::

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}.
Decompiled output from Dava was:

    import java.io.*;

    class Fibo
    {
        Fibo()
        {
            super();
            return;
        }

        private static int fib(int i0)
        {
            if (i0 <= 1)
            {
                return i0;
            }
            else
            {
                return Fibo.fib(i0 - 1) + Fibo.fib(i0 - 2);
            }
        }

        public static void main(java.lang.String[] r0) throws java.lang.Exception
        {
            int i0, i1;
            java.lang.Exception r1;
            i0 = 0;

            label_0:
            {
                try
                {
                    i0 = Integer.parseInt(r0[0]);
                }
                catch (Exception $r3)
                {
                    r1 = $r3;
                    System.out.println("Input error");
                    System.exit(1);
                    break label_0;
                }
            }

            i1 = Fibo.fib(i0);
            System.out.println((new StringBuffer()).append("fibonacci(").append(i0)
    .append(") = ").append(i1).toString());
            return;
        }
    }

While difficult to read and verbose, it is correct and recompiles and
runs without modification. Version 2.0.1 is even more verbose than
1.2.5, e.g. `r1 = $r3;`

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingTestSource](DecompilerCastingTestSource){.twikiLink}.
Here is Dava\'s output for `main`:

        public static void main(java.lang.String[] r0)
        {
            char c0;

            c0 = '\u0000';

            while (c0 < '\u0080')
            {
                System.out.println((new StringBuffer()).append("ascii ").append(c0)
    .append(" character ").append(c0).toString());
                c0 = (char) (c0 + 1);
            }

            return;
        }

Apart from being hard to read, the cast to integer is missing, so the
recompiled program has the wrong behaviour.

[]{#Inner_classes} Inner classes
--------------------------------

For source, see
[DecompilerInnerClassesTestSource](DecompilerInnerClassesTestSource){.twikiLink}.
When decompiled with Dava, the result is

    public class Usa
    {
        public java.lang.String name;

        public Usa()
        {
            super();

            name = "Detroit";
            return;
        }
    }

It has failed to reproduce the inner classes. However, when `javac`
compiles Usa.java, it creates in addition to Usa.class the files
Usa\$England.class and Usa\$England\$Ireland.class. When the latter is
decompiled with Dava, it produces Usa\$England\$Ireland.java, with this
in it:

    import java.io.*;
    public class Usa$England$Ireland
    {
        public java.lang.String name;
        private final Usa$England this$1;
        public Usa$England$Ireland(Usa$England r1)
        {
            super();
            this$1 = r1;
            name = "Dublin";
            return;
        }
        public void print_names()
        {
            System.out.println(name);
            return;
        }
    }

This is a reasonable decompilation of what is literally contained in the
associated .class file, but it does not compile with Sun\'s javac
compiler (`this$0` and `this$1` are reserved for internal use).

[]{#Deuces_Wild} Deuces Wild
----------------------------

I decided to try to decompile a moderately large .class file,
deuceswild.class from
<http://www.thewizardofodds.com/java/deuceswild/deuceswild.html> (the
Wizard of Odds; thanks, Wiz!). The class file can be saved by accessing
<http://www.thewizardofodds.com/java/deuceswild/deuceswild.class> in a
web browser; it\'s about 38K.

First I tried

    dava --app deuceswild

using the `dava` script mentioned above. It warned me that `card` is a
phantom class (meaning that I didn\'t provide the source for it). No
problem; I typed the [URL](URL){.twikiLink}
<http://www.thewizardofodds.com/java/deuceswild/card.class> into my
browser, and it dutifully downloaded it for me, asking me where to save
it. The same thing happed for class `cardeffects`. Then it took a while,
perhaps 3 minutes, to come up with java.lang.OutOfMemoryError. So I
added `-Xmx128M` to the dava script, and tried again. This time, it
succeeded, though it apparently decompiled every library function that
was used. Decompiling the libraries can be avoided by using
`dava deuceswild; dava card; dava cardeffects` instead of
`dava --app deuceswild`.

An error involving the type of an internal temporary variable has been
fixed in the verson of Dava that comes with soot 1.2.4. It compiled
without error. The applet seemed to run perfectly. The source code was
difficult to read in places, but then, evaluating the expected value of
a hand in Video Poker is difficult and complex at the best of times.
There is code like this where the decompiler could easily do a slightly
better job, e.g.

            $r15 = new String[13];
            $r15[0] = "Two";
            $r15[1] = "Three";
            ...
            $r15[11] = "King";
            $r15[12] = "Ace";
            cardrank = $r15;

Here, the stack variable (as indicated by the `$` in the name) could be
eliminated, and the meaningfully named `cardrank` could be used instead.

In version 2.0.1, it no longer decompiles all the library files by
default, but you have to decompile the `card` and `cardeffects` classes
separately. Although the compiled .class file is larger than before, it
compiled and ran with no modifications.

Update 5/July/2006: version 2.2.3 is producing for loops now, which is a
great improvement. See the technical report
[SABLE-TR-200-2](http://www.sable.mcgill.ca/publications/techreports/#report2006-2)
for details on the changes they have made for readability of the output.

[]{#Sable_test_program} Sable test program
------------------------------------------

For source, see
[DecompilerSableTestSource](DecompilerSableTestSource){.twikiLink}. Here
is the result for function `f` (as produced by Dava 1.2.5):

        public static void f(short s0)
        {
            boolean z0;
            Drawable r1;
            Rectangle $r3;
            Circle $r4;

            if (s0 <= 10)
            {
                $r4 = new Circle(s0);
                z0 = $r4.isFat();
                r1 = $r4;
            }
            else
            {
                $r3 = new Rectangle(s0, s0);
                z0 = $r3.isFat();
                r1 = $r3;
            }

            if (z0 == false)
            {
                r1.draw();
            }

            return;
        }

This result is correct and readable. The `d` variable of the original
source code is here called `r1` (first reference). Irritatingly, the
call from `main()` to `f()` is with constant 11, which lacks a cast to
short. However, this is not part of the current test. The output for
version 2.0.1 is similar, with different variable names.

[]{#Optimised_bytecode} Optimised bytecode
------------------------------------------

For source, see
[DecompilerOptimisedTestSource](DecompilerOptimisedTestSource){.twikiLink}.
This was the result from Dava 1.2.5 for the method `f`:

        public static void f(short s0)
        {
            Rectangle r0;
            boolean z0;
            Drawable r1;
            Circle r2;

            if (s0 <= 10)
            {
                r2 = new Circle(s0);
                z0 = r2.isFat();
                r1 = r2;
            }
            else
            {
                r0 = new Rectangle(s0, s0);
                z0 = r0.isFat();
                r1 = r0;
            }

            if (z0 == false)
            {
                r1.draw();
            }

            return;
        }

This is essentially the same code as the unoptimised version, and is
correct. All seven other decompilers tested here fail this test. In the
\"Pitfalls\" paper, the authors report that Wingsoft also fails this
test.

[]{#Simple_control_flow} Simple control flow
--------------------------------------------

For source, see
[DecompilerControlFlowTestSource](DecompilerControlFlowTestSource){.twikiLink}.
Dava 1.2.5 produces:

        public int foo(int i0, int i1)
        {
            int $i2;

            label_0:
            while (true)
            {
                try
                {
                    if (i0 < i1)
                    {
                        $i2 = i1;
                        i1 = i1 + 1;
                        i0 = $i2 / i0;
                        continue label_0;
                    }
                }
                catch (RuntimeException $r2)
                {
                    i0 = 10;
                    continue label_0;
                }

                return i1;
            }
        }

It\'s a pity the `continue` is labelled; it is not needed. (In the
example in the paper above, there is no label). It\'s also a shame that
the `i = j++/i` is split over three lines. However, the code is correct
and compiles without modification. Output for version 2.0.1 is the same,
with some extra exception code.

[]{#Exceptions} Exceptions
--------------------------

For source, see
[DecompilerExceptionTestSource](DecompilerExceptionTestSource){.twikiLink}.
Unfortunately, Dava failed for me with a null pointer exception. In the
paper, they report Dava producing correct code, handling cases `b`, `c`,
and `d` separately with three `try` statements. The exception code
(blocks `g` and `e`) are replicated, and the goto to block `f` is
accomplished with a labelled `break` statement. The new version of Dava
is expected to correct this problem. The exception still occurs in
version 2.0.1.

[]{#Life} Life
--------------

This program was originally written in Ada 95. The applet was at
<http://www.appletmagic.com/download/demo/LifeRect.html>; you may be
able to get it now at
<http://www.inmet.com/javadir/download/demo/LifeRect.html>. This is a
beautiful implementation of Conway\'s Game of Life. You can see it
running and read the source code at the above [URL](URL){.twikiLink}.
During the decompilation of the whole program (about 12 class files),
there were 4 runtime exceptions: two null pointer exceptions, and 2
class cast exceptions. The first two errors occured during the
decompilation of classes LifeRect (the top level class), and
LR\_lifeCol. Unfortunately, the results that were produced did not
compile; the first error was with this code in LR\_Colony.java:

                r15 = new LR_Colony;
                $r2 = r15;
                r15.<init>();

This sort of code is mentioned proudly in the McGill paper on type
inferencing; they use their second stage analysis to solve this typing
problem. Unfortunately, while pretty pseudo code, it isn\'t Java. When I
edited the above to

                r15 = new LR_Colony();
                $r2 = r15;

the Java compiler seemed to want to compile another file, which had
`import .*;`. When that was commented out, there was another error
similar to the one with `r15` above.

In version 2.0.1 of Dava, the missing file causes an error that I could
not work around, as per earlier versions.

------------------------------------------------------------------------

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
