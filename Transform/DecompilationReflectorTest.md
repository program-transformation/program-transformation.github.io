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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationReflectorTest?t=1536826460)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationReflectorTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationReflectorTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationReflectorTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationReflectorTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilationReflectorTest?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilationReflectorTest?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilationReflectorTest?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilationReflectorTest?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompilationReflectorTest?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationReflectorTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationReflectorTest?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationReflectorTest?template=oopsmore&param1=1.3&param2=1.3)
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
Decompilation Reflector Test {#decompilation-reflector-test .twikiTopicTitle}
============================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Reflector_NET_to_C_Decompiler_Te} Reflector .NET to C\# Decompiler Tests
============================================================================

[Reflector](http://www.aisto.com/roeder/dotnet/) is a .NET browser with
an integrated C\# decompiler. It will also display the code
\"translated\" into Visual Basic or Delphi, or disassembled as IL.
Reflector does not save an entire file of code to write to a source
file; I had to add the text in bold to the given output.

::: {.twikiToc}
-   [Reflector .NET to C\# Decompiler
    Tests](DecompilationReflectorTest#Reflector_NET_to_C_Decompiler_Te)
    -   [Fibo](DecompilationReflectorTest#Fibo)
    -   [Casting](DecompilationReflectorTest#Casting)
    -   [Inner Classes](DecompilationReflectorTest#Inner_Classes)
    -   [Sable Test
        Program](DecompilationReflectorTest#Sable_Test_Program)
    -   [Simple Control
        Flow](DecompilationReflectorTest#Simple_Control_Flow)
    -   [Image Viewer](DecompilationReflectorTest#Image_Viewer)
    -   [Conclusion](DecompilationReflectorTest#Conclusion)
:::

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboDotNetSource](DecompilerFiboDotNetSource){.twikiLink}.
Decompiled source from Reflector:

    using System;
    class Fibo {
    private static int fib(int x)
    {
        if (x > 1)
        {
            return (Fibo.fib((x - 1)) + Fibo.fib((x - 2)));
        }
        return x;
    }

    public static int Main(string[] args)
    {
          int num2 = 0;
          try
          {
                num2 = Convert.ToInt32(args[0]);
          }
          catch (Exception)
          {
                Console.WriteLine("Input error");
                return 1;
          }
          int num1 = Fibo.fib(num2);
          Console.WriteLine("fibonacci({0}) = {1}", num2, num1);
          return 0;
    }
    }

The source code compiles and runs with no modifications (other than
inserting the 3 bolded lines).

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingDotNetSource](DecompilerCastingDotNetSource){.twikiLink}.
Here is the output from Reflector:

    using System;
    class Casting {
    public static void Main(string[] args)
    {
        char ch1;
        char ch2;
        for (ch1 = '\0'; (ch1 < '\u0080'); ch1 = ch2)
        {
            Console.WriteLine("ascii {0} character {1}", ch1, ch1);
            ch2 = (ch1 + '\x01');
        }
    }
    }

The main cast is missing in the WriteLine statement. The line
`ch2=(ch1 + '\x01');` needs a cast to `(char)`. When both these changes
are made, the program compiles and runs correctly. The for loop is
reconstructed correctly, although the increment clause is imlemented a
little strangely.

[]{#Inner_Classes} Inner Classes
--------------------------------

For source, see
[DecompilerInnerClassesDotNetSource](DecompilerInnerClassesDotNetSource){.twikiLink}.
When decompiled with Reflector, the functions and hierarchy appear
correct, but is tedious to piece together from the individual functions
(and constructors). The names are **not** initialised. The print\_names
function decompiles as follows:

    public void print_names() {
        Console.WriteLine(this.name);
    }

The `this.` is not needed.

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source, see
[DecompilerSableDotNetSource](DecompilerSableDotNetSource){.twikiLink}.

Here is the output from Reflector:

    public static void f(short i)
    {
        Circle circle1;
        Drawable drawable1;
        Rectangle rectangle1;
        bool flag1;
        if (i > 10)
        {
            rectangle1 = new Rectangle(i, i);
            flag1 = rectangle1.isFat();
            drawable1 = rectangle1;
        }
        else
        {
            circle1 = new Circle(i);
            flag1 = circle1.isFat();
            drawable1 = circle1;
        }
        if (!flag1)
        {
            drawable1.draw();
        }
    }

    public static void Main(string[] args)
    {
        MainClass.f(11);
    }

I could not find a way to reproduce the class definitions readily. All
the information is there, it would just be tedious to reconstruct. To be
fair, Reflector is not designed to be a decompiler, just a browser. When
the class definitions for Circle, Rectangle, and Drawable were included,
the program compiled correctly.

[]{#Simple_Control_Flow} Simple Control Flow
--------------------------------------------

For source, see
[DecompilerControlFlowDotNetSource](DecompilerControlFlowDotNetSource){.twikiLink}.
Here is the output from Reflector:

    public static int foo(int i, int j)
    {
          int num1;
    Label_0000:
          try
          {
                while ((i < j))
                {
                      j = num1;
                      i = (j++ / i);
                }
          }
          catch (Exception)
          {
                i = 10;
                goto Label_0000;
          }
          return j;
    }
    public static void Main(string[] args)
    {
          Foo.foo(2, 3);
    }

The output does not compile, because there is an assignment to an
uninitialised variable (num1). When this is commented out, the program
compiles. The do while with continue is handled with a goto, which is
arguably not as easy to read.

[]{#Image_Viewer} Image Viewer
------------------------------

For source, see
[DecompilerImageViewerDotNetSource](DecompilerImageViewerDotNetSource){.twikiLink}.
This program was compiled with a Microsoft compiler, and so should be
easy to decompile. I did not have the libraries to compile this program,
however, it appeared to decompile without incident. As an example, here
is the function that gave Salamander and Anakrino problems:

    private static Pixbuf GetPixbufFromFile(string filename)
    {
        Pixbuf pixbuf1;
        Pixbuf pixbuf2;
        try
        {
            pixbuf1 = new Pixbuf(filename);
            pixbuf2 = pixbuf1;
        }
        catch (GException exception1)
        {
            Console.WriteLine(exception1.GetType());
            Console.WriteLine("Cannot Open file.");
            Environment.Exit(1);
            pixbuf2 = null;
        }
        return pixbuf2;
    }

No such probems are in evidence here.

For completeness, here is the main function.

    public static void Main(string[] args)
    {
          if (args.Length <= 0)
          {
                Console.WriteLine("\nUSAGE: ImageViewer.exe \n");
                return;
          }
          string text1 = args[0];
          Application.Init();
          ImageViewer.window = new Window("File Viewer");
          ImageViewer.window.SetDefaultSize(200, 200);
          ImageViewer.window.add_DeleteEvent(new EventHandler(ImageViewer.Window_Delete));
          ScrolledWindow window1 = new ScrolledWindow(new Adjustment(IntPtr.Zero), new Adjustment(IntPtr.Zero));
          VBox box1 = new VBox(false, 2);
          VBox box2 = new VBox(false, 0);
          MenuBar bar1 = new MenuBar();
          Menu menu1 = new Menu();
          MenuItem item1 = new ImageMenuItem("gtk-close", new AccelGroup(IntPtr.Zero));
          MenuItem item2 = new ImageMenuItem("gtk-open", new AccelGroup(IntPtr.Zero));
          item1.add_Activated(new EventHandler(ImageViewer.Window_Delete));
          item2.add_Activated(new EventHandler(ImageViewer.Window_Open));
          menu1.Append(item2);
          menu1.Append(new SeparatorMenuItem());
          menu1.Append(item1);
          MenuItem item3 = new MenuItem("_File");
          item3.set_Submenu(menu1);
          bar1.Append(item3);
          box2.PackStart(bar1, false, false, 0);
          Toolbar toolbar1 = new Toolbar();
          toolbar1.InsertStock("gtk-open", "Open", string.Empty, new SignalFunc(null, Window_Open), IntPtr.Zero, 0);
          toolbar1.InsertStock("gtk-close", "Close", string.Empty, new SignalFunc(null, Window_Delete), IntPtr.Zero, 1);
          box2.PackStart(toolbar1, false, false, 0);
          box1.PackStart(box2, false, false, 0);
          Pixbuf pixbuf1 = ImageViewer.GetPixbufFromFile(text1);
          ImageViewer.image = new Image(pixbuf1);
          ImageViewer.Refresh(text1, pixbuf1);
          window1.AddWithViewport(ImageViewer.image);
          box1.PackStart(window1, true, true, 0);
          window1.SetPolicy(1, 1);
          ImageViewer.window.Add(box1);
          ImageViewer.window.ShowAll();
          Application.Run();
    }

[]{#Conclusion} Conclusion
--------------------------

Although Reflector is not designed to be a decompiler, it performs
better than the other two decompilers tested.

\-- [MikeVanEmmerik](MikeVanEmmerik){.twikiLink} - 20 Aug 2004

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
