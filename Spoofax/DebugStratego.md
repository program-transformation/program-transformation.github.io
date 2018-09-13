::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[Spoofax](http://www.program-transformation.org/view/Spoofax/WebHome)**

\

**[Home](WebHome){.twikiLink}**

**[Tour and screenshots](Tour){.twikiLink}**

**[Documentation](Documentation){.twikiLink}**

**[Download](Download){.twikiLink}**

**[Research](Research){.twikiLink}**

**[Development](Development){.twikiLink}**

**[Support](Support){.twikiLink}**

\

\
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Spoofax/DebugStratego?t=1536826260)
-   [Rename
    Page](http://www.program-transformation.org/rename/Spoofax/DebugStratego)
-   [Attach
    File](http://www.program-transformation.org/attach/Spoofax/DebugStratego)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Spoofax/DebugStratego?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Spoofax/DebugStratego?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Spoofax/DebugStratego?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Spoofax/DebugStratego?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Spoofax/DebugStratego?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Spoofax/DebugStratego?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Spoofax/DebugStratego?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Spoofax/DebugStratego)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Spoofax/DebugStratego?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Spoofax/DebugStratego?template=oopsmore&param1=1.3&param2=1.3)
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
Debug Stratego {#debug-stratego .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Spoofax
:::

[]{#Debugging_Stratego_in_Spoofax_Pr} Debugging Stratego in Spoofax Projects
----------------------------------------------------------------------------

Spoofax supports debugging of Stratego code used in the implementation
of the various editor services. The Stratego debugger re-uses the
Eclipse Debug Perspective making debugging Stratego code similair to
debugging Java code.

Debugging can be enabled/disabled per project as it has a negative
impact on the performance. The debugger has to be enabled for two
components: (1) enable debug instrumentation in the ant build file and
(2) enable the debug mode for the runtime.

Currently, debugging support is only available in the nightly builds of
Spoofax, use <http://spoofax.org/update/nightly> as the Eclipse Update
site.

### []{#Enable_Debug_Instrumentation} Enable Debug Instrumentation

First, to enable debug instrumentation add a file called `.debugmode` in
the project directory. Adding this file will make sure the project is
build with debug information.

Second, change the provider in the Builders.esv file from `ctree` to
`jar`.

And third, change the \"all\" ant target from

    <target name="all" depends="spoofaximp.default"/>

to

    <target name="all" depends="spoofaximp.default.jar"/>

Now rebuild the project. After a succesful build the `trans-debug`
directory contains the stratego files from the `trans` directory
instrumented with debug information. The instrumented stratego files are
compiled to a jar file that is located in the `include` directory.

### []{#Enable_Debug_Runtime} Enable Debug Runtime

Although the project is build with debug information the debug mode
still has to be enabled. It is wise to only enable debug mode when it is
really needed as it has a huge impact on the performance. Disabling
debug mode will still instrument the stratego code, but any breakpoints
are ignored.

Select a DSL file (probably in the test directory of the project).
Select *Enable debug mode* from the *Transform* menu to enable stratego
debugging for this Spoofax project.

![enable-debug-mode-menu.png](http://strategoxt.org/pub/Spoofax/DebugStratego/enable-debug-mode-menu.png)

Sometimes the project will rebuild. Check if the debug mode was actually
enabled by clicking on the *Transform* menu, the *Enable debug mode*
menu item should have changed to *Disable debug mode*. If not select the
*Enable debug mode* menu item again.

Now open a stratego file and set a breakpoint.

![breakpoint-in-editor.png](http://strategoxt.org/pub/Spoofax/DebugStratego/breakpoint-in-editor.png)

When this breakpoint is hit Eclipse switches to the Debug View and the
execution is suspended.

![debug-view-overview.png](http://strategoxt.org/pub/Spoofax/DebugStratego/debug-view-overview.png)

The variables window shows the available variables, the current term
(`*current*`) and the names of the dynamic rules that are available
(`*dynamic rules*`).

![variables.png](http://strategoxt.org/pub/Spoofax/DebugStratego/variables.png)

Also, you can control the execution of the program with Step Into (F5),
Step Over (F6), Step Return (F7) and Resume (F8).

![execution-control.png](http://strategoxt.org/pub/Spoofax/DebugStratego/execution-control.png)

\-- [RickyLindeman](../Main/RickyLindeman){.twikiLink} - 22 Jun 2011\
[]{#TopicEnd}
:::

::: {.twikiAttachments}
  [I](DebugStratego@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Attachment](../TWiki/FileAttachment){.twikiLink} [![sort](../pub/TWiki/TablePlugin/diamond.gif)](DebugStratego@sortcol=1&table=1&up=0#sorted_table "Sort by this column")   [Action](DebugStratego@sortcol=2&table=1&up=0#sorted_table "Sort by this column")                                                                                                    [Size](DebugStratego@sortcol=3&table=1&up=0#sorted_table "Sort by this column") [Date](DebugStratego@sortcol=4&table=1&up=0#sorted_table "Sort by this column")   [Who](DebugStratego@sortcol=5&table=1&up=0#sorted_table "Sort by this column")   [Comment](DebugStratego@sortcol=6&table=1&up=0#sorted_table "Sort by this column")
  ------------------------------------------------------------------------------ ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------------------------------------- --------------------------------------------------------------------------------- -------------------------------------------------------------------------------- ------------------------------------------------------------------------------------
  ![](../pub/icn/else.gif){width="16" height="16"}                               [breakpoint-in-editor.png](../pub/Spoofax/DebugStratego/breakpoint-in-editor.png)                                                                                            [manage](http://www.program-transformation.org/attach/Spoofax/DebugStratego?filename=breakpoint-in-editor.png&revInfo=1 "change, update, previous revisions, move, delete...")                                                                               180.9 K 22 Jun 2011 - 09:56                                                               [RickyLindeman](../Main/RickyLindeman){.twikiLink}                                
  ![](../pub/icn/else.gif){width="16" height="16"}                               [debug-view-overview.png](../pub/Spoofax/DebugStratego/debug-view-overview.png)                                                                                              [manage](http://www.program-transformation.org/attach/Spoofax/DebugStratego?filename=debug-view-overview.png&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                144.9 K 22 Jun 2011 - 09:59                                                               [RickyLindeman](../Main/RickyLindeman){.twikiLink}                                
  ![](../pub/icn/else.gif){width="16" height="16"}                               [enable-debug-mode-menu.png](../pub/Spoofax/DebugStratego/enable-debug-mode-menu.png)                                                                                        [manage](http://www.program-transformation.org/attach/Spoofax/DebugStratego?filename=enable-debug-mode-menu.png&revInfo=1 "change, update, previous revisions, move, delete...")                                                                              20.8 K 22 Jun 2011 - 09:59                                                               [RickyLindeman](../Main/RickyLindeman){.twikiLink}                                
  ![](../pub/icn/else.gif){width="16" height="16"}                               [execution-control.png](../pub/Spoofax/DebugStratego/execution-control.png)                                                                                                  [manage](http://www.program-transformation.org/attach/Spoofax/DebugStratego?filename=execution-control.png&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                   15.6 K 22 Jun 2011 - 09:59                                                               [RickyLindeman](../Main/RickyLindeman){.twikiLink}                                
  ![](../pub/icn/else.gif){width="16" height="16"}                               [variables.png](../pub/Spoofax/DebugStratego/variables.png)                                                                                                                  [manage](http://www.program-transformation.org/attach/Spoofax/DebugStratego?filename=variables.png&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                           45.4 K 22 Jun 2011 - 10:00                                                               [RickyLindeman](../Main/RickyLindeman){.twikiLink}                                
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
