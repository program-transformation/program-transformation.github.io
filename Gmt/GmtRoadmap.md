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
    Page](http://www.program-transformation.org/edit/Gmt/GmtRoadmap?t=1536827562)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gmt/GmtRoadmap)
-   [Attach
    File](http://www.program-transformation.org/attach/Gmt/GmtRoadmap)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gmt/GmtRoadmap?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gmt/GmtRoadmap?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Gmt/GmtRoadmap?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gmt/GmtRoadmap)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gmt/GmtRoadmap?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Gmt/GmtRoadmap?template=oopsmore&param1=1.1&param2=1.1)
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
Gmt Roadmap {#gmt-roadmap .twikiTopicTitle}
===========

::: {.twikiWebTitle}
\*Generative Model Transformer\*
:::

This is intendet to be a collection of questions and answers regarding
GMT roadmap. It also is meant to store old discussion and to make GMT
more clear to newcomers.

Should not we move our roadmap document into the Wiki? It would be a
better way to evolve roadmap. \--
[MarkKofman](../Main/MarkKofman){.twikiLink}

#### []{#ROADMAP} ROADMAP

**Q:** To follow agile approach promised in MDSD so much I would like to
see something executable GMT as soon as possible. How can we achieve
this?

**A:** Think the roadmap does this (v0.1, v0.2, \...)

------------------------------------------------------------------------

**Q:** General comment. You speak different \"languages\" in roadmap
comparing to other parts of architecture document. You have talked about
subsystems, ecore, gcore, MDA tool components. And in roadmap concepts
like domain specific language, specification tool, EMF application,\...
jumps in without introduction. I would suggest to use terms from this
architecture documents. Thats once again shows that we need proper
Terminology for our project. It will avoid confusing ourselves and GMT
users.

**A:** That will all be clarified by mapping the use case view onto the
logical view, and by the
[GmtGlossary[^?^](http://www.program-transformation.org/edit/Gmt/GmtGlossary?topicparent=Gmt.GmtRoadmap)]{.twikiNewLink
style="background : #FFFFCE;"}. But let\'s not create documentation for
documentation sake, let\'s just create enough so that we are sure we\'re
on the same page.

------------------------------------------------------------------------

**Q:** version 0.1 goal. \"In version 0.1 of GMT the specification tools
that we use to capture models expressed in domain-specific languages can
be EMF applications generated from meta models captured in Ecore.\" I am
sorry, but I don\'t read our specific activities from this goal!

**A:** Yes this is the **goal** and not the set of activities to reach
the goal. One of the next items to produce is a GMT project plan with
activities that are assigned to individuals. A simple spreadsheet will
do. Send in what you would like to contribute towards v0.1. I\'ll
collect suggestions and coordinate the activities.

------------------------------------------------------------------------

**Q:** version 0.1 goal. Why don\'t we validate ecore as foundation by
trying to pluggin FUUTje?

**A:** As you have picked up, v0.1 is a very small step. Let\'s complete
that first.

------------------------------------------------------------------------

**Q:** I would have version 0.2 as 0.1 goal. I believe simplistic
implementation of gcore is what we have to concentrate first, because it
is the core component.

**A:** Patience. Unless we can satisfy ourselves that ecore and EMF
works as we think it should, there\'s little point building gcore on an
unproven foundation. (On steep house building sites for example
engineers first test the ground for solidity and potential for slips etc
before you start drawaing up plans for a building ;-) ecore is our
building site\... It can get very expensive if you\'re building on a
difficult site ;-)

------------------------------------------------------------------------

**Q:** I am getting the feeling that we are concentrating on creating
MDA tool components instead of working on GMT core ideas. I hope this
feeling is because I am still not very familiar with GMT. If not, then
we should review roadmap goals.

**A:** The goals are driven by very down-to-earth, practical
considerations. There will be more than enough \"cool\" work on gcore.
The requirements for gcore need to be driven from concrete MDA tool
component integration scenarios as outlined above. Otherwise we\'re
building an ivory tower. See MDSD patterns on interaction between domain
engineering and application engineering.

------------------------------------------------------------------------

**Q:** If we say that we are using MDSD What step in is creating this
architecture document is MDSD paradigm? What should be other activities
done by now according to MDSD? Yes, I have read MDSD Activities paper ;)
but what I am impling here is description of specific process of how we
are going to use MDSD in GMT development. Sure only if we are going to
do so!

**A:**

------------------------------------------------------------------------

\-- [MarkKofman](../Main/MarkKofman){.twikiLink} - 28 Jun 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
