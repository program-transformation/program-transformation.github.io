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
    Page](http://www.program-transformation.org/edit/Spoofax/WebPreferences?t=1536826268)
-   [Rename
    Page](http://www.program-transformation.org/rename/Spoofax/WebPreferences)
-   [Attach
    File](http://www.program-transformation.org/attach/Spoofax/WebPreferences)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Spoofax/WebPreferences?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Spoofax/WebPreferences?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Spoofax/WebPreferences?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Spoofax/WebPreferences)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Spoofax/WebPreferences?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Spoofax/WebPreferences?template=oopsmore&param1=1.1&param2=1.1)
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
Web Preferences {#web-preferences .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Spoofax
:::

[]{#TWiki_Spoofax_Web_Preferences} TWiki.Spoofax Web Preferences
----------------------------------------------------------------

The following settings are ***web preferences*** of the TWiki.Spoofax
web. These preferences overwrite the ***site-level preferences*** in
[TWikiPreferences](../TWiki/TWikiPreferences){.twikiLink}, and can be
overwritten by ***user preferences*** (your personal topic, i.e.
[TWikiGuest](../Main/TWikiGuest){.twikiLink} in the TWiki.Main web)

***Preferences:***

-   List of topics of the TWiki.Spoofax web:
    -   Set WEBTOPICLIST = [Home](WebHome){.twikiLink}
        [\|]{.twikiSeparator} [Changes](WebChanges){.twikiLink}
        [\|]{.twikiSeparator} [Index](WebIndex){.twikiLink}
        [\|]{.twikiSeparator} [Search](WebSearch){.twikiLink}
        [\|]{.twikiSeparator} Go

<!-- -->

-   Web specific background color: (Pick a lighter one of the
    [StandardColors](../TWiki/StandardColors){.twikiLink}; default
    FFD8AA)
    -   Set WEBBGCOLOR = \#FFFFFF
    -   Set WEBHEADERBGCOLOR = \#FFFFFF

<!-- -->

-   Exclude web from a `web="all"` search: (Set to `on` for hidden webs)
    -   Set NOSEARCHALL =

<!-- -->

-   Default template for new topics and form(s) for this web:
    -   [WebTopicEditTemplate[^?^](http://www.program-transformation.org/edit/Spoofax/WebTopicEditTemplate?topicparent=Spoofax.WebPreferences)]{.twikiNewLink
        style="background : #FFFFCE;"}: Default template for new topics
        in this web. (Site-level is used if topic does not exist)
    -   [TWiki.WebTopicEditTemplate](../TWiki/WebTopicEditTemplate){.twikiLink}:
        Site-level default template
    -   [TWikiForms](../TWiki/TWikiForms){.twikiLink}: How to enable
        form(s)
    -   Set WEBFORMS =

<!-- -->

-   Users or groups who ***are not*** / ***are*** allowed to ***view***
    / ***change*** / ***rename*** topics in the Spoofax web: (See
    [TWikiAccessControl](../TWiki/TWikiAccessControl){.twikiLink})
    -   Set DENYWEBVIEW =
    -   Set ALLOWWEBVIEW =
    -   Set DENYWEBCHANGE =
    -   Set ALLOWWEBCHANGE =
        [StrategoGroup](../Main/StrategoGroup){.twikiLink}
    -   Set DENYWEBRENAME =
    -   Set ALLOWWEBRENAME =
        [StrategoGroup](../Main/StrategoGroup){.twikiLink}

<!-- -->

-   Users or groups allowed to change or rename this WebPreferences
    topic: (I.e. [TWikiAdminGroup](../Main/TWikiAdminGroup){.twikiLink})
    -   Set ALLOWTOPICCHANGE =
        [StrategoGroup](../Main/StrategoGroup){.twikiLink}
    -   Set ALLOWTOPICRENAME =
        [StrategoGroup](../Main/StrategoGroup){.twikiLink}

<!-- -->

-   Web preferences that are **not** allowed to be overridden by user
    preferences:
    -   Set FINALPREFERENCES = WEBTOPICLIST, DENYWEBVIEW, ALLOWWEBVIEW,
        DENYWEBCHANGE, ALLOWWEBCHANGE, DENYWEBRENAME, ALLOWWEBRENAME

<!-- -->

-   Stuff documented at
    [TWikiPreferences](../TWiki/TWikiPreferences){.twikiLink}:
    -   Set SKIN = flexpattern
    -   Set TWIKILAYOUTURL = /pub/TWiki/PatternSkin/layout.css
    -   Set TWIKISTYLEURL =
        <http://strategoxt.org/pub/Spoofax/WebPreferences/style.css>

***Notes:***

-   A preference is defined as:\
    `6 spaces * Set NAME = value`\
    Example:
    -   Set WEBBGCOLOR = \#FFFFC0
-   Preferences are used as
    [TWikiVariables](../TWiki/TWikiVariables){.twikiLink} by enclosing
    the name in percent signs. Example:
    -   When you write variable `%WEBBGCOLOR%` , it gets expanded to
        `#FFFFFF` .
-   The sequential order of the preference settings is significant.
    Define preferences that use other preferences first, i.e. set
    `WEBCOPYRIGHT` before `WIKIWEBMASTER` since `%WEBCOPYRIGHT%` uses
    the `%WIKIWEBMASTER%` variable.
-   You can introduce new preferences variables and use them in your
    topics and templates. There is no need to change the TWiki engine
    (Perl scripts).

***Related Topics:***

-   [TWikiPreferences](../TWiki/TWikiPreferences){.twikiLink} has
    site-level preferences.
-   [TWikiUsers](../Main/TWikiUsers){.twikiLink} has a list of user
    topics. User topics can have optional user preferences.
-   [TWikiVariables](../TWiki/TWikiVariables){.twikiLink} has a list of
    common `%VARIABLES%`.
-   [TWikiAccessControl](../TWiki/TWikiAccessControl){.twikiLink}
    explains how to restrict access by users or groups.

\
[]{#TopicEnd}
:::

::: {.twikiAttachments}
  [I](WebPreferences@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Attachment](../TWiki/FileAttachment){.twikiLink} [![sort](../pub/TWiki/TablePlugin/diamond.gif)](WebPreferences@sortcol=1&table=1&up=0#sorted_table "Sort by this column")   [Action](WebPreferences@sortcol=2&table=1&up=0#sorted_table "Sort by this column")                                                                                              [Size](WebPreferences@sortcol=3&table=1&up=0#sorted_table "Sort by this column") [Date](WebPreferences@sortcol=4&table=1&up=0#sorted_table "Sort by this column")   [Who](WebPreferences@sortcol=5&table=1&up=0#sorted_table "Sort by this column")   [Comment](WebPreferences@sortcol=6&table=1&up=0#sorted_table "Sort by this column")
  ------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------- ---------------------------------------------------------------------------------- --------------------------------------------------------------------------------- -------------------------------------------------------------------------------------
  ![](../pub/icn/else.gif){width="16" height="16"}                                [style.css](../pub/Spoofax/WebPreferences/style.css)                                                                                                                          [manage](http://www.program-transformation.org/attach/Spoofax/WebPreferences?filename=style.css&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                          26.9 K 12 Feb 2010 - 15:03                                                                [LennartKats](../Main/LennartKats){.twikiLink}                                     
  ![](../pub/icn/else.gif){width="16" height="16"}                                [patternskinstyle.css](../pub/Spoofax/WebPreferences/patternskinstyle.css)                                                                                                    [manage](http://www.program-transformation.org/attach/Spoofax/WebPreferences?filename=patternskinstyle.css&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                1.3 K 12 Feb 2010 - 14:42                                                                [LennartKats](../Main/LennartKats){.twikiLink}                                     
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
