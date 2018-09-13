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
    Page](http://www.program-transformation.org/edit/Gmt/ModelAndTransformationManagement?t=1536827731)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gmt/ModelAndTransformationManagement)
-   [Attach
    File](http://www.program-transformation.org/attach/Gmt/ModelAndTransformationManagement)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gmt/ModelAndTransformationManagement?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gmt/ModelAndTransformationManagement?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Gmt/ModelAndTransformationManagement?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gmt/ModelAndTransformationManagement?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Gmt/ModelAndTransformationManagement?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gmt/ModelAndTransformationManagement)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gmt/ModelAndTransformationManagement?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Gmt/ModelAndTransformationManagement?template=oopsmore&param1=1.2&param2=1.2)
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
Model And Transformation Management {#model-and-transformation-management .twikiTopicTitle}
===================================

::: {.twikiWebTitle}
\*Generative Model Transformer\*
:::

First off lets make it easy on ourselves and NOT worry (yet) about
distributed tool use (we can have this as an eventual goal, along with a
\"visual aspect). Web based or not I venture to say that whatever
mechanisim we choose, once we introduce \"distributed\" use then the
same problems will have to be addressed. \--Jeff

Sure the distributed can come later, although once we have a web-based
interface, the \"only\" ;-) other thing we need is a good central
repository that can store models, see below. We could either use an SQL
database or use an object database. What such a repository should allow
you to do, is to open up a model for editing to a (small) group of
people. \--Jorn

*:) I like your smile near \"only\". As soon as we have model repository
there is no big difference how you access it. I think discussion on
Web-based or not is not very much related to
[ModelAndTransformationManagement](ModelAndTransformationManagement){.twikiLink}
topic. What do you think?* \--
[MarkKofman](../Main/MarkKofman){.twikiLink}

Ultimately what I think you need is:

-   a BA may sit together with a customer, capturing model information,
    while a designer is watching the model evolve in a different
    location, who may then modify bits and pieces.
-   Similarly two designers/developers may collaboratively work on a
    shared model even though they\'re in different locations.
-   Locking: As long as the models are accessible from multiple
    locations and updated in a repository as changes occur, it may be
    sufficient for one person to have a lock and others being able to
    watch the changes (live!). This works if the editing lock on a
    package (model part) can be passed around in a small virtual team
    like a token. (Like using a walkie tackie, you aquire the lock by
    pressing a button that signals your request to the current owner of
    the lock). The most important thing though is very simple: a locking
    mechanism at a \"package\" level, that gives access to a manageable
    model part to one person. Basically it amounts to shared workspaces
    for collaboration. If models get large, several separate workspaces
    can be used by different groups of people, with each workspace
    dealing with a separate package (model part). But to start, we can
    keep it **very simple**: One person locks a package and works on it
    and then check it back in. The \"repository\" can consist of XMI
    files and versioning is CVS (or \"Subversion\". Have you seen that
    yet? It\'s apparently \"next generation\" CVS). \--Jorn
-   Model comparisson and merge possibility \--
    [MarkKofman](../Main/MarkKofman){.twikiLink}
-   Decomposition of the model \--
    [MarkKofman](../Main/MarkKofman){.twikiLink}

Web based or not its about generation of a specification tool for use
with a specific meta-model. Having said that, a web based interface
seems to work well with the idea of \"Dynamic\" (re)generation of a
specification medium.

1.  It works on almost all platforms and is (nearly) identical in
    appearence.
2.  We have access to a good cross platform servlet reference
    implementation that is open-source (used by eGen, so we know it
    works).
3.  We know it can work, even if we can\'t vouch for the distributed
    part. However, as I said earlier this is an issue that would have to
    be address regardless of the specification medium choosen.

\--Jeff

Yes, exactly. \--Jorn

Perhaps the alternatives would come with additional issues, who knows?
\--Jeff

1.  OK, its good, but it doesn\'t help anyhow in solving needs described
    above.
2.  I am not sure what do you mean here. Do you want to say that Tomcat
    is good enough?

I would also like to mention some negative points of Web-based tools.
Those points in my opinion are quite important considering the fact that
we are talking about development tools

-   They are slow comparing to fat clients
-   They are usualy inconvinient to use.
-   They are harder to develop well
-   There is a lot to reuse in Eclipse platform

To conclude I would say that still I don\'t see any big additional value
comparing to Eclipse based solutions. If we are going to postpone model
management problems, then we should also postpone solution ideas for
now.

\-- [MarkKofman](../Main/MarkKofman){.twikiLink}

Yes. That\'s why I suggest: let\'s see how far we get with EMF for
version 0.1. Should hopefully allow us to bootstrap, and then focus on a
single user, web-based interface for generated specification tools.
\--Jorn

\-- [JornBettin](../Main/JornBettin){.twikiLink} - 13 Jun 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
