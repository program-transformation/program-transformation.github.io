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
    Page](http://www.program-transformation.org/edit/Gmt/FuutDependencies?t=1536827730)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gmt/FuutDependencies)
-   [Attach
    File](http://www.program-transformation.org/attach/Gmt/FuutDependencies)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gmt/FuutDependencies?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gmt/FuutDependencies?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Gmt/FuutDependencies?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gmt/FuutDependencies?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Gmt/FuutDependencies?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gmt/FuutDependencies)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gmt/FuutDependencies?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Gmt/FuutDependencies?template=oopsmore&param1=1.2&param2=1.2)
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
Fuut Dependencies {#fuut-dependencies .twikiTopicTitle}
=================

::: {.twikiWebTitle}
\*Generative Model Transformer\*
:::

I(Ghica) would like to make some remarks about splitting fuut into
various jars, considering dependency management. Maybe we can talk about
it tonight.

A candidate to put into a separate jar is the
org.eclipse.gmt.fuut.common package. This is exactly the code that needs
to be included in the classpath for all generated applications
(including fuut itself).

*What is exactly the functionality there? Is it possible to generate
code which doesn\'t use this common package \--
[MarkKofman](../Main/MarkKofman){.twikiLink}*

(Ghica) The functionality of the common package is used by the current
code generation templates. For example, it contains some Swing classes
and the generic XML parser. If you write your own templates, you may
avoid using the common package. It is a difficult question how much code
you should provide with generated code. My first version of Fuutje had a
whole framework from which the generated code inherited. The
disadvantage is, that it is much more difficult to make changes to the
code generation and to keep versions separate. The next version had no
common code at all. It turned out that this resulted in a lot of
duplication, and if you wanted to change something in code that is
actually commmon, you have to re-generate all applications. So the
common package contains what has proven to be actually common.

Similar for the org.eclipse.gmt.fuut.generator package. You will need it
in addition to common if you are using code generation in your generated
application.

*Isn\'t it too specific case to deal with that? I guess the probability
that you want to use fuut generator in you generated application is
quite low. \-- [MarkKofman](../Main/MarkKofman){.twikiLink}*

(Ghica) At contrary. A common scenario for a model-driven application
would be to first develop a (meta)model that constitutes your DSL. You
can then generate an application from this (meta)model. For example the
component model that Jorn made. Your action application would be modeled
using the DSL and the final application is generated from the generated
DSL application. In Fuutje you can use now either it\'s intrinsic
templates that are suitable for Fuutjes own tool model or something
close to it. For generated applications it is better to use VElocity
templates to further generate code. Another common application for using
generation in a (generated) application is for example to renerate
reports or html. Velocity was specifically designed as an alternative to
XSLT (XSLT is just another, rather difficult template language).

Another thing to think about is, whether we should split the packages
differently. For example, if you would not want to generate code using
Velocity, The easiest thing to do would be to remove
org.eclipse.gmt.fuut.action.FtGenVelocity from the list in the .ini
file. As a result, you would not see it, but the code is still there.
Since the space it takes is peanuts it is not problem. From a dependency
management point of view it would maybe be better to move
[FtGenVelocity[^?^](http://www.program-transformation.org/edit/Gmt/FtGenVelocity?topicparent=Gmt.FuutDependencies)]{.twikiNewLink
style="background : #FFFFCE;"} to the org.eclipse.gmt.fuut.velocity
package.

*Rearranging packages differently sound good. But in this case we should
proper design before. Doing it in refactorign style would take a lot of
time \-- [MarkKofman](../Main/MarkKofman){.twikiLink}*

Eclipse has some good facilities for rearranging modules and packages.
Almost everything is automatic. Of course you do not change
functionality this way, but it can be very effective to get the
dependencies between packages right.

We should be very careful to not create too many jars. In my previous
job the final project had a classpath of some 50 items, and I went
totally nuts from it, therefore I repackaged fuutje again into one jar
instead of the original 3. It is nice to re-use open or other source
from many places in a project, managing the classpath can become a real
nightmare and a source of very difficult to spot bugs.

*Are you worried about FUUTje own classpath or FUUTje generated
applications classpath? If first, then one idea is using Maven? If
second, I agree. I would say more: why should generated application be
dependent on FUUT jars at all? Only dependency should be generation
time, when you use FUUTje. \--
[MarkKofman](../Main/MarkKofman){.twikiLink}*

(Ghica) I am talking about the classpath for generated applications and
the enveroment where they run in. \--
[GhicaVanEmdeBoas](../Main/GhicaVanEmdeBoas){.twikiLink}

\-- [MarkKofman](../Main/MarkKofman){.twikiLink} - 28 Jun 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
