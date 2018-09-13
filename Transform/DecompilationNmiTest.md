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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationNmiTest?t=1536826460)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationNmiTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationNmiTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationNmiTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationNmiTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Transform/DecompilationNmiTest?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/DecompilationNmiTest?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/DecompilationNmiTest?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DecompilationNmiTest?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilationNmiTest?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilationNmiTest?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationNmiTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationNmiTest?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationNmiTest?template=oopsmore&param1=1.5&param2=1.5)
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
Decompilation Nmi Test {#decompilation-nmi-test .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#NMI_Java_Code_Viewer} NMI Java Code Viewer
==============================================

This is a commercial bytecode to Java decompiler and disassembler. It
runs under Windows only, even though it claims to have been written in
Java. I ran an evaluation copy of version 6.0. For brevity, NMI Java
Code Viewer will be abbreviated to NJCV. Results are startlingly similar
to those of Jad; the only difference is that Jad irritatingly puts data
declarations after the methods.

::: {.twikiToc}
-   [NMI Java Code Viewer](DecompilationNmiTest#NMI_Java_Code_Viewer)
    -   [Fibo](DecompilationNmiTest#Fibo)
    -   [Casting](DecompilationNmiTest#Casting)
    -   [Inner classes](DecompilationNmiTest#Inner_classes)
    -   [Deuces Wild](DecompilationNmiTest#Deuces_Wild)
    -   [Sable Test Program](DecompilationNmiTest#Sable_Test_Program)
    -   [Optimised code.](DecompilationNmiTest#Optimised_code)
    -   [Simple control flow](DecompilationNmiTest#Simple_control_flow)
    -   [Exceptions](DecompilationNmiTest#Exceptions)
    -   [Life](DecompilationNmiTest#Life)
    -   [Conclusion](DecompilationNmiTest#Conclusion)
:::

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}.
Decompiled source from NJCV:

    // NMI's Java Code Viewer 6.0 
    // http://www.njcv.tk
    // Registered to Evaluation Copy
    // Generated Sun Feb 23 2003 22:20:45 
    // Source File Name:   Fibo.java

    import java.io.PrintStream;

    class Fibo {
        Fibo() {
        }
        private static int fib(int i) {
            if(i > 1)
                return fib(i - 1) + fib(i - 2);
            else
                return i;
        }

        public static void main(String args[]) throws Exception {
            int i = 0;
            try {
                i = Integer.parseInt(args[0]);
            }
            catch(Exception exception) {
                System.out.println("Input error");
                System.exit(1);
            }
            int j = fib(i);
            System.out.println("fibonacci(" + i + ") = " + j);
        }
    }

As you can see, the decompilation is almost identical to the source. The
output compiled and ran perfectly with no changes required.

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingTestSource](DecompilerCastingTestSource){.twikiLink}.
Here is the output from NJCV:

    public class Casting {
        public Casting() {
        }
        public static void main(String args[]) {
            for(char c = '\0'; c < 128; c++)
                System.out.println("ascii " + (int)c + " character " + c);
        }
    }

As you can see, it\'s quite compact, readable, very similar to the
original, and is correct. No modifications were needed to recompile it.

[]{#Inner_classes} Inner classes
--------------------------------

For source, see
[DecompilerInnerClassesTestSource](DecompilerInnerClassesTestSource){.twikiLink}.
When decompiled with NJCV (turning on \"inner class support\"), the
result is

    public class Usa {
        public class England {
            public class Ireland {
                public String name;
                public void print_names() {
                    System.out.println(name);
                }
                public Ireland() {
                    name = "Dublin";
                }
            }
            public String name;
            public England() {
                name = "London";
            }
        }
        public String name;
        public Usa() {
            name = "Detroit";
        }
    }

It reproduced the inner classes correctly.

[]{#Deuces_Wild} Deuces Wild
----------------------------

This is a 38K applet with two dimensional arrays of integers, some
floating point code, and so on. It decompiled in a fraction of a second,
with no errors, and recompiled and ran perfectly with no modifications.
The arrays of strings are initialised naturally, e.g.

        String cardrank[] = {
            "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine",
    "Ten", "Jack", 
            "Queen", "King", "Ace"
        };

However, the string before this one also had ten strings on one line,
producing a line that had well over a hundred columns. This is a very
minor issue.

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source, see
[DecompilerSableTestSource](DecompilerSableTestSource){.twikiLink}. Here
is the result for function `f` (as produced by NJCV):

        public static void f(short word0) {
            Object obj;
            boolean flag;
            if(word0 > 10) {
                Rectangle rectangle = new Rectangle(word0, word0);
                flag = rectangle.isFat();
                obj = rectangle;
            } else {
                Circle circle = new Circle(word0);
                flag = circle.isFat();
                obj = circle;
            }
            if(!flag)
                ((Drawable) (obj)).draw();
        }

As you can see, it had no trouble with the tricky `d` variable (here
called `obj`), and produced correct code which compiled without
modification. However, the variable `d` of the original program becomes
here `obj` of type `Object`, but it\'s cast as needed. Better
decompilers infer that obj should be of type `Drawable`.

[]{#Optimised_code}[]{#Optimised_code_} Optimised code.
-------------------------------------------------------

For source, see
[DecompilerOptimisedTestSource](DecompilerOptimisedTestSource){.twikiLink}.
This was the result from NJCV for the method `f`:

        public static void f(short word0) {
            Object obj;
            if(word0 > 10) {
                obj = JVM INSTR new #37  <Class Rectangle>;
                ((Rectangle) (obj)).Rectangle(word0, word0);
                word0 = ((Rectangle) (obj)).isFat();
                obj = obj;
            } else {
                obj = JVM INSTR new #15  <Class Circle>;
                ((Circle) (obj)).Circle(word0);
                word0 = ((Circle) (obj)).isFat();
                obj = obj;
            }
            if(word0 == 0)
                ((Drawable) (obj)).draw();
        }

As you can see, it is confused with the two constructors. When the above
problems were corrected e.g. `obj = new Rectangle(word0, word0)`, the
code still did not compile, because NJCV failed to separate the ranges
of the local variable (part `short`, part `boolean`).

[]{#Simple_control_flow} Simple control flow
--------------------------------------------

For source, see
[DecompilerControlFlowTestSource](DecompilerControlFlowTestSource){.twikiLink}.
NJCV produces:

    class foo {
        foo() {
        }
        public int foo(int i, int j) {
            while(true) 
                try {
                    while(i < j) 
                        i = j++ / i;
                    break MISSING_BLOCK_LABEL_28;
                }
                catch(RuntimeException runtimeexception) {
                    i = 10;
                }
            return j;
        }
        public void main() {
            foo(2, 3);
        }
    }

The \"=while(true)\" is preserved, but it has not gotten the continue or
break correct.

[]{#Exceptions} Exceptions
--------------------------

NJVC produces this:

    class foo {
        foo() {
        }
        public void foo() {
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
        public static void main() {
            foo foo1 = new foo();
        }
    }

This code will obviously not compile, and it has made no attempt to
separate the exception handling cases. In fact, the execptions have all
gone.

[]{#Life} Life
--------------

This version of Conway\'s Game of Life was compiled from Ada 95 source
code. The applet is at
<http://www.appletmagic.com/download/demo/LifeRect.html>. NJCV seemed to
be happy decompiling one class at a time, but it produced code with
errors, e.g.

            if(Result >= 0) goto _L2; else goto _L1
    _L1:
            int i = Result + 60;
            i;
            if(i < 0 || i > 59)
                throw new IndexOutOfBoundsException();
            return;
    _L2:

This would appear to be a simple if-then-else. Note the line with just
`"i;"`; what is missing here? At least the index bounds checking is
natural (compare with JODE output, which has a `"do while(false)"`
loop).

NJCV was able to type some parameters that JODE regarded as type errors
(e.g. the parameter to `Directed_Copy`).

At least it never bombs out with runtime errors, so it would presumably
be possible to edit the code to get it to work properly (with a fair bit
of effort).

[]{#Conclusion} Conclusion
--------------------------

This is overall a good decompiler: very fast, good output quality. It
does have a few problems here and there, but most of the time it\'s easy
to correct. Its output is not significantly better than that of Jad
(which is free for non commercial use), but with NJCV you get support.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 23 Feb 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
