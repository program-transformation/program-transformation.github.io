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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationJodeTest?t=1536826459)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationJodeTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationJodeTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationJodeTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationJodeTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    18](http://www.program-transformation.org/view/Transform/DecompilationJodeTest?rev=1.18)
    [(diff 17)](http://www.program-transformation.org/rdiff/Transform/DecompilationJodeTest?rev1=1.18&rev2=1.17)
-   [Rev
    17](http://www.program-transformation.org/view/Transform/DecompilationJodeTest?rev=1.17)
    [(diff 16)](http://www.program-transformation.org/rdiff/Transform/DecompilationJodeTest?rev1=1.17&rev2=1.16)
-   [Rev
    16](http://www.program-transformation.org/view/Transform/DecompilationJodeTest?rev=1.16)
    [(diff 15)](http://www.program-transformation.org/rdiff/Transform/DecompilationJodeTest?rev1=1.16&rev2=1.15)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationJodeTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationJodeTest?template=oopsmore&param1=1.18&param2=1.18)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationJodeTest?template=oopsmore&param1=1.18&param2=1.18)
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
Decompilation Jode Test {#decompilation-jode-test .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#JODE_open_source_Java_Decompiler} JODE open source Java Decompiler Simple Tests
===================================================================================

::: {.twikiToc}
-   [JODE open source Java Decompiler Simple
    Tests](DecompilationJodeTest#JODE_open_source_Java_Decompiler)
    -   [Fibo](DecompilationJodeTest#Fibo)
    -   [Casting](DecompilationJodeTest#Casting)
    -   [Inner classes](DecompilationJodeTest#Inner_classes)
    -   [Deuces Wild](DecompilationJodeTest#Deuces_Wild)
    -   [Sable Test Program](DecompilationJodeTest#Sable_Test_Program)
    -   [Optimised code.](DecompilationJodeTest#Optimised_code)
    -   [Simple control flow](DecompilationJodeTest#Simple_control_flow)
    -   [Exceptions](DecompilationJodeTest#Exceptions)
    -   [Life](DecompilationJodeTest#Life)
    -   [Conclusion](DecompilationJodeTest#Conclusion)
:::

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}.
Decompiled source from JODE:

    /* Fibo - Decompiled by JODE
     * Visit http://jode.sourceforge.net/
     */

    class Fibo
    {
        private static int fib(int i) {
            if (i > 1)
                return fib(i - 1) + fib(i - 2);
            return i;
        }
        
        public static void main(String[] strings) throws Exception {
            int i = 0;
            try {
                i = Integer.parseInt(strings[0]);
            } catch (Exception exception) {
                System.out.println("Input error");
                System.exit(1);
            }
            int i_0_ = fib(i);
            System.out.println("fibonacci(" + i + ") = " + i_0_);
        }
    }

As you can see, the decompilation is almost identical to the source
(save the strange local variable name). The output compiled and ran
perfectly with no changes required.

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingTestSource](DecompilerCastingTestSource){.twikiLink}.
Here is the output from JODE:

    /* Casting - Decompiled by JODE
     * Visit http://jode.sourceforge.net/
     */

    public class Casting
    {
        public static void main(String[] strings) {
            for (char c = '\0'; c < '\u0080'; c++)
                System.out.println("ascii " + (int) c + " character " + c);
        }
    }

As you can see, it\'s quite readable, very similar to the original, and
is correct. No modifications were needed to recompile it.

[]{#Inner_classes} Inner classes
--------------------------------

For source, see
[DecompilerInnerClassesTestSource](DecompilerInnerClassesTestSource){.twikiLink}.
When decompiled with JODE, the result is

    /* Usa - Decompiled by JODE
     * Visit http://jode.sourceforge.net/
     */

    public class Usa
    {
        public String name = "Detroit";
        
        public class England
        {
            public String name = "London";
            
            public class Ireland
            {
                public String name = "Dublin";
                
                public void print_names() {
                    System.out.println(name);
                }
            }
        }
    }

It reproduced the inner classes correctly.

[]{#Deuces_Wild} Deuces Wild
----------------------------

This is a 38K applet with two dimensional arrays of integers, some
floating point code, and so on. It decompiled in about 8 seconds, with
no errors, and recompiled and ran perfectly with no modifications. The
arrays of strings are initialised naturally, e.g.

    String[] cardrank
            = { "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine",
                "Ten", "Jack", "Queen", "King", "Ace" };
    String[] cardsuit = { "clubs", "diamonds", "hearts", "spades" };

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source, see
[DecompilerSableTestSource](DecompilerSableTestSource){.twikiLink}. Here
is the result for function `f` (as produced by JODE):

        public static void f(short i) {
            boolean bool;
            Drawable drawable;
            if (i > 10) {
                Rectangle rectangle = new Rectangle(i, i);
                bool = rectangle.isFat();
                drawable = rectangle;
            } else {
                Circle circle = new Circle(i);
                bool = circle.isFat();
                drawable = circle;
            }
            if (!bool)
                drawable.draw();
        }

As you can see, it had no trouble with the tricky `d` variable (here
called `drawable`), and produced correct code which compiled without
modification.

[]{#Optimised_code}[]{#Optimised_code_} Optimised code.
-------------------------------------------------------

For source, see
[DecompilerOptimisedTestSource](DecompilerOptimisedTestSource){.twikiLink}.
This was the result from JODE for the method `f`:

     
        public static void f(short i) {
            boolean bool;
            Drawable drawable;
            if (i > 10) {
                Rectangle rectangle = new Rectangle;
                ((UNCONSTRUCTED)rectangle).Rectangle(i, i);
                bool = rectangle.isFat();
                drawable = rectangle;
            } else {
                Circle circle = new Circle;
                ((UNCONSTRUCTED)circle).Circle(i);
                bool = circle.isFat();
                drawable = circle;
            }
            if (!bool)
                drawable.draw();
        }

As you can see, it is confused with the two constructors. I have no idea
why this is any sort of problem for decompilers; they all see a call to
new, then a call to the constructor. They must expect the constructor to
immediately follow the call to new, or something.

When the above problems were corrected (e.g.
`Rectangle rectangle = new Rectangle(i, i)`, the code compiled and is
correct.

[]{#Simple_control_flow} Simple control flow
--------------------------------------------

For source, see
[DecompilerControlFlowTestSource](DecompilerControlFlowTestSource){.twikiLink}.
JODE produces:

        public int foo(int i, int i_0_) {
            while (i < i_0_) {
                try {
                    i = i_0_++ / i;
                } catch (RuntimeException runtimeexception) {
                    i = 10;
                }
            }
            return i_0_;
        }

While not like the original source code, I think that this would be
correct. After an exception, the `continue` (in the original source)
should cause the program to escape to the outer `while` loop; the Jode
version stays in the inner `while` loop, which is all that there really
is in the outer loop.

[]{#Exceptions} Exceptions
--------------------------

For source, see
[DecompilerExceptionTestSource](DecompilerExceptionTestSource){.twikiLink}.
Unfortunately, JODE bombs out with this assertion:

    jode.AssertError: Exception handlers ranges are intersecting:
    [16, 47] and [8, 24].

While this is true, and the exception handlers will never overlap in
programs compiled from Java source code, this is not a good solution to
the problem.

[]{#Life} Life
--------------

This version of Conway\'s Game of Life was compiled from Ada 95 source
code. The applet is at
<http://www.appletmagic.com/download/demo/LifeRect.html>. The only way I
could find to decompile the whole program at once was to jar up all the
.class files. When this was done, the decompilation produced numerous
type errors, and many of the decompiled results did not recompile. Some
of the errors were due to one .class file being missing
(interface/java/NonLimited\_.class). The applet seems to run fine
without this class file. I ended up copying
interface/java/NonLimited.class to keep it happy. It looks as though the
output could be forced to compile with a lot of work. Not good, but
better than all the other decompilers.

There was a lot of code like this:

            do {
                if (i >= 1) {
                    if (i <= 1000)
                        break;
                }
                throw new IndexOutOfBoundsException();
            } while (false);

which could be cleaned up to the much more readable

      if (i < 1 || i > 1000) throw new IndexOutOfBoundsException();

or removed altogether if the array is declared correctly.

[]{#Conclusion} Conclusion
--------------------------

This is overall an excellent decompiler: fast, good output quality. It
does have a problem with some optimised code, as shown above, but most
of the time it\'s easy to correct. None of the Java decompilers I have
tested so far (eight in total) has passed all tests. Of these, and with
these limited tests, JODE has the fewer errors.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
