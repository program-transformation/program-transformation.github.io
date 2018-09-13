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
    Page](http://www.program-transformation.org/edit/Main/RssBase?t=1536827839)
-   [Rename
    Page](http://www.program-transformation.org/rename/Main/RssBase)
-   [Attach
    File](http://www.program-transformation.org/attach/Main/RssBase)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Main/RssBase?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Main/RssBase?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Main/RssBase?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Main/RssBase)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Main/RssBase?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Main/RssBase?template=oopsmore&param1=1.1&param2=1.1)
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
Rss Base {#rss-base .twikiTopicTitle}
========

::: {.twikiWebTitle}
Program-Transformation.Org
:::

    %STARTINCLUDE%  <dc:language>en-us</dc:language>
      <dc:rights>Copyright %GMTIME{"$year"}%, Contributing authors of Program-Transformation.Org.</dc:rights>
      <dc:publisher>Program-Transformation.Org</dc:publisher>
      <dc:creator>Program-Transformation.Org</dc:creator>
      <dc:source>TWiki</dc:source>
      <items>
             <rdf:Seq>
    %SEARCH{".*" web="%INCLUDINGWEB%" regex="on" nosearch="on" order="modified" reverse="on" nototal="on" limit="16" format="<rdf:li rdf:resource=\"http://www.program-transformation.org/$web/$topic\" />"}%
             </rdf:Seq>
      </items>
    </channel>
    %SEARCH{".*" web="%INCLUDINGWEB%" regex="on" nosearch="on" order="modified" reverse="on" nototal="on" limit="16" format="<item rdf:about=\"http://www.program-transformation.org/$web/$topic\">$n  <title>$topic</title>$n  <link>http://www.program-transformation.org/$web/$topic</link>$n  <description>$summary</description>$n  <dc:date>$isodate</dc:date>$n  <dc:contributor>$n     <rdf:Description link=\"%SCRIPTURL%/view%SCRIPTSUFFIX%?topic=$wikiusername\">$n                <rdf:value>$username</rdf:value>$n   </rdf:Description>$n  </dc:contributor>$n  <wiki:version>$rev</wiki:version>$n  <wiki:status>updated</wiki:status>$n  <wiki:importance>major</wiki:importance>$n  <wiki:diff>%SCRIPTURL%/rdiff%SCRIPTSUFFIX%/$web/$topic</wiki:diff>$n  <wiki:history>%SCRIPTURL%/rdiff%SCRIPTSUFFIX%/$web/$topic</wiki:history>$n</item>"}%
    %STOPINCLUDE%

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Main.RssBase moved from Main.OurRssBase on 09 May 2005 - 13:51 by
[MartinBravenboer](MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Main/RssBase?newweb=Main&newtopic=OurRssBase&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
