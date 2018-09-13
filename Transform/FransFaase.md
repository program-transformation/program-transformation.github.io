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
    Page](http://www.program-transformation.org/edit/Transform/FransFaase?t=1536826484)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/FransFaase)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/FransFaase)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/FransFaase?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/FransFaase?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/FransFaase?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/FransFaase)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/FransFaase?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/FransFaase?template=oopsmore&param1=1.1&param2=1.1)
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
Frans Faase {#frans-faase .twikiTopicTitle}
===========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This is my idea of how I would write a general decompiler:

1.  Lets assume, we start with the assembler output of the
    disassemblers, which already contain the proper labels. My idea
    would to read in the whole file into memory (no problem on a Linux
    box, I would say), and group instructions in blocks, based on the
    labels.
2.  Then I would decode each instruction in more primitive operations,
    in order to do away with all the different addressing modes. Most
    instructions only modify on register or memory location.
3.  From this, it should be possible to determine which are the
    registers read and written by each block (assuming that all memory
    locations refer to C-variables). Based on this we can do a flow
    analysis, in order to find out whether there are any register mapped
    variables.
4.  If this has be done, we can determine which are the expressions that
    are calculated by the instructions for each store to a variable
    (either register based or memory based). Normalisation of these
    expression might be needed.
5.  Further more we have to recognize the high-level statements that
    resulted in the block structure, and the jumps between them (which
    is described in: *Reverse Compilation Techniques*
    ([Cifuentes](CristinaCifuentes){.twikiLink} 1994) (download gzipped
    postscript file
    [here](http://www.program-transformation.org/twiki/bin/viewfile/Transform/CristinaCifuentes?rev=/sw/bin/rlog%20%20-h%20/users/www/staff/research/projects/stratego/twiki/pub/Transform/CristinaCifuentes/decompilation_thesis.ps.gz,v&filename=decompilation_thesis.ps.gz)).
    From this, we can start generating the code, which will only deal
    with operations on bytes, words, long words, and float (doubles).

For the reconstructing of the types, we first of all need type
resolution techniques, whenever parameters are passed in function calls,
or when they are assigned to each other. The way to do this is to assign
a unique type to each variable and parameter, and derive equivalence
rules. Problems are caused when in the original source type casts are
used. Also enumeration types, and other types, which are equivalent with
one of the standard types cannot be recovered.

The detection of array types and pointer types is not hard. Structured
types, especially when union\'s are used, pose extra problems.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
