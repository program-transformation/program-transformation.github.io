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
    Page](http://www.program-transformation.org/edit/Transform/Exec2cDecompiler?t=1536826477)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/Exec2cDecompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/Exec2cDecompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/Exec2cDecompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/Exec2cDecompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/Exec2cDecompiler?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/Exec2cDecompiler?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/Exec2cDecompiler?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/Exec2cDecompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/Exec2cDecompiler?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/Exec2cDecompiler?template=oopsmore&param1=1.2&param2=1.2)
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
Exec 2 c Decompiler {#exec-2-c-decompiler .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

A beta-release of the decompiler exec2c by Scott Guthery was distributed
to beta testers in 1991. The program is copyrighted by \`The Austin Code
Works and Polyglot International\':

        EXEC-2-C (e2c)
        As of 1991 in beta test
        (c)The Austin Code Works and Polyglot International.
        by guthery@acw.com (Scott Guthery )

This decompiler consist of three programs, which have to be called
sequentially, or you can use a menu-based driver program (envmnu.exe).
The first program is an automatic disassembler. The second program does
some intermediate analyses and generates the data part of the C file.
The third program generates the C-like code for the procedures,
basically by translating each assembly instruction into an equivalent
C-statement (i.e. making registers variables and emulating the stack).
Some recovery of high-level language control structures is done. The
C-output file is about three times as large as the assembly output file.

The programs have memory limits, imposed by the DOS environment (64Kb).
There are also some small bugs. Apparently, this project was only a
trial that was never finished. It was judged that a lot more work was
required to make it a useful tool.

Overall evaluation: This is a good first attempt, with a good front-end
(the disassembler).

An archive of the distribution is available below.

For tests, see [DecompilerE2cTest](DecompilerE2cTest){.twikiLink}.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiAttachments}
  [I](Exec2cDecompiler@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Attachment](../TWiki/FileAttachment){.twikiLink} [![sort](../pub/TWiki/TablePlugin/diamond.gif)](Exec2cDecompiler@sortcol=1&table=1&up=0#sorted_table "Sort by this column")   [Action](Exec2cDecompiler@sortcol=2&table=1&up=0#sorted_table "Sort by this column")                                                                                       [Size](Exec2cDecompiler@sortcol=3&table=1&up=0#sorted_table "Sort by this column") [Date](Exec2cDecompiler@sortcol=4&table=1&up=0#sorted_table "Sort by this column")   [Who](Exec2cDecompiler@sortcol=5&table=1&up=0#sorted_table "Sort by this column")   [Comment](Exec2cDecompiler@sortcol=6&table=1&up=0#sorted_table "Sort by this column")
  --------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ ------------------------------------------------------------------------------------ ------------------------------------------------------------------------------------ ----------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------
  ![](../pub/icn/zip.gif){width="16" height="16"}                                   [exe-2-c.zip](../pub/Transform/Exec2cDecompiler/exe-2-c.zip)                                                                                                                    [manage](http://www.program-transformation.org/attach/Transform/Exec2cDecompiler?filename=exe-2-c.zip&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                212.8 K 24 Jan 2003 - 07:51                                                                  [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}                                exe-2-C decompiler
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
