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
    Page](http://www.program-transformation.org/edit/Transform/FalkeDiplomaSummary?t=1536826480)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/FalkeDiplomaSummary)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/FalkeDiplomaSummary)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/FalkeDiplomaSummary?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/FalkeDiplomaSummary?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/FalkeDiplomaSummary?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/FalkeDiplomaSummary?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/FalkeDiplomaSummary?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/FalkeDiplomaSummary)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/FalkeDiplomaSummary?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/FalkeDiplomaSummary?template=oopsmore&param1=1.2&param2=1.2)
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
Falke Diploma Summary {#falke-diploma-summary .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Raimar Falke\'s [Diploma Thesis](http://risimo.net/diplom.ps) is written
in German. For English readers, I have translated the final section
using [Google\'s translation
facility](http://translate.google.com/translate_t) and some hand
editing.

It strikes me that natural language translation is at a somewhat
equivalent stage as decompilation: automatic translators exist, and you
can get a sense of the original text, sometimes clearly, at other times
quite muddled. Often hand editing is required to produce a clean
translation. The automatic translator is useful despite its low quality,
because at least initially, you have very little idea of what the input
text means.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 13 Jan 2005

[]{#5_Summary_and_Conclusion} 5 Summary and Conclusion
------------------------------------------------------

In this paper a type analysis system for a decompiler was presented.
Characteristics were defined, which contain all type-relevant
information about the examined program. Furthermore a multitude of
possibilities of the user were modelled for influencing the type
analysis. The presented type system supports the complex types array,
struct and sum types in addition to integers and pointers. Sum types are
used to model conflicts. The presented methods for the recognition of
arrays work for all compiler optimizations except two (loop unrolling
and loop collapsing).

Multidimensional array types, classes, floating-point numbers, 64-Bit
integers, enumerated types and bit fields were not considered in this
paper. These types offer challenges for the future. A procedure which
measures the quality of the extraction of type-relevant information and
the type reconstruction, would also be useful. Without this, one cannot
formally measure the quality of a type analysis. A graphical interface
for the input of the user instructions would simplify the use of the
decompiler.

With the help of clone detection, it would be possible to recognise
compiler optimisations such as loop unrolling, and also improve
statements relating to array parameters. As became evident, aliases
limit the decompiler in many ways. This can be improved by the
employment of an alias analysis component. Compilers usually include
additional information for debugging in the examined program. Using
these information is a also possible task. Harmful programs such as
worms and viruses are partially polymorphic, i.e. they change their form
(e.g. the sequence of assembler instructions) during their propagation.
It would be interesting to find out to what extent these transformations
are still visible after decompilation.

------------------------------------------------------------------------

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
