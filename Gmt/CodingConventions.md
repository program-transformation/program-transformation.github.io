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
    Page](http://www.program-transformation.org/edit/Gmt/CodingConventions?t=1536827729)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gmt/CodingConventions)
-   [Attach
    File](http://www.program-transformation.org/attach/Gmt/CodingConventions)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gmt/CodingConventions?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gmt/CodingConventions?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Gmt/CodingConventions?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Gmt/CodingConventions?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Gmt/CodingConventions?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gmt/CodingConventions?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Gmt/CodingConventions?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gmt/CodingConventions)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gmt/CodingConventions?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Gmt/CodingConventions?template=oopsmore&param1=1.3&param2=1.3)
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
Coding Conventions {#coding-conventions .twikiTopicTitle}
==================

::: {.twikiWebTitle}
\*Generative Model Transformer\*
:::

Which conventions should we follow in GMT project? There are Eclipse
conventions at <http://dev.eclipse.org/conventions.html> . Should we
follow those blindly?

In FUUT There is a target to run checkstyle with Sun conventions(Eclipse
ones are based on them). We can use it to make sure our new code is good
enough. Similar way could be applied in other GMT project components.

\-- [MarkKofman](../Main/MarkKofman){.twikiLink} - 03 Jul 2004

FUUT: What about getting rid of warning list in the Eclipse\'s problems
view? This issue could also be mentioned on the list of possible
refactoring issues, but i believe first of all we should agree on what
warnings we shall fix. Thus, this is also a coding convention issue ;)

\-- [AntonLitvinenko](../Main/AntonLitvinenko){.twikiLink} - 04 Jul 2004

FUUT: I have always used Eclipse with ignore warnings about unused
imports. Now, with Eclipse 3, I found that there are \>150 of them, so I
am fixing them all. It makes the dependencies that we have more clear. I
think that in the generated code it is more difficult to avoid unused
imports.

\-- [GhicaVanEmdeBoas](../Main/GhicaVanEmdeBoas){.twikiLink} - 05Jul
2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
