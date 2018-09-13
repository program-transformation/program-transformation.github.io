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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationCcTest?t=1536826456)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationCcTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationCcTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationCcTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationCcTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/Transform/DecompilationCcTest?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Transform/DecompilationCcTest?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Transform/DecompilationCcTest?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Transform/DecompilationCcTest?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Transform/DecompilationCcTest?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Transform/DecompilationCcTest?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationCcTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationCcTest?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationCcTest?template=oopsmore&param1=1.10&param2=1.10)
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
Decompilation Cc Test {#decompilation-cc-test .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#ClassCracker_3_Java_Decompiler_S} ClassCracker 3 Java Decompiler Simple Tests
=================================================================================

I performed some simple tests on ClassCracker 3 (version 3.01), purely
as a decompiler.

::: {.twikiToc}
-   [ClassCracker 3 Java Decompiler Simple
    Tests](DecompilationCcTest#ClassCracker_3_Java_Decompiler_S)
    -   [Fibo](DecompilationCcTest#Fibo)
    -   [Casting](DecompilationCcTest#Casting)
    -   [Inner classes](DecompilationCcTest#Inner_classes)
    -   [Deuces Wild](DecompilationCcTest#Deuces_Wild)
    -   [Sable Test Program](DecompilationCcTest#Sable_Test_Program)
    -   [Optimised Bytecodes](DecompilationCcTest#Optimised_Bytecodes)
    -   [Simple control flow](DecompilationCcTest#Simple_control_flow)
    -   [Exceptions](DecompilationCcTest#Exceptions)
    -   [Conclusion](DecompilationCcTest#Conclusion)
:::

[]{#Fibo} Fibo
--------------

For source code, see
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}. The
output from ClassCracker was this:

    /* CONVERSION by ClassCracker 3 */

    import java.io.PrintStream;

    class Fibo extends Object
    {

      Fibo( )
      {
      }

      private static int fib( int locVar_0)
      {
        if( locVar_0 > 1 )  {
          return  ( fib( ( locVar_0 - 1 ) ) + fib( ( locVar_0 - 2 ) ) );
        }
        return  locVar_0;
      }

      public static void main( String[] args)  throws Exception
      {
        int locVar_1;
        int locVar_2;
        Object locVar_3;

        locVar_1 = 0;
        try {
          locVar_1 = Integer.parseInt( args[ 0 ] );
        }
        catch( Exception locVar_3 ) {
          System.out.println( "Input error" );
          System.exit( 1 );
        }
        locVar_2 = fib( locVar_1 );
        System.out.println( (new StringBuffer(  )).toString(  ) + "fibonacci(" +
    String.valueOf( locVar_1 ) + ") = " + String.valueOf( locVar_2 ) );
      }
    }

The variable names aren\'t as easy to read as some of the other
decompilers, but that\'s a minor point. The `println` call is also more
difficult to read than most. When recompiled, the above results in an
error:

    Fibo.java:31: locVar_3 is already defined in main(java.lang.String[])
        catch( Exception locVar_3 ) {

ClassCracker doesn\'t seem to have been tested with many programs
containing exceptions. When I commented out the first declaration of
locVar\_3, the program compiled and ran correctly.

[]{#Casting} Casting
--------------------

For source code, see
[DecompilerCastingTestSource](DecompilerCastingTestSource){.twikiLink}.
Here is the output from ClassCracker for `main`:

      public static void main( String[] args)
      {
        int locVar_1;

        locVar_1 = 0;
        while( locVar_1 < 128 )  {
          System.out.println( (new StringBuffer(  )).toString(  ) + "ascii " +
    String.valueOf( locVar_1 ) + " character " + String.valueOf( locVar_1 ) );
          locVar_1 = ( (char) ( locVar_1 + 1 ) );
        }
      }

Here, the `char` loop variable has been changed to `int`, and there is
no cast back to char, so the program does not work like the original.
The output compiled without errors, and if a cast is added to the last
use of `locVar_1`, the decompiled program works the same as the
original.

[]{#Inner_classes} Inner classes
--------------------------------

For source code, see
[DecompilerInnerClassesTestSource](DecompilerInnerClassesTestSource){.twikiLink}.
When decompiled with ClassCracker, the result is

    /* CONVERSION by ClassCracker 3 */

    public class Usa extends Object
    {
      public String name;

      public Usa( )
      {
        this.name = "Detroit";
      }
    }

This is equivalent to what is literally in the file `Usa.class`.
However, there is are also files `Usa$England.class` and
`Usa$England$Ireland.class` (which show up clearly in ClassCracker\'s
GUI interface). When the latter is decompiled, the result is

    /* CONVERSION by ClassCracker 3 */

    import java.io.PrintStream;

    /*
    NOTE:
    This is an inner class named "Ireland"
      within a class named "England"
        within a class named "Usa"
    */

    public class Usa$England$Ireland extends Object
    {
      public String name;
      private final Usa$England this$1;

      public Usa$England$Ireland( Usa$England locVar_1)
      {
        this.this$1 = locVar_1;
        this.name = "Dublin";
      }

      public void print_names( )
      {
        System.out.println( this.name );
      }
    }

Unfortunately, the above doesn\'t compile. At least, it appears to be
\"inner class aware\".

[]{#Deuces_Wild} Deuces Wild
----------------------------

As a much larger test (class file is about 30 times as large as
Fibo\'s), I tried to decompile a file called deuceswild.class. It is an
applet of some 38K bytes (.class file), which plays the casino game of
Deuces Wild. It also calculates the optimal play, and prompts the user
if an error (suboptimal play) is made. The decompilation was quite fast
(for a decompiler written in Java); about 2 seconds, but only the first
5 methods are decompiled. Because of this, the output was not
compilable. It did not have the problem with `indeck` that
[JReversePro](DecompilationJrpTest){.twikiLink} did. The output is
cluttered with many unnecessary and distracting prefixes of \" `this.`
\".

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source code, see
[DecompilerSableTestSource](DecompilerSableTestSource){.twikiLink}. Here
is the result for function `f` (as produced by ClassCracker):

      public static void f( short locVar_0)
      {
        Object locVar_1;
        Object locVar_2;
        Object locVar_3;
        int locVar_4;

        if( locVar_0 > 10 )  {
          locVar_2 = (new Rectangle( locVar_0, locVar_0 ));
          locVar_4 = locVar_2.isFat(  );
          locVar_3 = locVar_2;
        }
        else {
          locVar_1 = (new Circle( locVar_0 ));
          locVar_4 = locVar_1.isFat(  );
          locVar_3 = locVar_1;
        }
        if( locVar_4 == 0 )  {
          locVar_3.draw(  );
        }
      }

No attempt has been made to type the references; they are all of type
`Object`, and there are\'t even casts to allow the code to recompile.
Even the boolean is typed as an `int` (other decompilers are able to
type it as a `boolean`, presumably from the return type of `isFat`.
Using the \"batch mode\" of ClassCracker on all 4 class files at once
did not produce any improvement.

[]{#Optimised_Bytecodes} Optimised Bytecodes
--------------------------------------------

For source code, see
[DecompilerOptimisedTestSource](DecompilerOptimisedTestSource){.twikiLink}.
Output from ClassCracker for this code was (method `f` only):

      public static void f( short locVar_0)
      {
        Object locVar_1;

        if( locVar_0 > 10 )  {
          locVar_1 = (  );
          locVar_0 = locVar_1.isFat(  );
          locVar_1 = locVar_1;
        }
        else {
          locVar_1 = (  );
          locVar_0 = locVar_1.isFat(  );
          locVar_1 = locVar_1;
        }
        if( locVar_0 == 0 )  {
          locVar_1.draw(  );
        }
      }

All decompilers apart from [Dava](DecompilationDava){.twikiLink} seem to
have trouble with this code. In addition to the above problems, the
constructors for the Rectangle and Circle objects are missing.

[]{#Simple_control_flow} Simple control flow
--------------------------------------------

For source code, see
[DecompilerControlFlowTestSource](DecompilerControlFlowTestSource){.twikiLink}.
ClassCracker produces:

      public int foo( int locVar_1, int locVar_2)
      {
        Object locVar_3;

        L0: {  // this line may need to be moved but within the same
    indentation depth
          break L0;
          try {
            while( locVar_1 < locVar_2 )  {
              locVar_2 ++;
              locVar_1 = ( locVar_2 / locVar_1 );
            }
          }
        }
        catch( RuntimeException locVar_3 ) {
          locVar_1 = 10;
          break L0;
        }
        return  locVar_2;
      }

This code doesn\'t even compile. The first `break L0` is clearly wrong,
and neither of the `break` statements is in a loop. The compiler (Sun\'s
`javac`) does not consider that the `try` and `catch` are connected.

[]{#Exceptions} Exceptions
--------------------------

For source code, see
[DecompilerExceptionTestSource](DecompilerExceptionTestSource){.twikiLink}.
Here is Class Cracker\'s output:

      public void foo( )
      {
        L1: {  // this line may need to be moved but within the same
    indentation depth
          System.out.println( "a" );
          try {
            System.out.println( "b" );
            try {
              System.out.println( "c" );
            }
            catch( RuntimeException this ) {
              System.out.println( "g" );
              break L1;
            }
            System.out.println( "d" );
          }
          catch( Exception this ) {
            System.out.println( "e" );
          }
        }
        System.out.println( "f" );
      }

This looks somewhat promising, but fails for a number of reasons. The
output doesn\'t compile, because `this` can\'t be used as an exception
variable. If an `Exception` occurs in block `b`, flow will go to `e`,
which is not original program behaviour. Also, an Exception in `c` does
not go to `e` as it should.

[]{#Conclusion} Conclusion
--------------------------

The GUI for this product takes a little getting used to, but after a
while it becomes natural. It seems very fast for a Java based
decompiler, but that could be because it only decompiles the first 5
methods (only in the demo version, obviously). Unfortunately, the
decompiler, despite now being in its third version, needs some work to
cater for the tricky cases covered in these tests.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
