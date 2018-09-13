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
    Page](http://www.program-transformation.org/edit/Gmt/GmtArchitecture?t=1536827730)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gmt/GmtArchitecture)
-   [Attach
    File](http://www.program-transformation.org/attach/Gmt/GmtArchitecture)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gmt/GmtArchitecture?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gmt/GmtArchitecture?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Gmt/GmtArchitecture?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gmt/GmtArchitecture)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gmt/GmtArchitecture?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Gmt/GmtArchitecture?template=oopsmore&param1=1.1&param2=1.1)
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
Gmt Architecture {#gmt-architecture .twikiTopicTitle}
================

::: {.twikiWebTitle}
\*Generative Model Transformer\*
:::

This is intendet to be a collection of questions and answers regarding
GMT architecture. It also is meant to store old discussion and to make
GMT more clear to newcomers. As soon as this page is mature it can be a
source for GMT FAQ

#### []{#ARCHITECTURE_DOCUMENT} ARCHITECTURE DOCUMENT

**Q:** I think it would be of great value if you would start
Architecture description with some introduciton. For example what do you
mean by \"GMT\" or by \"GMT tool set\", \"GMT Platform\"? Purpose,
Scope, Audience and Glossary would be simple to add, however would add
great value! I would actualy create separate Glossary document, because
terminology in GMT is quite important to understand.

**A:** A short Purpose, Scope, Audience is still missing. We should make
a start. But there is no need for overlap with the glossary started on
<http://www.mdsd.info>.

------------------------------------------------------------------------

**Q:** What does \"gcore\" name stands for? GMT core? Isn\'t gmtcore a
better name then?

**A:** Just sticking with the eclipse.emf naming style (emf.ecore &
gmt.gcore).

------------------------------------------------------------------------

**Q:** Are there any prerequisites to understand the document? I am
still having hard time to understand architecture contents.

**A:** It\'s not complete yet. It\'s a living document that needs to
evolve and grow over time. But it\'s not intended as an exhaustive
design document! It\'s intention is to convey the big picture so that
GMT developers can get started and know where to look for more detail.

------------------------------------------------------------------------

**Q:** Why would GMT architecture contain \"spectoolgenerator\". Isn\'t
it one of the pluggable MDA tool components? I am not getting point of
its importance! I would concentrate first on building touchable core of
GMT architecture and then take tool components one by one and try to
integrate them.

**A:** Correct, it\'s the one \[important\] MDA tool component that\'s
part of GMT. (FUUT-je may be a second one).

------------------------------------------------------------------------

**Q:** After reading subsystem overview paragraph I am still not sure
what are the subsystems of GMT :)! Is it only gcore and
spectoolgenerator(See also previous question)? gcore seem like logical
subsystems! But what are the others, Workflow?

**A:** gcore is the subsystem that provides the interface to all the MDA
tool components. Workflow should reside withing gcore, because it is the
\"core\" of GMT. Any other subsystems outside gcore should **not** have
any dependencies to or from any MDA tool components. Examples for other
subsystems: one for integrating with the eclipse ide platform, any gmt
presentation/UI (how much of that we need depends on whether we need to
define workflows withing gmt, or whether we can leverage some open
source workflow tool that already has a UI), etc.

------------------------------------------------------------------------

**Q:** Is there compact 3-5 sentance free text description for each
subsystem? Now those description are spread through the document.

**A:** That is already the case in the UML model.

------------------------------------------------------------------------

**Q:** I think in architecture document we should also describe
decomposition of gcore itself in more details!

**A:** Only to a certain point - to clarify the responsibilities of
gcore and to define the gcore interface (in the form of Java interfaces
with complete signatures). Look at org.eclipse.emf.ecore to see how a
good package hierarchy is constructed, i.e. the interfaces that
represent the subsystem facade are defined immediately outside the
package that implements the subsystem. The nitty-gritty internals of GMT
workflow should go into a workflow design document. But we may not even
need that much of that if we leverage an external workflow tool.

------------------------------------------------------------------------

**Q:** concept of \"ecorewrapper\" I believe is a bit out of scope of
GMT architecture. Why should GMT care how tool components will implement
dependency? For example why should GMT bother how for example GME will
implement the integration. We should not care on architecture level if
they would do package called ecorewrapper or they will structure their
classes any other way. Though, it doesn\'t mean we should care on
political level and not try to help to do this integration. ecorewrapper
package itself will not help plugging the component. I think of bigger
interest would be specific interfaces and ways of plugging those
components and that should be discussed in architecture document.

**A:** The package name is not so important, let\'s just call it
\<\<ecorewrapper\>\> so that we\'ve got a name to refer to it. The
intention of this early version of the document is to draw a line in the
sand regarding the dependencies that are permissible. The important
message: no dependencies whatsoever from gcore on specific MDA tool
components. And no dependencies from MDA tool components on any GMT
package beyond gcore. The details of the gcore interface and the
requirements on \<\<ecorewrapper\>\> packages will come as the next
step.

------------------------------------------------------------------------

**Q:** In Figure 1 you mix different levels of packages. I think it is
not very good to have eclipse and ecore on the same level. It is not
very clear what dependency is this and why is it important to be on the
model!

**A:** the \"eclipse\" package there just stands for the relevant
eclipse platform stuff that serves as the foundation. I have not looked
at that yet, so don\'t take the package name literally.

------------------------------------------------------------------------

**Q:** In Figure 1. What does the yellow box Generative Model
Transformer means?

**A:** It\'s the top level package that contains gcore, and any other
gmt subsystems.

------------------------------------------------------------------------

**Q:** \"This architecture keeps GMT focussed on tool component
orchestration and on providing the integration with the org.eclipse IDE
platform\". HOW? It would be good to see more details.

**A:** Still to be done, but within the allowable dependencies defined
in the architecture document.

------------------------------------------------------------------------

**Q:** Figure 2. Doesn\'t explain much to me! What I read from this
diagram is that all tool components depend on ecore and gcore. It
didn\'t give promised idea of how MDA tool components will hook into GMT
platform. What are the interfaces?

**A:** See above. Patience, we\'ll get to that. I\'ve seen too many
teams get excited about \"internal design\" and rush into the supposedly
\"cool\" stuff completely forgetting the bigger picture and creating
external dependencies on zillions of things.

------------------------------------------------------------------------

**Q:** Figure 3. GMT package is a bit confusing. \"examples\" are
\"fuut\" are they really ment to be there?

**A:** These things are part of the complete GMT package, but they are
certainly not part of the GMT functionality that a user would typically
use. \"fuut\" should become just another \"MDA tool component\" (or two
if Ghica wants to keep the visual editor as well).

------------------------------------------------------------------------

**Q:** Now we have Logical View only. Is there any specific reason or is
it only time constraint? I would like to see for example mapping with
Use Case Model and some kind of implementation view also.

**A:** Yes, time\...Yes we need to relate the use case view to the
logical view. The implementation and deployment view are usually not a
big deal and can be added as appropriate.

------------------------------------------------------------------------

**Q:** \"For this purpose GMT will come equipped with a default set of
code generation templates that delivers a web-based specification tool
that is suitable for use in a distributed team environment.\". Web-based
tool doesn\'t seam for me as remedy for distributed team environment. I
don\'t believe it is possible to develop this in near future.

**A:** I think you may not yet see what this is about. In a nutshell, in
a distributed environment development teams of different subsystems are
typically in different locations, however all the modeling artefacts
need to be accessible to everyone just like normal source code. A web
based application modeling environment greatly eases deployment in a
large choatic environment, where developer desktops are not standardised
etc. It\'s actually not such a big deal at all to get a simple version
of that working.

------------------------------------------------------------------------

**Q:** Workflow component description is not very well connected now. It
would be good to have better description of how workflow fits into GMT.

**A:** To see what we need from a workflow component we should not
theorise, but look at the concrete requirements of \"wiring up\" oAW to
talk to GME via GMT or \"wiring up\" FUUTje/Velocity to talk to GME via
GMT. To be attractive to users the workflow needs to happen as much as
possibl behind the scenes, and the user should be working with a \"GMT
perspective\" within Eclipse to launch tools as needed. Again, maybe we
don\'t need a full-blown workflow engine but just the Eclipse plug-in
architecture. We can qualify the requirements by mapping out concrete
scenarios of the GMT use cases that explicitly refer to oAW,
FUUT-je/Velocity, GME, etc. This will lead to concrete worflow
requirements, and we use these as the starting point to define the gcore
interface(s).

------------------------------------------------------------------------

\-- [MarkKofman](../Main/MarkKofman){.twikiLink} - 28 Jun 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
