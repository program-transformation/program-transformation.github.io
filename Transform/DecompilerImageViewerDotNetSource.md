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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerImageViewerDotNetSource?t=1536826465)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerImageViewerDotNetSource)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerImageViewerDotNetSource)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerImageViewerDotNetSource?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerImageViewerDotNetSource?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/DecompilerImageViewerDotNetSource?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DecompilerImageViewerDotNetSource?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilerImageViewerDotNetSource?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilerImageViewerDotNetSource?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilerImageViewerDotNetSource?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilerImageViewerDotNetSource?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerImageViewerDotNetSource)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerImageViewerDotNetSource?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerImageViewerDotNetSource?template=oopsmore&param1=1.4&param2=1.4)
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
Decompiler Image Viewer Dot Net Source {#decompiler-image-viewer-dot-net-source .twikiTopicTitle}
======================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

I found this sample program in a page called [Sample gtk\#
applications](http://primates.ximian.com/~duncan/Mono/). The program is
already compiled (possibly with a now-obsolete version of the Microsoft
C\# compiler), but this is a non-Mono executable that should decompile
readily.

Source code:

    //
    // ImageViewer.cs: A Image Viewer written in C#
    //
    // Author: Duncan Mak  (duncan@ximian.com)
    //
    // Copyright (C) 2002, Ximian. Inc.
    //

    using Gtk;
    using Gdk;
    using GtkSharp;
    using Gdk.Imaging;
    using System;

    public class ImageViewer {

        static Gtk.Window window = null;
        static Gtk.FileSelection selections = null;
        static Gtk.Image image = null;
        static Gtk.Dialog about = null;

        public static void Main (string [] args)
        {
            if (args.Length <= 0) {
                Console.WriteLine ("\nUSAGE: ImageViewer.exe \n");
                return;
            }

            string filename = args [0];
            Application.Init ();
            window = new Gtk.Window ("Image Viewer");
            window.SetDefaultSize (200, 200);

            window.DeleteEvent += new EventHandler (Window_Delete);

            Gtk.ScrolledWindow scrolled_window = new Gtk.ScrolledWindow (
    new Adjustment (IntPtr.Zero), new Adjustment (IntPtr.Zero));

            Gtk.VBox vbox = new VBox (false, 2);
            Gtk.VBox menubox = new VBox (false, 0);

            // Pack menubar
            MenuBar mb = new MenuBar ();

            Menu file_menu = new Menu ();
            MenuItem exit_item = new ImageMenuItem (
    "gtk-close", new Gtk.AccelGroup (IntPtr.Zero));
            MenuItem open_item = new ImageMenuItem (
    "gtk-open", new Gtk.AccelGroup (IntPtr.Zero));
            exit_item.Activated += new EventHandler (Window_Delete);
            open_item.Activated += new EventHandler (Window_Open);

            file_menu.Append (open_item);
            file_menu.Append (new Gtk.SeparatorMenuItem ());
            file_menu.Append (exit_item);
            MenuItem file_item = new MenuItem ("_File");
            file_item.Submenu = file_menu;

            mb.Append (file_item);
            menubox.PackStart (mb, false, false, 0);

            // Pack toolbar
            Gtk.Toolbar toolbar = new Gtk.Toolbar ();
            toolbar.InsertStock ("gtk-open", "Open", String.Empty,
    new Gtk.SignalFunc (Window_Open), IntPtr.Zero, 0);
            toolbar.InsertStock ("gtk-close", "Close", String.Empty,
    new Gtk.SignalFunc (Window_Delete), IntPtr.Zero, 1);
            menubox.PackStart (toolbar, false, false, 0);
            vbox.PackStart (menubox, false, false, 0);

            Pixbuf pix = GetPixbufFromFile (filename);
            image = new Image (pix);

            Refresh (filename, pix);

            scrolled_window.AddWithViewport (image);
            vbox.PackStart (scrolled_window, true, true, 0);

            scrolled_window.SetPolicy (PolicyType.Automatic,
    PolicyType.Automatic);
            window.Add (vbox);
            window.ShowAll ();

            Application.Run ();
        }

        static void Refresh (string new_filename, Gdk.Pixbuf p)
        {
            window.Resize (p.Width + 25, p.Height + 75);
            window.Title = String.Format ("Image Viewer: {0}",
    new_filename);
        }

        static Gdk.Pixbuf GetPixbufFromFile (string filename)
        {
            try {
                Pixbuf p = new Pixbuf (filename);
                return p;

            } catch (GLib.GException e) {
                Console.WriteLine (e.GetType ());
                Console.WriteLine ("Cannot Open file.");
                Environment.Exit (1);
                return null;
            }

        }

        static void Window_Delete (object o, EventArgs args)
        {
            SignalArgs s = (SignalArgs) args;
            Application.Quit ();
            s.RetVal = true;
        }

        static void Window_Open (object o, EventArgs args)
        {
            Window_Open ();
        }

        static void Window_Delete ()
        {
            Application.Quit ();
        }

        static void Window_Open ()
        {
            selections = new Gtk.FileSelection ("Open... ");
            selections.Modal = true;
            selections.OkButton.Clicked += new EventHandler (OK_Clicked);
            selections.CancelButton.Clicked +=
    new EventHandler (Cancel_Clicked);
            selections.ShowAll ();
        }

        static void OK_Clicked (object o, EventArgs args)
        {
            Pixbuf p = GetPixbufFromFile (selections.Filename);
            image.Pixbuf = p;

            Refresh (selections.Filename, p);

            selections.Hide ();
        }

        static void Cancel_Clicked (object o , EventArgs args)
        {
            selections.Hide ();
        }
    }

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
