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
    Page](http://www.program-transformation.org/edit/Spoofax/Refactorings?t=1536825365)
-   [Rename
    Page](http://www.program-transformation.org/rename/Spoofax/Refactorings)
-   [Attach
    File](http://www.program-transformation.org/attach/Spoofax/Refactorings)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Spoofax/Refactorings?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Spoofax/Refactorings?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Spoofax/Refactorings?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Spoofax/Refactorings?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Spoofax/Refactorings?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Spoofax/Refactorings?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Spoofax/Refactorings?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Spoofax/Refactorings?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Spoofax/Refactorings)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Spoofax/Refactorings?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Spoofax/Refactorings?template=oopsmore&param1=1.4&param2=1.4)
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
Refactorings {#refactorings .twikiTopicTitle}
============

::: {.twikiWebTitle}
Spoofax
:::

[]{#Refactorings} Refactorings
------------------------------

Spoofax helps you to enrich your editor with refactorings. You can find
the refactorings in the context menu of the file being edited.

![refactoring-in-editor.png](http://strategoxt.org/pub/Spoofax/Tour/refactoring-in-editor.png)

### []{#Refactoring_Specifications} Refactoring Specifications

The `EntityLang-Builders.esv` file in the `editor` directory defines the
entries in the Refactor menu:

![refactoring-builder.png](http://strategoxt.org/pub/Spoofax/Tour/refactoring-builder.png)

The given `refactoring` specifies the \"Rename\" menu item, which is
enabled in case an ID node is selected.The menu action is bind to the
rename shortcut (Shift+Alt+R). After the user applies the rename
refactoring, a dialog is prompted with an input field labeled \"New
name\" that has the empty string as initial value.

![refactoring-rename-dialog.png](http://strategoxt.org/pub/Spoofax/Tour/refactoring-rename-dialog.png)

The OK button of the dialog triggers the action defined with the
`rename` rule that we discuss in the next paragraph.

\

### []{#Refactoring_Transformations} Refactoring Transformations

Refactorings are defined in Stratego. The `refactor.str` file in the
`trans` directory defines the renaming refactoring for the entity
language.

![refactor-rule.png](http://strategoxt.org/pub/Spoofax/Tour/refactor-rule.png)

This rule follows a fixed interface for interoperability with the
editor. The left-hand-side of the rule is a tuple of: the result of the
user input dialog, the selected node, its tree position, the complete
ast of the file, the file path and the project path. The right-hand-side
is a tuple containing the refactoring output: a list of node changes,
plus lists with errors and warnings that will be reported to the user.
Errors and warnings are specified as a tuple of the offending language
element (which location will be reported) and the error message itself.

![refactoring-semantic-error.png](http://strategoxt.org/pub/Spoofax/Tour/refactoring-semantic-error.png)

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------
  *Tip*: multiple-file refactorings can be specified in the change list using the root nodes: \[(ast-1-before, ast-1-after), (ast-2-before, ast-2-after), \...\]
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------

\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
