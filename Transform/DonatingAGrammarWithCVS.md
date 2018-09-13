::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/DonatingAGrammarWithCVS?t=1536826472)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DonatingAGrammarWithCVS)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DonatingAGrammarWithCVS)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DonatingAGrammarWithCVS?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DonatingAGrammarWithCVS?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/DonatingAGrammarWithCVS?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DonatingAGrammarWithCVS)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DonatingAGrammarWithCVS?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/DonatingAGrammarWithCVS?template=oopsmore&param1=1.1&param2=1.1)
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
Donating AGrammar With [CVS](CVS){.twikiLink} {#donating-agrammar-with-cvs .twikiTopicTitle}
=============================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Description**

This page describes how to donate your grammar to the
[GrammarBase[^?^](http://www.program-transformation.org/edit/Transform/GrammarBase?topicparent=Transform.DonatingAGrammarWithCVS)]{.twikiNewLink
style="background : #FFFFCE;"} by adding it to the central
[CVS](CVS){.twikiLink} repository. It requires write permission the the
[GrammarBase[^?^](http://www.program-transformation.org/edit/Transform/GrammarBase?topicparent=Transform.DonatingAGrammarWithCVS)]{.twikiNewLink
style="background : #FFFFCE;"} source repository.

**Donating with [CVS](CVS){.twikiLink}**

*Since the
[GrammarBase[^?^](http://www.program-transformation.org/edit/Transform/GrammarBase?topicparent=Transform.DonatingAGrammarWithCVS)]{.twikiNewLink
style="background : #FFFFCE;"} is
[FreeSoftware](FreeSoftware){.twikiLink}, you should accept that after
donating, your grammar becomes [FreeSoftware](FreeSoftware){.twikiLink}
as well.*

To add a grammar \'\<g\>\' with version \'\<v\>\' to the
[GrammarBase[^?^](http://www.program-transformation.org/edit/Transform/GrammarBase?topicparent=Transform.DonatingAGrammarWithCVS)]{.twikiNewLink
style="background : #FFFFCE;"} repository you should do the following:

: **1.** Add the directories grammars/\<g\>.\<v\> and
grammars/\<g\>.\<v\>/data to the repository: cvs add
grammars/\<g\>.\<v\> cvs add grammars/\<g\>.\<v\>/data

: **2.** Add all required files to the [CVS](CVS){.twikiLink}
repository: cd grammars/\<g\>.\<v\> cvs add Makefile.am \<g\>.spec
README.src \*.sdf cd data cvs add Makefile.am \*.\<suffix\>

: Here \*.\<suffix\> denotes all files with the suffix as defined for
the grammar in \<g\>.spec.

: **3.** Commit all changes to the central [CVS](CVS){.twikiLink}
repository: cvs commit

**See Also**

[AddingAGrammarToGB[^?^](http://www.program-transformation.org/edit/Transform/AddingAGrammarToGB?topicparent=Transform.DonatingAGrammarWithCVS)]{.twikiNewLink
style="background : #FFFFCE;"},
[FreeSoftware](FreeSoftware){.twikiLink},
[GrammarSpecFiles[^?^](http://www.program-transformation.org/edit/Transform/GrammarSpecFiles?topicparent=Transform.DonatingAGrammarWithCVS)]{.twikiNewLink
style="background : #FFFFCE;"}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
