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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationAnakrinoTest?t=1536826455)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationAnakrinoTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationAnakrinoTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationAnakrinoTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationAnakrinoTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/DecompilationAnakrinoTest?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DecompilationAnakrinoTest?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilationAnakrinoTest?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilationAnakrinoTest?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilationAnakrinoTest?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilationAnakrinoTest?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationAnakrinoTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationAnakrinoTest?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationAnakrinoTest?template=oopsmore&param1=1.4&param2=1.4)
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
Decompilation Anakrino Test {#decompilation-anakrino-test .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Anakrino_NET_to_C_Decompiler_Tes} Anakrino .NET to C\# Decompiler Tests
===========================================================================

[Anakrino](http://www.saurik.com/net/exemplar/) is a .NET to C\#
decompiler, released under a BSD-like license. These tests refer to
\"Interim \#9\" (Anakrino9.zip). Anakrino does not save an entire file
of code to write to a source file; I had to add the text in **bold** to
the given output.

The distributed binaries require Windows XP (or perhaps another Windows
based .NET JIT). It would not run under Mono version 0.20 (current in
early March 2003).

::: {.twikiToc}
-   [Anakrino .NET to C\# Decompiler
    Tests](DecompilationAnakrinoTest#Anakrino_NET_to_C_Decompiler_Tes)
    -   [Fibo](DecompilationAnakrinoTest#Fibo)
    -   [Casting](DecompilationAnakrinoTest#Casting)
    -   [Inner Classes](DecompilationAnakrinoTest#Inner_Classes)
    -   [Sable Test
        Program](DecompilationAnakrinoTest#Sable_Test_Program)
    -   [Simple Control
        Flow](DecompilationAnakrinoTest#Simple_Control_Flow)
    -   [Image Viewer](DecompilationAnakrinoTest#Image_Viewer)
    -   [Conclusion](DecompilationAnakrinoTest#Conclusion)
:::

[]{#Fibo} Fibo
--------------

For source, see
[DecompilerFiboDotNetSource](DecompilerFiboDotNetSource){.twikiLink}.
Decompiled source from Anakrino:

    using System;
    class Fibo {
    private static int fib(int x) {
        if (x > 1)
            return Fibo.fib(x - 1) + Fibo.fib(x - 2);
        return x;
    }

    public static int Main(string[] args) {
        int local0;
        int local1;
        Exception local2;
        int local3;

        local1 = 0;
        try {
            local1 = Convert.ToInt32(args[0]);
        }
        catch (Exception local2) {
            Console.WriteLine("Input error");
            local3 = 1;
            <{ class ILEngineer::Ops::MSIL::Leave }>
        }
        local0 = Fibo.fib(local1);
        Console.WriteLine("fibonacci({0}) = {1}", local1, local0);
        return 0;
        return local3;
    }
    }

There are several errors in this output. Most obviously, there is the
*Leave* code which should be `return local3`. The `return local3;` at
the end should be removed. Finally, `local2` is declared twice. When all
these changes are made, the result compiles and runs correctly.

[]{#Casting} Casting
--------------------

For source, see
[DecompilerCastingDotNetSource](DecompilerCastingDotNetSource){.twikiLink}.
Here is the output from Anakrino:

    using System;
    class Casting {
    public static void Main(string[] args) {
        char local0;
        char local1;

        local0 = '';
        while (local0 < 128) {
            Console.WriteLine("ascii {0} character {1}", local0, local0);
            local1 = local0 + 1;
            local0 = local1;
        }
    }
    }

The main cast is missing in the `WriteLine` statement. The character
constant for character 0 is `'\0'` , not `''` as given. The line
`local1 = local0 + 1;` needs to be replaced with
`local1 = (char) (((int)local0)+1);`. When all these changes are made,
the program compiles and is correct.

[]{#Inner_Classes} Inner Classes
--------------------------------

For source, see
[DecompilerInnerClassesDotNetSource](DecompilerInnerClassesDotNetSource){.twikiLink}.
When decompiled with Anakrino, the result appears correct, but tedious
to piece together from the individual functions (and constructors). The
`print_names` function decompiles as follows:

    public void print_names() {
        Console.WriteLine(this.name);
    }

The `this.` is not needed.

[]{#Sable_Test_Program} Sable Test Program
------------------------------------------

For source, see
[DecompilerSableDotNetSource](DecompilerSableDotNetSource){.twikiLink}.
The decompiler exited with a runtime fault when this program was loaded.

[]{#Simple_Control_Flow} Simple Control Flow
--------------------------------------------

For source, see
[DecompilerControlFlowDotNetSource](DecompilerControlFlowDotNetSource){.twikiLink}.
The decompiler exited with a runtime fault when this program was loaded.

[]{#Image_Viewer} Image Viewer
------------------------------

For source, see
[DecompilerImageViewerDotNetSource](DecompilerImageViewerDotNetSource){.twikiLink}.
This program was compiled with a Microsoft compiler, and so should be
easy to decompile. Unfortunately, it had problems with the same method
that caused problems for Salamander:

    private static Pixbuf GetPixbufFromFile(string filename) {
        Pixbuf local0;
        GException local1;
        Pixbuf local2;

        try {
            local0 = new Pixbuf(filename);
            local2 = local0;
            <{ class ILEngineer::Ops::MSIL::Leave }>;
        }
        catch (GException local1) {
            Console.WriteLine(local1.GetType());
            Console.WriteLine("Cannot Open file.");
            Environment.Exit(1);
            local2 = null;
            <{ class ILEngineer::Ops::MSIL::Leave }>;
        }
        return local2;
    }

Also, `local1` is declared twice.

For completeness, here is the `main` function.

    public static void Main(string[] args) {
        string local0;
        ScrolledWindow local1;
        VBox local2;
        VBox local3;
        MenuBar local4;
        Menu local5;
        MenuItem local6;
        MenuItem local7;
        MenuItem local8;
        Toolbar local9;
        Pixbuf local10;

        if (args.Length > 0 == 0) {
            Console.WriteLine("\nUSAGE: ImageViewer.exe <filename>\n");
            return;
        }
        local0 = args[0];
        Application.Init();
        ImageViewer.window = new Window("File Viewer");
        ImageViewer.window.SetDefaultSize(200, 200);
        ImageViewer.window.add_DeleteEvent(new EventHandler(null,
    ImageViewer.Window_Delete));
        local1 = new ScrolledWindow(new Adjustment(IntPtr.Zero),
    new Adjustment(IntPtr.Zero));
        local2 = new VBox(0, 2);
        local3 = new VBox(0, 0);
        local4 = new MenuBar();
        local5 = new Menu();
        local6 = new ImageMenuItem("gtk-close", new AccelGroup(IntPtr.Zero));
        local7 = new ImageMenuItem("gtk-open", new AccelGroup(IntPtr.Zero));
        local6.add_Activated(new EventHandler(null, ImageViewer.Window_Delete));
        local7.add_Activated(new EventHandler(null, ImageViewer.Window_Open));
        local5.Append(local7);
        local5.Append(new SeparatorMenuItem());
        local5.Append(local6);
        local8 = new MenuItem("_File");
        local8.Submenu = local5;
        local4.Append(local8);
        local3.PackStart(local4, false, false, 0);
        local9 = new Toolbar();
        local9.InsertStock("gtk-open", "Open", String.Empty,
    new SignalFunc(null, ImageViewer.Window_Open), IntPtr.Zero, 0);
        local9.InsertStock("gtk-close", "Close", String.Empty,
    new SignalFunc(null, ImageViewer.Window_Delete), IntPtr.Zero, 1);
        local3.PackStart(local9, false, false, 0);
        local2.PackStart(local3, false, false, 0);
        local10 = ImageViewer.GetPixbufFromFile(local0);
        ImageViewer.image = new Image(local10);
        ImageViewer.Refresh(local0, local10);
        local1.AddWithViewport(ImageViewer.image);
        local2.PackStart(local1, true, true, 0);
        local1.SetPolicy(1, 1);
        ImageViewer.window.Add(local2);
        ImageViewer.window.ShowAll();
        Application.Run();
    }

The translation \"if (args.Length \> 0 == 0)\" seems clumsy and
confusing.

[]{#Conclusion} Conclusion
--------------------------

As of early March 2003, Anakrino is not a mature decompiler. It may be
useful for examining snippets of code here and there, or even for
decompiling small assemblies if you have a fair bit of time spare.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 07 Mar 2003\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
