::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[Home](WebHome){.twikiLink}**\
[News](WebNews){.twikiLink}\
[Recent Changes](WebChanges){.twikiLink}

[WebContents[^?^](http://www.program-transformation.org/edit/Variability/WebContents?topicparent=Variability.WebPreferences)]{.twikiNewLink
style="background : #FFFFCE;"}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Variability/WebPreferences?t=1536827705)
-   [Rename
    Page](http://www.program-transformation.org/rename/Variability/WebPreferences)
-   [Attach
    File](http://www.program-transformation.org/attach/Variability/WebPreferences)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Variability/WebPreferences?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Variability/WebPreferences?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Variability/WebPreferences?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Variability/WebPreferences?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Variability/WebPreferences?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Variability/WebPreferences)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Variability/WebPreferences?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Variability/WebPreferences?template=oopsmore&param1=1.2&param2=1.2)
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
\*Software Variability Management\*
:::

[]{#TWiki_Variability_Web_Preference} TWiki.Variability Web Preferences
-----------------------------------------------------------------------

The following settings are ***web preferences*** of the
TWiki.Variability web. These preferences overwrite the ***site-level
preferences*** in
[TWikiPreferences](../TWiki/TWikiPreferences){.twikiLink}, and can be
overwritten by ***user preferences*** (your personal topic, i.e.
[TWikiGuest](../Main/TWikiGuest){.twikiLink} in the TWiki.Main web)

***Preferences:***

-   Set WEBTITLE = **Software Variability Management**

<!-- -->

-   List of topics of the TWiki.Variability web:
    -   Set WEBTOPICLIST = [Home](WebHome){.twikiLink}
        [\|]{.twikiSeparator} [Changes](WebChanges){.twikiLink}
        [\|]{.twikiSeparator} [Index](WebIndex){.twikiLink}
        [\|]{.twikiSeparator} [Search](WebSearch){.twikiLink}
        [\|]{.twikiSeparator} Go

<!-- -->

-   Web specific background color: (Pick a lighter one of the
    [StandardColors](../TWiki/StandardColors){.twikiLink})
    -   Set WEBBGCOLOR = \#FFFF99

<!-- -->

-   Exclude web from a `web="all"` search: (Set to `on` for hidden webs)
    -   Set NOSEARCHALL =

<!-- -->

-   Default template for new topics and form(s) for this web:
    -   [WebTopicEditTemplate[^?^](http://www.program-transformation.org/edit/Variability/WebTopicEditTemplate?topicparent=Variability.WebPreferences)]{.twikiNewLink
        style="background : #FFFFCE;"}: Default template for new topics
        in this web. (Site-level is used if topic does not exist)
    -   [TWiki.WebTopicEditTemplate](../TWiki/WebTopicEditTemplate){.twikiLink}:
        Site-level default template
    -   [TWikiForms](../TWiki/TWikiForms){.twikiLink}: How to enable
        form(s)
    -   Set WEBFORMS =

<!-- -->

-   Users or groups who ***are not*** / ***are*** allowed to ***view***
    / ***change*** / ***rename*** topics in the Variability web: (See
    [TWikiAccessControl](../TWiki/TWikiAccessControl){.twikiLink})
    -   Set DENYWEBVIEW =
    -   Set ALLOWWEBVIEW =
    -   Set DENYWEBCHANGE = [TWikiGuest](../Main/TWikiGuest){.twikiLink}
    -   Set ALLOWWEBCHANGE =
    -   Set DENYWEBRENAME = [TWikiGuest](../Main/TWikiGuest){.twikiLink}
    -   Set ALLOWWEBRENAME =

<!-- -->

-   Users or groups allowed to change or rename this WebPreferences
    topic: (I.e. [TWikiAdminGroup](../Main/TWikiAdminGroup){.twikiLink})
    -   Set ALLOWTOPICCHANGE =
    -   Set ALLOWTOPICRENAME =

<!-- -->

-   Web preferences that are **not** allowed to be overridden by user
    preferences:
    -   Set FINALPREFERENCES = WEBTOPICLIST, DENYWEBVIEW, ALLOWWEBVIEW,
        DENYWEBCHANGE, ALLOWWEBCHANGE, DENYWEBRENAME, ALLOWWEBRENAME

***Notes:***

-   A preference is defined as:\
    `6 spaces * Set NAME = value`\
    Example:
    -   Set WEBBGCOLOR = \#FFFFC0
-   Preferences are used as
    [TWikiVariables](../TWiki/TWikiVariables){.twikiLink} by enclosing
    the name in percent signs. Example:
    -   When you write variable `%WEBBGCOLOR%` , it gets expanded to
        `#FFFF99` .
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

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
