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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationJrpTest?t=1536826460)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationJrpTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationJrpTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationJrpTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationJrpTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    23](http://www.program-transformation.org/view/Transform/DecompilationJrpTest?rev=1.23)
    [(diff 22)](http://www.program-transformation.org/rdiff/Transform/DecompilationJrpTest?rev1=1.23&rev2=1.22)
-   [Rev
    22](http://www.program-transformation.org/view/Transform/DecompilationJrpTest?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Transform/DecompilationJrpTest?rev1=1.22&rev2=1.21)
-   [Rev
    21](http://www.program-transformation.org/view/Transform/DecompilationJrpTest?rev=1.21)
    [(diff 20)](http://www.program-transformation.org/rdiff/Transform/DecompilationJrpTest?rev1=1.21&rev2=1.20)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationJrpTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationJrpTest?template=oopsmore&param1=1.23&param2=1.23)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationJrpTest?template=oopsmore&param1=1.23&param2=1.23)
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
Decompilation Jrp Test {#decompilation-jrp-test .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#JReversePro_Java_Decompiler_Simp} JReversePro (Java Decompiler) Simple Tests
================================================================================

I installed JReversePro version 1.4.1 (binary distribution;
[Sourceforge](http://sourceforge.net) page is
[here](http://sourceforge.net/projects/jrevpro)).

::: {.twikiToc}
-   [JReversePro (Java Decompiler) Simple
    Tests](DecompilationJrpTest#JReversePro_Java_Decompiler_Simp)
    -   [Fibo](DecompilationJrpTest#Fibo)
    -   [Casting](DecompilationJrpTest#Casting)
    -   [Inner classes](DecompilationJrpTest#Inner_classes)
    -   [Deuces Wild](DecompilationJrpTest#Deuces_Wild)
    -   [Sable Test Program](DecompilationJrpTest#Sable_Test_Program)
    -   [Optimised bytecodes](DecompilationJrpTest#Optimised_bytecodes)
    -   [Simple control flow](DecompilationJrpTest#Simple_control_flow)
    -   [Exceptions](DecompilationJrpTest#Exceptions)
    -   [Conclusion](DecompilationJrpTest#Conclusion)
:::

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}. The
output from JReversePro was this:

    // JReversePro v 1.4.1 Fri Jan 10 11:31:40 EST 2003
    import java.io.PrintStream;

    class Fibo{
        Fibo()
        {
             ;
             return;
        }
        private static int fib(int i)
        {
             if (i > 1) 
                  return (Fibo_jrp.fib(i - 1) + Fibo_jrp.fib(i - 2));
             return (i);
        }

        public static void main(String[] stringArr)
                    throws Exception
        {
             int i = 0;
             int k;
             try {
                  i = Integer.parseInt(stringArr[0]);
             }
             catch (Exception exception) {
                  System.out.println("Input error");
                  System.exit(1);
                  k = Fibo_jrp.fib(i);
                  System.out.println(new StringBuffer().append(
    "fibonacci(").append(i).append(") = ").append(k).toString());
                  return;
             }
        }
    }

When this is run, the result is blank (no output at all).

Obviously, the code to actually call the fib function is in the catch
clause, instead of outsude the whole try/catch block. When this was
corrected (moved a curly bracket), the result was correct.

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingTestSource](DecompilerCastingTestSource){.twikiLink}.
Here is the output from JReversePro for `main`:

        public static void main(String[] stringArr)
        {
             int i = 0;
             for (;j < 128;) {
                  System.out.println(new StringBuffer().append("ascii ")
    .append(i).append(" character ").append(i).toString());
                  char j = (char)(i + 1);
             }
             return;
        }

This doesn\'t compile because `j` is referenced before it is used. It
needs extensive changes to make it work. Also, the nature of the code
has changed; it\'s not working on integers whereas the original program
worked on chars.

[]{#Inner_classes} Inner classes
--------------------------------

For source, see
[DecompilerInnerClassesTestSource](DecompilerInnerClassesTestSource){.twikiLink}.
When decompiled with JReversePro, the result is

    // Decompiled by JReversePro 1.4.1
    public class Usa{

            public String name;

        public Usa()
        {
             ;
             name = "Detroit";
             return;
        }

    }

It seems to sense that there is more there, but the inner classes are
not reproduced.

[]{#Deuces_Wild} Deuces Wild
----------------------------

As a much larger test (class file is about 30 times as large as
Fibo\'s), I tried to decompile a file called deuceswild.class. It is an
applet of some 27.5K bytes (.class file), which plays the casino game of
Deuces Wild. It also calculates the optimal play, and prompts the user
if an error (suboptimal play) is made. The decompilation was quite fast
(for a decompiler written in Java); less than 5 seconds. (It takes
`javac` a little longer to compile the source code than for JReversePro
to produce it!) When recompiled, however, it had scores of errors. The
first error was at this line of source code:

    indeck = new int[][][ 14 ][ 5 ];

It\'s pretty obvious that this should be

    indeck = new int[ 14 ][ 5 ];

With this correction, the next error was because of an unknown class
\"card\". When this classfile, and a companion called cardeffects.class
were downloaded, the errors included

    deuceswild.java:650: cannot resolve symbol
    symbol  : class ActionEvent  
                                    ^
    deuceswild.java:85: incompatible types
    found   : card[]
    required: card
             card card = new card[6];

I fixed the first error with

    import java.awt.AWTEvent;
    import java.awt.event.ActionEvent;

The second was fixed by adding the missing brackets in the declaration
for reference `card` (should be type `card[]`, as the compiler told me).
There were several of these.

Next there were a lot of tedious problems like this one:

    deuceswild.java:360: possible loss of precision
    found   : double
    required: float
                       return (0.0);

Finally, this slightly interesting case:

                       do {
                            int j = 0;
                            ...
                       } while (j == 1);

The variabe `j` is out of scope in the while part of the loop. Once all
these things (perhaps a dozen edits in all) were fixed, the source code
compiled, but did not run properly. For example, after advising me to
hold all five cards, it told me \"You have a null, You win \$0\".

As with most Java decompilations, the output looks very impressive,
because the decompiler knows the names and types of all class members
(methods and data members).

When I tried to decompile the latest version of deuceswild.class (38K
verses 27.5K for the one used here), it bombed out with

    jreversepro.parser.ClassParserException :
      Referring invalid constantpool index 658

The Jode, Jad, and Dava decompilers were able to successfully decompile
this larger deuceswild.class file, except that Dava had one small error
which was easily fixed.

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source, see
[DecompilerSableTestSource](DecompilerSableTestSource){.twikiLink}. Here
is the result for function `f` (as produced by JReversePro):

        public static void f(short i)
        {
             boolean j;
             Drawable drawable;
             Circle circle;
             if (i > 10) {
                  Rectangle rectangle = new Rectangle(i , i);
                  j = rectangle.isFat();
                  Rectangle rectangle3 = rectangle;
             }
             else {
                  circle = new Circle(i);
                  j = circle.isFat();
                  drawable = circle;
             }
             if (!j) 
                  drawable.draw();
             
             return;
        }

It types the local variable `d` correctly (here called `drawable`). The
result is correct, except for the assignment to local variable
`rectangle3` (which immediately goes out of scope). (This corresponds to
line 9 of the original method.)

[]{#Optimised_bytecodes} Optimised bytecodes
--------------------------------------------

For source, see
[DecompilerOptimisedTestSource](DecompilerOptimisedTestSource){.twikiLink}.
Output from JReversePro 1.4.1 for this code was (method `f` only):

        public static void f(short i)
        {
             Drawable drawable;
             if (i > 10) {
                  Rectangle rectangle = new Rectangle;
                  rectangle(i , i);
                  i = rectangle.isFat();
                  rectangle = rectangle;
             }
             else {
                  drawable = new Circle;
                  drawable(i);
                  i = drawable.isFat();
                  drawable = drawable;
             }
             if (i == 0) 
                  drawable.draw();
             
             return;
        }

Now, in addition to the problems with the variable called `d` in the
original source code, the decompiler does not separate local variable 0
into two distinct variables (initially it is a short integer parameter;
later it is the boolean `is_fat`. Also, it didn\'t join the call to new
Rectangle (and Circle) with the call to the constructor.

[]{#Simple_control_flow} Simple control flow
--------------------------------------------

For source, see
[DecompilerControlFlowTestSource](DecompilerControlFlowTestSource){.twikiLink}.
JReversePro produces:

        public int foo(int i ,int j)
        {
             try {
                  for (;i < j;)
                       i = j++ / i;
             }
             catch (RuntimeException runtimeexception) {
                  i = 10;
                  return (j);
             }
        }

This is wrong. When the exception code is executed, the program should
continue to loop. Also, if there is no exception, when `i` is no longer
less than `j`, the program should return `j` (the code does not even
compile).

[]{#Exceptions} Exceptions
--------------------------

For source, see
[DecompilerExceptionTestSource](DecompilerExceptionTestSource){.twikiLink}.
Here is JReversePro\'s output:

        public void foo()
        {
             System.out.println("a");
             try {
                  System.out.println("b");
                  try {
                       System.out.println("c");
                  }
             }
             catch (**this_class** this) {
                  System.out.println("g");
                  System.out.println("d");
             }
             catch (**this_class** this) {
                  System.out.println("e");
                  System.out.println("f");
                  return;
             }
        }

The exception variable classes are not correct, the flow from block `g`
should be to block `f`, `d` should be in a `try` clause, not a `catch`
clause; `f` should not be in a `catch` clause.

[]{#Conclusion} Conclusion
--------------------------

This decompiler is still officially in \"alpha\" status, and the results
confirm this. However, it is one of very few that attempts to type local
references.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 10 Jan 2003

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.DecompilationJrpTest moved from
Transform.DeCompilationJrpTest on 29 Jan 2003 - 06:43 by
[MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/DecompilationJrpTest?newweb=Transform&newtopic=DeCompilationJrpTest&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
