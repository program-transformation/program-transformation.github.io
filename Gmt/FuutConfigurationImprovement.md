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
    Page](http://www.program-transformation.org/edit/Gmt/FuutConfigurationImprovement?t=1536827729)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gmt/FuutConfigurationImprovement)
-   [Attach
    File](http://www.program-transformation.org/attach/Gmt/FuutConfigurationImprovement)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gmt/FuutConfigurationImprovement?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gmt/FuutConfigurationImprovement?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Gmt/FuutConfigurationImprovement?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Gmt/FuutConfigurationImprovement?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Gmt/FuutConfigurationImprovement?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gmt/FuutConfigurationImprovement?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Gmt/FuutConfigurationImprovement?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gmt/FuutConfigurationImprovement)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gmt/FuutConfigurationImprovement?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Gmt/FuutConfigurationImprovement?template=oopsmore&param1=1.3&param2=1.3)
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
Fuut Configuration Improvement {#fuut-configuration-improvement .twikiTopicTitle}
==============================

::: {.twikiWebTitle}
\*Generative Model Transformer\*
:::

Before joining this discussion take a look at
[FuutConfiguration](FuutConfiguration){.twikiLink} topic.

Do You think, it is better to separate batch processing configuration
and GUI application configuration into separate parts of configuration?
I believe it would be more convinient to have one configuration file (as
You pointed out on the wiki) and some property of this would tell if
FUUT-je to be ran as a GUI app or in batch mode. I think it is possible
to create such structure that will represent/encapsulate equally well
properties of both configurations. \--
[AntonLitvinenko](../Main/AntonLitvinenko){.twikiLink} - 06 Jul 2004

*I think it is better, as I said in the wiki, to combine batch and GUI
processing. Actually, Fuutje is not aware at all whether it is running
batch or GUI. It depends on the plugins you are loading. You can even do
batch in the GUI. It is like a movie you are showing then.* \--
[GhicaVanEmdeBoas](../Main/GhicaVanEmdeBoas){.twikiLink} - 07 Jul 2004

`Combining GUI FUUTje and headless FUUTje (running in batch mode) doesn't mean we should not separate configuration for those! I think final result we would like to achieve is that by configuring build script we can create distribution of headless FUUT or GUI versioned FUUT. It would be good not to leave too much configuration for a user.`
\-- [MarkKofman](../Main/MarkKofman){.twikiLink} - 07 Jul 2004

*It depends. It is not clear to me when you want to run the build. If it
is done by us and we provide 2 different downloadable versions, I
strongly disagree. The idea of various ways to run Fuut-je is to
determine at **start-up** of Fuut-je what to include anf what not.
Still, the user has more classes, not used at that moment in the jar on
his local disk.* \--
[GhicaVanEmdeBoas](../Main/GhicaVanEmdeBoas){.twikiLink} - 12 Jul 2004

`One file vs many configuration files.  Sure one file is better, however I don't think it is reasonable sometimes. E.g. we will need to maintain 2 similar configuration files both for GUI FUUTje and for headless. It will make sence to break up the file into units logicaly and to reuse them.`
\-- [MarkKofman](../Main/MarkKofman){.twikiLink} - 07 Jul 2004

I have already tried Jfig,
[XmlDigester[^?^](http://www.program-transformation.org/edit/Gmt/XmlDigester?topicparent=Gmt.FuutConfigurationImprovement)]{.twikiNewLink
style="background : #FFFFCE;"} and Castor tools for managing the XML
configuration of projects. I think, it is a good idea to use FUUT-je
facilities to manage its configuration, since if i am not mistaken this
will let us to have configuration in a object-oriented style (like
castor with its mapping files and marshalling/unmarshalling
functionality). On the other hand Jfig is very simple and is very
similar to java \"properties configuration\" in style.
[XmlDigester[^?^](http://www.program-transformation.org/edit/Gmt/XmlDigester?topicparent=Gmt.FuutConfigurationImprovement)]{.twikiNewLink
style="background : #FFFFCE;"} is capable of processing configuration in
both object-oriented and properties style and it is quite easy to parse
XMLs with it. But neither of these libraries have a tool for editing the
configuration. So,in my opinion, it would be cool to generate such GUI
tool by FUUT-je. \--
[AntonLitvinenko](../Main/AntonLitvinenko){.twikiLink} - 06 Jul 2004

*You will find that Fuut-je is the easiest to use of all these tools,
once you understand how a model maps onto the XML. Just do the tutorial,
and look at the XML that is saved if you run the generated application
and enter some data in it.* \--
[GhicaVanEmdeBoas](../Main/GhicaVanEmdeBoas){.twikiLink} - 07 Jul 2004

`Ghica, I guess you are a bit biased ;)`
`Some points which in my opinion should influence our decision:`

-   `Using FUUTje for configuration would be "politicaly correct" :). It is ideal case to show benefits of model driven approach or generative approach.`
-   `Using a tool like Jfig can add additional features specific to managing configuration files and not only XML parsing`
-   `By using tool meant specially for convinient XML parsing we could gain some good ideas and probably later implement them in the FUUTje`

\-- [MarkKofman](../Main/MarkKofman){.twikiLink} - 07 Jul 2004

*Of course I am biased :-). Not unfounded though. I have encountered
lots of different kinds of XML files in quite a few projects. Each time
I have adapted Fuut-je to allow to handle parsing and modeling the XML
in the easiest way possible. I did not try Jfig and I have no
opportunity to do so now. How would we use it for Fuut-je? Let\'s have a
more specific problem stement. What would you like to have in the
configuration and how would you like to influence the build-running of
Fuut-je with it, in addition to what is there now?* \--
[GhicaVanEmdeBoas](../Main/GhicaVanEmdeBoas){.twikiLink} - 12 Jul 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
