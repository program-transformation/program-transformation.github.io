::: {#content}
::: {#header}
![Stratego
Logo](http://stratego.insanity.nl/StrategoLogoTextlessWhite-100px.png)

<div>

[Octave](WebHome){.twikiLink} {#web-title}
=============================

Octave-Compiler.org

</div>
:::

::: {#main}
::: {#main2}
Web Preferences {#web-preferences .topic-header}
===============

::: {.topic-text}
[]{#TWiki_Octave_Web_Preferences} TWiki.Octave Web Preferences
--------------------------------------------------------------

The following settings are ***web preferences*** of the TWiki.Octave
web. These preferences overwrite the ***site-level preferences*** in
[TWikiPreferences](../TWiki/TWikiPreferences){.twikiLink}, and can be
overwritten by ***user preferences*** (your personal topic, i.e.
[TWikiGuest](../Main/TWikiGuest){.twikiLink} in the TWiki.Main web)

The following settings are ***web preferences*** of the TWiki.Octave
web. These preferences overwrite the ***site-level preferences*** in
[TWikiPreferences](../TWiki/TWikiPreferences){.twikiLink}, and can be
overwritten by ***user preferences*** (your personal topic, i.e.
[TWikiGuest](../Main/TWikiGuest){.twikiLink} in the TWiki.Main web)

-   -   Set FTP = <ftp://ftp.stratego-language.org/pub>
    -   Set SVNROOT = <https://svn.cs.uu.nl:12443/repos>
    -   Set DUMPROOT = <https://svn.cs.uu.nl:12443/dist/StrategoXT>
    -   Set SVNSTRATEGOXT =
        <https://svn.cs.uu.nl:12443/repos/StrategoXT>
    -   Set JIRA = <https://catamaran.labs.cs.uu.nl/jira>
    -   Set ISSUE = <https://catamaran.labs.cs.uu.nl/jira/browse>

***Preferences:***

-   -   Set PAGEHEADERCONTENTS =

<!-- -->

-   -   Set WEBTITLE = Octave-Compiler.org
    -   Set SHORTWEBTITLE = Octave
    -   Set WEBSUBTITLE = Octave-Compiler.org

<!-- -->

-   -   Set WEBLOGO =
        /pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png
    -   Set WEBICON =
        /pub/Stratego/StrategoLogo/stratego-logo-16only.ico

<!-- -->

-   List of topics of the TWiki.Octave web:
    -   Set WEBTOPICLIST =

<!-- -->

-   Web specific background color: (Pick a lighter one of the
    [StandardColors](../TWiki/StandardColors){.twikiLink})
    -   Set WEBBGCOLOR = \#EEEEAA

<!-- -->

-   Web specific background color: (Pick a lighter one of the
    [StandardColors](../TWiki/StandardColors){.twikiLink})
    -   Set WEBCONTENTBGCOLOR = \#EEEEAA

<!-- -->

-   List this web in the [SiteMap](../TWiki/SiteMap){.twikiLink}:
    -   If yes, Set SITEMAPLIST = `on`, and add the \"what\" and \"use
        to\...\" description for the site map. Make sure to list only
        links that include the name of the web, e.g. Octave.Topic links.
    -   Set SITEMAPLIST = on
    -   Set SITEMAPWHAT = The
        [Stratego](../Stratego/WebHome){.twikiLink} web is the home of
        Stratego, a language for program transformation based on the
        paradigm of [rewriting
        strategies](../Stratego/RewritingStrategy){.twikiLink}. The aim
        of this language is to provide an expressive and declarative
        language for expressing all kinds of program transformations.
        The web includes
        [publications](../Stratego/StrategoPublications){.twikiLink} on
        Stratego, [download](../Stratego/StrategoDownload){.twikiLink}
        of the
        [StrategoCompiler](../Stratego/StrategoCompiler){.twikiLink},
        [documentation](../Stratego/StrategoDocumentation){.twikiLink},
        and descriptions of
        [applications](../Stratego/StrategoApplication){.twikiLink}.
    -   Set SITEMAPUSETO = \...

<!-- -->

-   Exclude web from a `web="all"` search: (Set to `on` for hidden webs)
    -   Set NOSEARCHALL =

<!-- -->

-   Default template for new topics and form(s) for this web:
    -   [WebTopicEditTemplate[^?^](http://www.program-transformation.org/edit/Octave/WebTopicEditTemplate?topicparent=Octave.WebPreferences)]{.twikiNewLink
        style="background : #FFFFCE;"}: Default template for new topics
        in this web. (Site-level is used if topic does not exist)
    -   [TWiki.WebTopicEditTemplate](../TWiki/WebTopicEditTemplate){.twikiLink}:
        Site-level default template
    -   [TWikiForms](../TWiki/TWikiForms){.twikiLink}: How to enable
        form(s)
    -   Set WEBFORMS =

<!-- -->

-   Users or groups who ***are not*** / ***are*** allowed to ***view***
    / ***change*** / ***rename*** topics in the Octave web: (See
    [TWikiAccessControl](../TWiki/TWikiAccessControl){.twikiLink})
    -   Set DENYWEBVIEW =
    -   Set ALLOWWEBVIEW =
    -   Set DENYWEBCHANGE = [TWikiGuest](../Main/TWikiGuest){.twikiLink}
    -   Set ALLOWWEBCHANGE =
    -   Set DENYWEBRENAME = [TWikiGuest](../Main/TWikiGuest){.twikiLink}
    -   Set ALLOWWEBRENAME =

<!-- -->

-   Users or groups allowed to change or rename this
    [WebPreferences](WebPreferences){.twikiLink} topic: (I.e.
    [TWikiAdminGroup](../Main/TWikiAdminGroup){.twikiLink})
    -   Set ALLOWTOPICCHANGE =
        [TWikiAdminGroup](../Main/TWikiAdminGroup){.twikiLink}
        [RobVermaas](../Main/RobVermaas){.twikiLink}
    -   Set ALLOWTOPICRENAME =
        [TWikiAdminGroup](../Main/TWikiAdminGroup){.twikiLink}
        [RobVermaas](../Main/RobVermaas){.twikiLink}

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
    -   When you write variable `#EEEEAA` , it gets expanded to
        `#EEEEAA` .
-   The sequential order of the preference settings is significant.
    Define preferences that use other preferences first, i.e. set
    `WEBCOPYRIGHT` before `WIKIWEBMASTER` since =Copyright © 1999-2018
    by the contributing authors.

All material on this collaboration platform is the property of the
contributing authors.\
Ideas, requests, problems regarding TWiki? [Send
feedback](mailto:webmaster@strategoxt.org?subject=TWiki%20Feedback%20on%20Octave.WebPreferences)=
uses the `webmaster@strategoxt.org` variable.

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

<!-- -->

-   Set SKIN = bluebox

<!-- -->

-   Set OCTAVELINK = [Octave](http://www.octave.org)
:::
:::
:::

::: {#sidebar}
::: {.box}
::: {.box2}
[Home](WebHome){.twikiLink} {#home .sidebar-title}
---------------------------

-   [About](AboutOctaveCompiler){.twikiLink}
-   [News](OctaveCompilerNews){.twikiLink}
-   [Documentation](OctaveCompilerDocumentation){.twikiLink}
-   [Bugs](https://catamaran.labs.cs.uu.nl/jira/browse/OCT)
-   [Download](OctaveCompilerDownload){.twikiLink}

\
\
:::
:::
:::

::: {#footer}
<div>

<div>

------------------------------------------------------------------------

[search](WebSearch){.twikiLink} \| [index](WebIndex){.twikiLink} \|
[recent changes](WebChanges){.twikiLink} \|
[statistics](WebStatistics){.twikiLink}    
[printable](http://www.program-transformation.org/view/Octave/WebPreferences?skin=print)
\|
[refresh](http://www.program-transformation.org/fresh/Octave/WebPreferences)
\|
[edit](http://www.program-transformation.org/edit/Octave/WebPreferences?t=1536826804)
\|
[history](http://www.program-transformation.org/rdiff/Octave/WebPreferences)
\| [more
actions](http://www.program-transformation.org/oops/Octave/WebPreferences?template=oopsmore&param1=1.5&param2=1.5)

</div>

</div>
:::
:::
