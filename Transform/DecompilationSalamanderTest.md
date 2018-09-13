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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationSalamanderTest?t=1536826461)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationSalamanderTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationSalamanderTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationSalamanderTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationSalamanderTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/Transform/DecompilationSalamanderTest?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Transform/DecompilationSalamanderTest?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Transform/DecompilationSalamanderTest?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Transform/DecompilationSalamanderTest?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Transform/DecompilationSalamanderTest?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Transform/DecompilationSalamanderTest?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationSalamanderTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationSalamanderTest?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationSalamanderTest?template=oopsmore&param1=1.10&param2=1.10)
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
Decompilation Salamander Test {#decompilation-salamander-test .twikiTopicTitle}
=============================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Salamander_NET_to_C_Decompiler_T} Salamander .NET to C\# Decompiler Tests
=============================================================================

Salamander is a commercial .NET to C\# decompiler.

::: {.twikiToc}
-   [Salamander .NET to C\# Decompiler
    Tests](DecompilationSalamanderTest#Salamander_NET_to_C_Decompiler_T)
    -   [Fibo](DecompilationSalamanderTest#Fibo)
    -   [Casting](DecompilationSalamanderTest#Casting)
    -   [Inner Classes](DecompilationSalamanderTest#Inner_Classes)
    -   [Sable Test
        Program](DecompilationSalamanderTest#Sable_Test_Program)
    -   [Simple Control
        Flow](DecompilationSalamanderTest#Simple_Control_Flow)
    -   [Image Viewer](DecompilationSalamanderTest#Image_Viewer)
:::

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboDotNetSource](DecompilerFiboDotNetSource){.twikiLink}.
Decompiled source from Salamander:

    // Decompiled by Salamander version 1.0.9
    // Copyright 2002 Remotesoft Inc. All rights reserved.
    // http://www.remotesoft.com/salamander

    using System;

    class Fibo
    {

      private static int fib(int x)
      {
        if (x > 1)
        {
          return fib(x - 1) + fib(x - 2);
        }
        else
        {
          return x;
        }
      }

      // Decompilation not complete! (2)
      public static int Main(string[] args)
      {
        int j = 0;
        try
        {
          j = Convert.ToInt32(args[0]);
        }
        catch (Exception e)
        {
          Console.WriteLine("Input error");
          int k = 1;
          return k;
        }
        goto IL_0027;
        IL_0022:  leave      IL_0027
    IL_0027:
        int i = fib(j);
        Console.WriteLine("fibonacci({0}) = {1}", j, i);
        return 0;
      }
    }

The decompilation is complete, except for a goto over a `leave` opcode.
This is presumably because Salamander has been tested only on Microsoft
compilers (and mostly only on the C\# compiler, according to the web
page). (However, see the [Image Viewer
test](DecompilationSalamanderTest#Image_Viewer){.twikiAnchorLink}
below). When the line with *leave* is commented out, the result compiles
and runs correctly.

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingDotNetSource](DecompilerCastingDotNetSource){.twikiLink}.
A few casts are required to get this program to compile correctly. Here
is the output from Salamander:

    // Decompiled by Salamander version 1.0.9
    using System;

    public class Casting
    {

      public static void Main(string[] args)
      {
        for (char ch1 = '\0'; ch1 < '\u0080'; ch1++)
        {
          Console.WriteLine("ascii {0} character {1}", ch1, ch1);
        }
      }
    }

The main cast is missing in the `WriteLine` statement. When the cast is
inserted, the program compiles and is correct.

[]{#Inner_Classes} Inner Classes
--------------------------------

For source, see
[DecompilerInnerClassesDotNetSource](DecompilerInnerClassesDotNetSource){.twikiLink}.
When decompiled with Salamander, the result is

    // Decompiled by Salamander version 1.0.9
    using System;
    public class Usa
    {
      public class England
      {
        public class Ireland
        {
          public string name = "Dublin";
          public void print_names()
          {
            Console.WriteLine(name);
          }
        }
        public string name = "London";
      }
      public string name = "Detroit";
      public static void Main(string[] args)
      {
      }
    }

It reproduced the inner classes correctly. The output compiled with no
errors.

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source, see
[DecompilerSableDotNetSource](DecompilerSableDotNetSource){.twikiLink}.
Here is the result for class `MainClass` (as produced by Salamander):

    public class MainClass
    {
      public static void f(short i)
      {
        Drawable drawable;

        bool flag;

        if (i > 10)
        {
          Rectangle rectangle = new Rectangle(i, i);
          flag = rectangle.isFat();
          drawable = rectangle;
        }
        else
        {
          Circle circle = new Circle(i);
          flag = circle.isFat();
          drawable = circle;
        }
        if (!flag)
        {
          drawable.draw();
        }
      }
      public static void Main(string[] args)
      {
        f(11);
      }

The code is reproduced correctly, and no unnecessary casts are
generated. Note the lack of a cast to the constant `11` in `Main()`;
unlike Java, no cast is necessary in C\#.

[]{#Simple_Control_Flow} Simple Control Flow
--------------------------------------------

For source, see
[DecompilerControlFlowDotNetSource](DecompilerControlFlowDotNetSource){.twikiLink}.
For function `foo`, Salamander produces:

    // Decompiled by Salamander version 1.0.9
      // Decompilation not complete! (1)
      public static int foo(int i, int j)
      {
        Exception e;

        for (; i < j; i = j++ / i)
        {
        }
        IL_0018:  leave      IL_002c
        IL_001d:  stloc.0
        i = 10;
        IL_0022:  leave      IL_0000
        IL_0027:  leave      IL_002c
        return j;
      }

It has moved the divide out of the `try` block into the `for` loop,
which is not correct. The exception code is missing, and the output is
obviously wrong.

[]{#Image_Viewer} Image Viewer
------------------------------

For source, see
[DecompilerImageViewerDotNetSource](DecompilerImageViewerDotNetSource){.twikiLink}.
This is a slightly larger example, compiled with the Microsoft C\#
compiler. Still, it has problems with branches over leave instructions,
e.g.

      private static Pixbuf GetPixbufFromFile(string filename)
      {
        Pixbuf pixbuf2;

        try
        {
          Pixbuf pixbuf1 = new Pixbuf(filename);
          pixbuf2 = pixbuf1;
        }
        catch (GException e)
        {
          Console.WriteLine(e.GetType());
          Console.WriteLine("Cannot Open file.");
          Environment.Exit(1);
          pixbuf2 = null;
        }
        goto IL_003c;
        IL_000f:  leave      IL_003c
        IL_0037:  leave      IL_003c
    IL_003c:
        return pixbuf2;
      }

The rest appears to have decompiled successfully, e.g.

      public static void Main(string[] args)
      {
        if (args.Length > 0 != false)
        {
          Console.WriteLine("\nUSAGE: ImageViewer.exe \n");
          return;
        }
        string str = args[0];
        Application.Init();
        window = new Window("File Viewer");
        window.SetDefaultSize(200, 200);
        window.DeleteEvent += new EventHandler(null.Window_Delete);
        ScrolledWindow scrolledWindow = new ScrolledWindow(
    new Adjustment(IntPtr.Zero), new Adjustment(IntPtr.Zero));
        VBox vBox1 = new VBox(false, 2);
        VBox vBox2 = new VBox(false, 0);
        MenuBar menuBar = new MenuBar();
        Menu menu = new Menu();
        MenuItem menuItem1 = new ImageMenuItem("gtk-close",
    new AccelGroup(IntPtr.Zero));
        MenuItem menuItem2 = new ImageMenuItem("gtk-open",
    new AccelGroup(IntPtr.Zero));
        menuItem1.Activated += new EventHandler(null.Window_Delete);
        menuItem2.Activated += new EventHandler(null.Window_Open);
        menu.Append(menuItem2);
        menu.Append(new SeparatorMenuItem());
        menu.Append(menuItem1);
        MenuItem menuItem3 = new MenuItem("_File");
        menuItem3.Submenu = menu;
        menuBar.Append(menuItem3);
        vBox2.PackStart(menuBar, false, false, 0);
        Toolbar toolbar = new Toolbar();
        toolbar.InsertStock("gtk-open", "Open", String.Empty,
    new SignalFunc(null, Window_Open), IntPtr.Zero, 0);
        toolbar.InsertStock("gtk-close", "Close", String.Empty,
    new SignalFunc(null, Window_Delete), IntPtr.Zero, 1);
        vBox2.PackStart(toolbar, false, false, 0);
        vBox1.PackStart(vBox2, false, false, 0);
        Pixbuf pixbuf = GetPixbufFromFile(str);
        image = new Image(pixbuf);
        Refresh(str, pixbuf);
        scrolledWindow.AddWithViewport(image);
        vBox1.PackStart(scrolledWindow, true, true, 0);
        scrolledWindow.SetPolicy(1, 1);
        window.Add(vBox1);
        window.ShowAll();
        Application.Run();
      }

The translation \"if (args.Length \> 0 = false)\" seems clumsy.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 06 Mar 2003\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
