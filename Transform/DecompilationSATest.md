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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationSATest?t=1536826461)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationSATest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationSATest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationSATest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationSATest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    16](http://www.program-transformation.org/view/Transform/DecompilationSATest?rev=1.16)
    [(diff 15)](http://www.program-transformation.org/rdiff/Transform/DecompilationSATest?rev1=1.16&rev2=1.15)
-   [Rev
    15](http://www.program-transformation.org/view/Transform/DecompilationSATest?rev=1.15)
    [(diff 14)](http://www.program-transformation.org/rdiff/Transform/DecompilationSATest?rev1=1.15&rev2=1.14)
-   [Rev
    14](http://www.program-transformation.org/view/Transform/DecompilationSATest?rev=1.14)
    [(diff 13)](http://www.program-transformation.org/rdiff/Transform/DecompilationSATest?rev1=1.14&rev2=1.13)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationSATest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationSATest?template=oopsmore&param1=1.16&param2=1.16)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationSATest?template=oopsmore&param1=1.16&param2=1.16)
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
Decompilation SATest {#decompilation-satest .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Source_Again_Java_Decompiler_Tes} Source Again Java Decompiler Tests
========================================================================

::: {.twikiToc}
-   [Source Again Java Decompiler
    Tests](DecompilationSATest#Source_Again_Java_Decompiler_Tes)
    -   [Fibo](DecompilationSATest#Fibo)
    -   [Casting](DecompilationSATest#Casting)
    -   [Inner classes](DecompilationSATest#Inner_classes)
    -   [Deuces Wild](DecompilationSATest#Deuces_Wild)
    -   [Sable Test Program](DecompilationSATest#Sable_Test_Program)
    -   [Optimised bytecode](DecompilationSATest#Optimised_bytecode)
    -   [Simple control flow](DecompilationSATest#Simple_control_flow)
    -   [Exceptions](DecompilationSATest#Exceptions)
    -   [Life](DecompilationSATest#Life)
:::

[Ahpah](http://www.ahpah.com) kindly provided a copy of [Source
Again](http://www.ahpah.com/products.html) Professional version 1.10j (a
commercial decompiler). Earlier tests were based on the demonstration
decompiler available at [this
website](http://www.ahpah.com/cgi-bin/suid/~pah/demo.cgi).

[]{#Fibo} Fibo
--------------

For source code see
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}.
Decompiled output:

    // 
    // SourceAgain (TM) Professional v1.10j (C) 2003 Ahpah Software Inc
    // 

    import java.io.PrintStream;

    class Fibo {

        private static int fib(int int1)
        {
            if( int1 > 1 )
                return fib( int1 - 1 ) + fib( int1 - 2 );
            else
                return int1;
        }

        public static void main(String[] String_1darray1)
            throws Exception
        {
            int int2 = 0;
            int int3;

            try
            {
                int2 = Integer.parseInt( String_1darray1[0] );
            }
            catch( Exception Exception4 )
            {
                System.out.println( "Input error" );
                System.exit( 1 );
            }
            int3 = fib( int2 );
            System.out.println( "fibonacci(" + int2 + ") = " + int3 );
        }
    }

The output compiled correctly with no modifications.

[]{#Casting} Casting
--------------------

For source code see
[DecompilerCastingTestSource](DecompilerCastingTestSource){.twikiLink}.
Here is the output from Source Again:

    //
    // SourceAgain (TM) Professional v1.10j (C) 2003 Ahpah Software Inc
    //

    import java.io.PrintStream;

    public class Casting {

        public static void main(String[] String_1darray1)
        {
            char char2;

            for( char2 = (char) 0; char2 < 128; char2 = (char) (char2 + 1) )
                System.out.println( "ascii " + char2 + " character " + char2 );
        }
    }

This is pretty and compact, but the cast is missing. The non
professional version (as for example available on the web) gives
variable names that are to my mind prettier (e.g. \"c\" vs \"char2\"),
but both versions are incorrect.

[]{#Inner_classes} Inner classes
--------------------------------

For source code, see
[DecompilerInnerClassesTestSource](DecompilerInnerClassesTestSource){.twikiLink}.
When decompiled with Source Again, the result is:

    //
    // SourceAgain (TM) Professional v1.10j (C) 2003 Ahpah Software Inc
    //

    import java.io.PrintStream;

    public class Usa {

        public class England {

            public class Ireland {

                public String name = "Dublin";

                public void print_names()
                {
                    System.out.println( name );
                }
            }

            public String name = "London";
        }

        public String name = "Detroit";
    }

The inner classes are reproduced perfectly. This is an area where the
professional version differs markedly from the non professional version;
in the latter, the inner classes are completely missing.

[]{#Deuces_Wild} Deuces Wild
----------------------------

This is a 38K applet with two dimensional arrays of integers, some
floating point code, and so on. The output from this decompiler is very
readable. However, there were a few compile errors, all associated with
defining the variable `i` more than once. In a few cases, this was
moderately serious, because it was not clear which version of `i` some
references were referring to. When these errors were corrected, the
application compiled without warning or error. It displayed the initial
screen correctly, but the cards did not turn over, and none of the
buttons appeared to do anything.

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source code, see
[DecompilerSableTestSource](DecompilerSableTestSource){.twikiLink}. Here
is the result for function `f` (as produced by Source Again):

    // 
    // SourceAgain (TM) Professional v1.10j (C) 2003 Ahpah Software Inc
    //

    public class Main {

        public static void f(short short1)
        {
            Object Object4;
            boolean boolean5;

            if( short1 > 10 )
            {
                Object Object3 = new Rectangle( short1, short1 );

                boolean5 = ((Rectangle) Object3).isFat();
                Object4 = Object3;
            }
            else
            {
                Object Object2 = new Circle( short1 );

                boolean5 = ((Circle) Object2).isFat();
                Object4 = Object2;
            }
            if( !boolean5 )
                ((Drawable) Object4).draw();
        }

        public static void main(String[] String_1darray1)
        {
            f( (short) 11 );
        }
    }

Source Again has ignored the class hierarchy; `obj` is of type `Object`
. It is correctly cast as needed; the program compiles without error.

[]{#Optimised_bytecode} Optimised bytecode
------------------------------------------

For source code, see
[DecompilerOptimisedTestSource](DecompilerOptimisedTestSource){.twikiLink}.
This was the result from Source Again for the method `f`:

    // 
    // SourceAgain (TM) Professional v1.10j (C) 2003 Ahpah
    //

    public class Main {

        public static void f(short short1)
        {
            Object Object2;
            boolean boolean3;

            if( short1 > 10 )
            {
                Object2 = new Rectangle;
                (Rectangle) Object2( short1, short1 );
                boolean3 = ((Rectangle) Object2).isFat();
                Object2 = Object2;
            }
            else
            {
                Object2 = new Circle;
                (Circle) Object2( boolean3 );
                boolean3 = ((Circle) Object2).isFat();
                Object2 = Object2;
            }
            if( !boolean3 )
                ((Drawable) Object2).draw();
        }

        public static void main(String[] String_1darray1)
        {
            f( (short) 11 );
        }
    }

In addition, the call to `new` and the constructor for both the
`Rectangle` and the `Circle` object are separated. Strangely, all
decompilers except [Dava](DecompilationDava){.twikiLink} have had this
problem. Also, the parameter to the constructor for `Circle` should be
`short1`, not `boolean3`.

[]{#Simple_control_flow} Simple control flow
--------------------------------------------

For source code, see
[DecompilerControlFlowTestSource](DecompilerControlFlowTestSource){.twikiLink}.
Source Again produces:

        public int foo(int int1, int int2)
        {
            while( int1 < int2 )
                int1 = int2++ / int1;
            return int2;
        }

This is certainly wrong, because there is no exception handling code,
and a divide by zero error is clearly possible.

[]{#Exceptions} Exceptions
--------------------------

For source code, see
[DecompilerExceptionTestSource](DecompilerExceptionTestSource){.twikiLink}.
Here is Source Again\'s output:

        public void foo()
        {
            System.out.println( "a" );
    label_15:
            {
                try
                {
                    System.out.println( "b" );
                    try
                    {
                        System.out.println( "c" );
                        break label_15;
                    }
                    catch( Exception Exception1 )
                    {
                        System.out.println( "e" );
                    }
                }
                catch( RuntimeException RuntimeException2 )
                {
                    System.out.println( "g" );
                }
                System.out.println( "f" );
                return;
            }
            System.out.println( "d" );
        }

While this is close to correct, block `d` is not protected (if an
Exception occurs in block `d`, the code in `e` is supposed to be
executed).

[]{#Life} Life
--------------

The professional version of Source Again did a very creditable job.
There were irritating errors, mainly to do with constructors again. For
example, here is a change I had to make:

            /*
            (Coord_Pair4 = (Coord_Pair) new Coord_Pair).X = From.X;
            (Coord_Pair4 = (Coord_Pair) new Coord_Pair).Y = From.Y;
            return Coord_Pair4 = (Coord_Pair) new Coord_Pair;
            */
            Coord_Pair4 = new Coord_Pair();
            Coord_Pair4.X = From.X;
            Coord_Pair4.Y = From.Y;
            return Coord_Pair4;

I have not had time to finish this test, but it feels to me that Source
Again professional comes the closest to being able to decompile this
program.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
