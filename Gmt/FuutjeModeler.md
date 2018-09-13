::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[WebHome](WebHome){.twikiLink}**\
[News](WebNews){.twikiLink}\
[Changes](WebChanges){.twikiLink}

------------------------------------------------------------------------

[![](http://www.program-transformation.org/twiki/pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Gmt/FuutjeModeler?t=1536827563)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gmt/FuutjeModeler)
-   [Attach
    File](http://www.program-transformation.org/attach/Gmt/FuutjeModeler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gmt/FuutjeModeler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gmt/FuutjeModeler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Gmt/FuutjeModeler?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gmt/FuutjeModeler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gmt/FuutjeModeler?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Gmt/FuutjeModeler?template=oopsmore&param1=1.1&param2=1.1)
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
Fuutje Modeler {#fuutje-modeler .twikiTopicTitle}
==============

::: {.twikiWebTitle}
\*Generative Model Transformer\*
:::

Models can be expressed in text, XMI etc. The most convenient form to
visualize a model is trough a diagram. The most commonly used diagram
notation is UML. A simple UML diagram consists of rectangles and lines
between rectangles. The rectangles represent classes and the lines
represent relationships between classes.

A class in a model should not be confused with a class that is
implemented in a programming language such as Java. In business models
there will usually be fewer model classes than programmed classes.

### []{#Model_Diagramming_in_Fuut_je} Model Diagramming in Fuut-je

The notation that Fuut-je uses for its diagramming is simplified UML,
the rectangles represent classes or interfaces and the lines are 1-1 or
1-\* relationships. Classes have *attributes* and *methods*, relations
can have names, roles, multiplicity etc. A significant feature of
Fuut-je is, that for each of the tool-model concepts: **Classes,
Attributes, Methods, Relations,** the tool user can define new
properties. These properties become part of the tool model and can be
used/accessed to steer code generation.

The Fuut-je diagramming part was originally implemented in AWT, and
later adapted to Swing. A diagrammer implemented using *JHotdraw* has
been available, but was unfortunately proprietary. With the advent of
Eclipse and SWT, and the inclusion of Fuut-je into GMT, the question
arises whether Fuut-je should continue to provide its own diagrammer and
if yes, whether this diagrammer should use SWT.

\-- [GhicaVanEmdeBoas](../Main/GhicaVanEmdeBoas){.twikiLink} - 29 Jul
2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
