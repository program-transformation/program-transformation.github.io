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
    Page](http://www.program-transformation.org/edit/Gmt/FuutConfiguration?t=1536827729)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gmt/FuutConfiguration)
-   [Attach
    File](http://www.program-transformation.org/attach/Gmt/FuutConfiguration)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gmt/FuutConfiguration?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gmt/FuutConfiguration?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Gmt/FuutConfiguration?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gmt/FuutConfiguration?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Gmt/FuutConfiguration?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gmt/FuutConfiguration)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gmt/FuutConfiguration?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Gmt/FuutConfiguration?template=oopsmore&param1=1.2&param2=1.2)
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
Fuut Configuration {#fuut-configuration .twikiTopicTitle}
==================

::: {.twikiWebTitle}
\*Generative Model Transformer\*
:::

Since it is really difficult for a newbie to understand ideas behind the
configuration of FUUT, i believe we need a document describing the
purpose of each configuration file.

*(Ghica) Here goes\...* There are three kinds of configurations:\

1.  **start-up** - Needed is a list of plugins to load, this list is
    supplied in a **.ini** file, and a **.properties** file.\
2.  **code-generation** - Needed is a list of templates to use for code
    generation. If you use the Fuut-je built-in template language, a
    **cglist** is needed, if you use Velocity templates, a **vlist** is
    needed. Each time the code generation action is invoked, you are
    given the possibility to choose a list, and the list is read. This
    means that you can create lists, or change them without
    stopping/starting Fuut-je. Very handy when developing templates.\
3.  **batch-processing** - Here a list of operations to be performed
    must be provided in an **.ftbatch** file.\

\-- [GhicaVanEmdeBoas](../Main/GhicaVanEmdeBoas){.twikiLink} - 06 Jul
2004

Extensions of configuration files stand for:\
**cglist** - code generation list\
**vlist** - velocity list

While surfing through the FUUT documentation, i have found descritpions
for some configuration files.\
*(Ghica - I am reorganizing this list according to purpose)*\
processing of a fuut model\

**conf/fuut2s.ini** - List of FUUT plugins used for \... *the basic
Fuut-je configuration*\
**conf/FtSuperTab.ini** - List of FUUT plugins used for \... *This list
is an extension of the previous list and can be loaded multpiple times,
since you can add new tab-panels, each with its own model to your
Fuut-je workspace.*\
**conf/fuutbatch.ini** - List of FUUT plugins used during the batch
processing of fuut models. *Note that this is an example only. The
actual list needed depends on the list of actions you want to execute,
as provided by an .ftbatch file.*\

**conf/FtSwingSet.cglist** - A template set used to generate Swing
components of generated application (correct?)\
*Not exactly. This is the basic set of templates needed to generate a
full application with a Swing GUI from a **Fuut-je model**. This set is
also used for the generated parts od Fuut-je itself.*\
**conf/EMFStructure.cglist** - A template set used to generate EMF
structure of a model (correct?)\
*Almost. This is a set of templates that you can use to generate
**annotated Java**. This Java you can use to import into EMF and EMF
will create an EMF model out of it. This is the easiest way to convert a
Fuut-je model into an EMF model.*\
**conf/FtDocOnly.cglist** - A template set used to generate FUUT
documentation (correct? *yes* Javadoc? *no, it is much more compact than
Javadoc* )\
\
**conf/Velo.cglist** - A template set used to generate Velocity
templates (correct?) \-- *this should be removed from CVS. It was a
failed attempt to generate Velocity templates from Fuut-je templates.
Not worth the trouble. (Ghica)*

**conf/php.vlist** - \... *this is a set of Velocity templates to
generate PHP code and
[MySQL[^?^](http://www.program-transformation.org/edit/Gmt/MySQL?topicparent=Gmt.FuutConfiguration)]{.twikiNewLink
style="background : #FFFFCE;"} DDL from a Fuut-je model. It actually
works great, and it is very much work in progress. (Ghica)*\
**conf/FtvList.vlist** - \... *should be removed*\

**conf/exampleBatch.ftbatch** - An example file containing the sequence
of actions to be taking during a particular batch procedure. *Fuut-je
batch processing is very handy to generate code in a build procedure.
(Ghica)*

**resources/exampleBatch.properties** - An example file containing the
list of configuration properties used during the batch processing of a
fuut model (Exactly what properties are defined here?)\
**resources/Ft.properties** - List of configuration properties used for
initialization of a swing-based FUUT frontend (correct? Exactly what
properties are defined here?)\
*(Ghica) At start-up of Fuut-je you can specify a **properties** file as
parameter (default: ft.properties). If you open up one of the files, the
parameters defined in it are pretty obvious I think.*\
*One execption: \"InitialMessage =
[FtBatch[^?^](http://www.program-transformation.org/edit/Gmt/FtBatch?topicparent=Gmt.FuutConfiguration)]{.twikiNewLink
style="background : #FFFFCE;"} conf/examplebatch.ftbatch\" in the
exampleBatch.properties indicates the first action to be taken after
Fuut-je is started. In this case the
[FtBatch[^?^](http://www.program-transformation.org/edit/Gmt/FtBatch?topicparent=Gmt.FuutConfiguration)]{.twikiNewLink
style="background : #FFFFCE;"} action, that takes the .ftbatch file as
parameter (see the description about batch processing on the gmt site).*

\-- [AntonLitvinenko](../Main/AntonLitvinenko){.twikiLink} - 04 Jul 2004

My suggestion for refactoring the startup configuration processing would
be to combine the information in the .ini, .properties and .ftbatch
files into **one** XML file.

Make a model using Fuut-je that can handle this information and generate
code for it (see the Fuut-je tutorial). The generated code is capable of
reading and writing XML in the desired format, it also has a Swing GUI
that you can use to create/edit the XML files. You just have to write a
little wrapper to interface this with `FuutTool`, or whichever module
you choose to process the configuration information.

\-- [GhicaVanEmdeBoas](../Main/GhicaVanEmdeBoas){.twikiLink} - 06 Jul
2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
