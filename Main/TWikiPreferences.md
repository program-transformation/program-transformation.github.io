::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[WebHome](WebHome){.twikiLink}**\
[Transformation](../Transform/WebHome){.twikiLink}\
[GPCE](../Gpce/WebHome){.twikiLink}\
\
[Stratego/XT](../Stratego/WebHome){.twikiLink}\
[Tiger](../Tiger/WebHome){.twikiLink}\
[Tools](../Tools/WebHome){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Main/TWikiPreferences?t=1536827718)
-   [Rename
    Page](http://www.program-transformation.org/rename/Main/TWikiPreferences)
-   [Attach
    File](http://www.program-transformation.org/attach/Main/TWikiPreferences)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Main/TWikiPreferences?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Main/TWikiPreferences?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Main/TWikiPreferences?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Main/TWikiPreferences?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Main/TWikiPreferences?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Main/TWikiPreferences?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Main/TWikiPreferences?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Main/TWikiPreferences?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Main/TWikiPreferences)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Main/TWikiPreferences?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Main/TWikiPreferences?template=oopsmore&param1=1.7&param2=1.7)
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
TWiki Preferences {#twiki-preferences .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Program-Transformation.Org
:::

-   Logo
    -   Set WEBLOGO = /pub/transformation.gif
    -   Set WEBLOGODISPLAY =
          -------------------------------------------
          [![](../pub/transformation.gif)](WebHome)
          -------------------------------------------

<!-- -->

-   Message
    -   Set BROADCASTMESSAGE =

[]{#TWiki_Platform_Settings} TWiki Platform Settings
----------------------------------------------------

-   TWiki platform name:
    -   Set WIKITOOLNAME = TWiki

<!-- -->

-   Image, URL and alternate tooltip text of TWiki logo: (can be
    overwritten by web preferences)
    -   Set WIKILOGOIMG = /pub/TWiki/TWikiLogos/twikiRobot46x50.gif
    -   Set WIKILOGOURL = <http://TWiki.org/>
    -   Set WIKILOGOALT = TWiki home

[]{#Shortcuts} Shortcuts
------------------------

-   Set STWIKIURL = <http://www.cs.uu.nl/groups/ST/twiki/bin/view>
-   Set STWIKI = [ST
    Wiki](http://www.cs.uu.nl/groups/ST/twiki/bin/view/Center)

[]{#Email_and_Proxy_Server_Settings} Email and Proxy Server Settings
--------------------------------------------------------------------

-   TWiki webmaster email address:
    -   Set WIKIWEBMASTER = <info@program-transformation.org>

<!-- -->

-   Mail host for outgoing mail. This is used for
    [WebChangesAlert[^?^](http://www.program-transformation.org/edit/Main/WebChangesAlert?topicparent=Main.TWikiPreferences)]{.twikiNewLink
    style="background : #FFFFCE;"} if Perl module `Net::SMTP` is
    installed. If not, or if `SMTPMAILHOST` is empty, the external
    sendmail program is used instead (defined by `$mailProgram` in
    `TWiki.cfg`). Examples: `mail.your.company` or `localhost`
    -   Set SMTPMAILHOST = smtp.cs.uu.nl

<!-- -->

-   Mail domain sending mail. SMTP requires that you identify the TWiki
    server sending mail. If not set, `Net::SMTP` will guess it for you.
    Ex: `twiki.your.company`
    -   Set SMTPSENDERHOST =

[]{#Plugins_Settings} Plugins Settings
--------------------------------------

-   [TWikiPlugins[^?^](http://www.program-transformation.org/edit/Main/TWikiPlugins?topicparent=Main.TWikiPreferences)]{.twikiNewLink
    style="background : #FFFFCE;"} configuration: All plugin modules
    that exist in the `lib/TWiki/Plugins` directory are activated
    automatically unless disabled by DISABLEDPLUGINS. You can optionally
    list the installed plugins in INSTALLEDPLUGINS. This is useful to
    define the sequence of plugin execution, or to specify other webs
    then the TWiki web for the plugin topics. Specify plugins as a comma
    separated list of topics.
    -   Set INSTALLEDPLUGINS =
        [DefaultPlugin](../TWiki/DefaultPlugin){.twikiLink},
        [InterwikiPlugin[^?^](http://www.program-transformation.org/edit/Plugins/InterwikiPlugin?topicparent=Main.TWikiPreferences)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   Set DISABLEDPLUGINS =
        [EmptyPlugin[^?^](http://www.program-transformation.org/edit/Main/EmptyPlugin?topicparent=Main.TWikiPreferences)]{.twikiNewLink
        style="background : #FFFFCE;"},
        [SmiliesPlugin[^?^](http://www.program-transformation.org/edit/Main/SmiliesPlugin?topicparent=Main.TWikiPreferences)]{.twikiNewLink
        style="background : #FFFFCE;"},
        [SlideShowPlugin[^?^](http://www.program-transformation.org/edit/Main/SlideShowPlugin?topicparent=Main.TWikiPreferences)]{.twikiNewLink
        style="background : #FFFFCE;"},
        [BibTexPlugin[^?^](http://www.program-transformation.org/edit/Main/BibTexPlugin?topicparent=Main.TWikiPreferences)]{.twikiNewLink
        style="background : #FFFFCE;"},
        [CommentPlugin[^?^](http://www.program-transformation.org/edit/Main/CommentPlugin?topicparent=Main.TWikiPreferences)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   Currently activated plugins:
        [DefaultPlugin](../TWiki/DefaultPlugin){.twikiLink},
        [EditTablePlugin](../TWiki/EditTablePlugin){.twikiLink},
        [InterwikiPlugin](../TWiki/InterwikiPlugin){.twikiLink},
        [RenderListPlugin](../TWiki/RenderListPlugin){.twikiLink},
        [SpreadSheetPlugin](../TWiki/SpreadSheetPlugin){.twikiLink},
        [TablePlugin](../TWiki/TablePlugin){.twikiLink}
    -   ![TIP](../pub/TWiki/TWikiDocGraphics/tip.gif){width="16"
        height="16"} **NOTE:** You can enable/disable all plugins with
        the `$disableAllPlugins` flag in the `lib/TWiki.cfg` file.

\-- [EelcoVisser](EelcoVisser){.twikiLink} - 10 Jul 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
