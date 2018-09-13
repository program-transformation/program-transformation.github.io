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
    Page](http://www.program-transformation.org/edit/Transform/DecompDecompiler?t=1536826455)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompDecompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompDecompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompDecompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompDecompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompDecompiler?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompDecompiler?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompDecompiler?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompDecompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompDecompiler?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompDecompiler?template=oopsmore&param1=1.2&param2=1.2)
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
Decomp Decompiler {#decomp-decompiler .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

*This information is pieced together from a few sources. I hope it is
still accurate.*

In about 1985, Jim Reuter wrote decomp, a decompiler for the Vax BSD 4.2
(a.out format) which took as input object files with symbolic
information and produced C-like programs. The nature of this decompiler
was to port the Empire game to the VMS environment, given that source
code was not available. The decompiler was freely available on the
Internet from <ftp://ftp.cs.washington.edu/pub/decomp.tar.Z> . Since
that is no longer available, I have attached a copy below.

Decomp worked only on object (.o or .obj) files, and made use of the
symbol table information present in these files to find the entry points
to functions, determine data used in the program, and the names of that
data. Subroutines were decompiled one at a time, in the following way: a
control flow graph of basic blocks was built and optimised by the
removal of arcs leading to intermediate unconditional branches. Control
flow analysis was performed in the graph to find high-level control
constructs, converting the control flow graph into a tree of generic
constructs. The algorithm used by this analysis was taken from the
struct program, a program that structures graphs produced by Fortran
programs, which was based on the structuring algorithm described by
B.Baker in \[
[Bake77](HistoryOfDecompilation2#RefBake77){.twikiAnchorLink} \].
Finally, the generic constructs in the tree were converted to C-specific
constructs, and code was generated. The final output programs required
manual modifications to place the arguments on the procedure\'s argument
list, and determine that a subroutine returned a value (i.e. was a
function). This decompiler was written in about 5 man-months \[
[Reut91](HistoryOfDecompilation2#RefReut91){.twikiAnchorLink} \].

*Sample programs were written and compiled in C in a Vax BSD 4.2
machine. The resulting C programs are not compilable, and require some
hand editing. The programs have the correct control structures, due to
the structuring algorithm implemented, and the right data type of
variables, due to the embedded symbol table in the object code. The
names of library routines and procedures, and the user\'s program entry
point are also known from the symbol table; therefore, no extraneous
procedures (e.g. compiler start up code, library routines) are
decompiled. The need for a data flow analysis stage is vital, though, as
neither expressions, actual arguments, nor function return value are
determined. An interprocedural data flow analysis would eliminate much
of the hand-editing required to recompile the output programs.*

You can read his [DecompReadMe](DecompReadMe){.twikiLink} file for more
information.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiAttachments}
  [I](DecompDecompiler@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Attachment](../TWiki/FileAttachment){.twikiLink} [![sort](../pub/TWiki/TablePlugin/diamond.gif)](DecompDecompiler@sortcol=1&table=1&up=0#sorted_table "Sort by this column")   [Action](DecompDecompiler@sortcol=2&table=1&up=0#sorted_table "Sort by this column")                                                                                        [Size](DecompDecompiler@sortcol=3&table=1&up=0#sorted_table "Sort by this column") [Date](DecompDecompiler@sortcol=4&table=1&up=0#sorted_table "Sort by this column")   [Who](DecompDecompiler@sortcol=5&table=1&up=0#sorted_table "Sort by this column")   [Comment](DecompDecompiler@sortcol=6&table=1&up=0#sorted_table "Sort by this column")
  --------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------ ------------------------------------------------------------------------------------ ----------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------
  ![](../pub/icn/zip.gif){width="16" height="16"}                                   [decomp.tar.Z](../pub/Transform/DecompDecompiler/decomp.tar.Z)                                                                                                                  [manage](http://www.program-transformation.org/attach/Transform/DecompDecompiler?filename=decomp.tar.Z&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                 71.9 K 04 Dec 2004 - 08:52                                                                  [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}                                 
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
