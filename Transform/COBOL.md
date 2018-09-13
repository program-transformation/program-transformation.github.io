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
    Page](http://www.program-transformation.org/edit/Transform/COBOL?t=1536825469)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/COBOL)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/COBOL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/COBOL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/COBOL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Transform/COBOL?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Transform/COBOL?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Transform/COBOL?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/COBOL?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/COBOL?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/COBOL?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/COBOL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/COBOL?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Transform/COBOL?template=oopsmore&param1=1.8&param2=1.8)
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
COBOL {#cobol .twikiTopicTitle}
=====

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[COBOL](COBOL){.twikiLink} stands for Common Business Oriented Language
and is considered by many as a legacy language. It was designed by the
CODASYL committee in 1957 and is the second oldest third generation
language.

The idea behind [COBOL](COBOL){.twikiLink} is that even managers can
read the code, to be able to prevent programmers from writing *bad code*
(as in: programs that transfer interest roundoff \'errors\' to their own
account). [COBOL](COBOL){.twikiLink} stems from the age of punch cards,
which is why the syntax is highly restricted.

-   columns 1-6: line number
-   column 7: line continuation or empty
-   columns 8-11: division, section and paragraph labels
-   columns 12-72: code
-   columns 73-80: comments

Commands can\'t be longer then 61 characters, or they must be continued
using a \\ character in column 72. Only capital letters can be used.
Some characters in the ASCII range 0-32 are normal characters for
[COBOL](COBOL){.twikiLink}, which presents some problems for
contemporary systems, because they use these characters for control
codes.

A lot of legacy code is written in [COBOL](COBOL){.twikiLink}. Most
programs used today are in [COBOL](COBOL){.twikiLink}. The impossibility
to port all these programs to nowadays more common (more concise and
better maintainable) languages gave rise to many projects that aim at
automatic improvement of [COBOL](COBOL){.twikiLink} programs.

------------------------------------------------------------------------

Cobol documentation and grammars at:

-   <http://publibz.boulder.ibm.com/cgi-bin/bookmgr_OS390/BOOKS/IGYR1101/CCONTENTS>
-   The [GrammarBase](../Sdf/GrammarBase){.twikiLink}
-   <http://www.cs.vu.nl/grammars/>

See <http://www.itl.nist.gov/div897/ctg/cobol_form.htm> for a test suite
for Cobol-85 processors.

------------------------------------------------------------------------

Tools for transforming [COBOL](COBOL){.twikiLink}:

-   [DMSSoftwareReengineeringToolkit](DMSSoftwareReengineeringToolkit){.twikiLink}
-   [CobolX](../Stratego/CobolX){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
