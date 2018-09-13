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
    Page](http://www.program-transformation.org/edit/Transform/PilerSystem?t=1536826534)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/PilerSystem)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/PilerSystem)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/PilerSystem?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/PilerSystem?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/PilerSystem?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/PilerSystem?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/PilerSystem?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/PilerSystem)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/PilerSystem?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/PilerSystem?template=oopsmore&param1=1.2&param2=1.2)
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
Piler System {#piler-system .twikiTopicTitle}
============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#The_PILER_Decompilation_System} The PILER Decompilation System
==================================================================

::: {.twikiToc}
-   [The PILER Decompilation
    System](PilerSystem#The_PILER_Decompilation_System)
    -   [The \"interpreter\" phase](PilerSystem#The_interpreter_phase)
    -   [Micro Form](PilerSystem#Micro_Form)
    -   [The analyser phase](PilerSystem#The_analyser_phase)
    -   [Intermediate Form](PilerSystem#Intermediate_Form)
    -   [The Converter phase](PilerSystem#The_Converter_phase)
    -   [Conclusion](PilerSystem#Conclusion)
:::

The PILER decompilation system is documented in \[
[Barb74](http://www.program-transformation.org/twiki/bin/view/Transform/HistoryOfDecompilation1#RefBarb74)
\]. However, this document is probably only available in Microfiche
form, and would be difficult for many to access. As the first attempt at
a general decompiler, I thought it was worth summarising in a little
more detail.

The PILER decompiler system follows (almost) the classic three phase
structure:

-   Interpretation of the subject (input) program\'s \"commands\" (the
    Interpreter)
-   Analysis of the source program for function and data usage (the
    Analyser)
-   Expression of the source program in the target language (the
    Converter)

Each of these phases is a totally separate program, and could be run on
three different machines! The interpreter phase was always run on the
source machine.

![Piler.png](../pub/Transform/PilerSystem/Piler.png)

A reproduction of Figure 2 of \[Barb74\], complete with upper case text.

[]{#The_interpreter_phase} The \"interpreter\" phase
----------------------------------------------------

The \"interpreter\" phase (not a program interpreter as we would use the
term now) ran on the source machine, and has the input program loaded
with it (just insert the cards into the deck!). The interpreter
therefore used the loader and operating system of the source machine.
The output of this phase (the first intermediate representation) was
called Micro Form. This was supposed to be general, but reflected the
narrow variety of machines at that time. Instead of making this a clean
interface, they decided that Micro Form could be in any form that was
convenient for the interpreter phase, as long as the subroutine RMR
(Read Microform Record) in the Analyser phase could read it.

The interpreter phase had three subphases: loader, analysis (not the
same as the analysis phase; this subphase just attempts to separate code
from data), and interpretation. The analysis subphase generated several
data structures: a memory map, symbol table, subroutine table, data
reference table, and an input/output buffer table. It seems that the
opcode field was often used to decide if a word was instruction, data,
or I/O control. \"Secondary microforms\" were appended for indexed
instructions and the like.

[]{#Micro_Form} Micro Form
--------------------------

Microform was the low level intermediate representation. It was 3
address.

[]{#The_analyser_phase} The analyser phase
------------------------------------------

This phase could be run on any computer, not necessarily the source or
target machines. The basic procedures were (from \[Barb74\]):

-   First level analysis. Memory mapping for separation of program
    instructions and data. Division of program into logical blocks.
    Preliminary \"timing analysis\". Flagging of indexed or modified
    branch addresses and operation codes. Subroutine analysis.

<!-- -->

-   Data analysis. Historical use of data locations and registers.
    Formats of data.

<!-- -->

-   Second level analysis. Analysis of modified addresses and operation
    codes and completion of first level analysis and data analysis for
    any additional segments. Program reduction.

<!-- -->

-   \"Timing analysis\". Assignments of computational priorities based
    on data usage requirements.

<!-- -->

-   Third level analysis. Reduction of program to functional level,
    rather than instructive level.

<!-- -->

-   Preparation of flowchart blocks.

<!-- -->

-   Preparation of Intermediate Form subject program.

The folowing programs were part of the analyser phase:

-   Reader (contains the Read Microform Record (RMR) subroutine)
-   Data handler
-   Analyser
-   Flow charter
-   Program modifier (accepts directives from the user to modify the
    subject program).

The Reader was overlaid by the analyser. Its job was to read the
Mircoform.

Some of the analyses included jump elimination and crude loop analysis.
\"Register usage analysis\" seems to have been a crude form of dataflow
analysis, but pattern based! There were 9 patterns (somewhat high level,
e.g. any load followed by another load to the same register). Most
patterns seemed to be aimed at removing registers from the intermediate
form. (Those not removed were assigned \"pseudo memory locations\".)

In summary, the analyses were not very general, but with the simple
machines of the day, they seemed to get away with it.

The \"timing analysis\" does not appear to be associated with the
execution time of instructions, but more about sequence of uses of data.
Perhaps it was to do with splitting live ranges, or to somehow cope with
self modifying code. It seems to have been associated with the
\"precedence hierarchy\" of logical blocks (basic blocks), to \"free the
program from programmer- and hardware- dictated arbitrariness\", and to
\"locate elements which depend on their relative position in the program
flow for their content or meaning\".

The intermediate form has such high level concepts as indexes (indexed
variables, such as arrays). However, it falls short of structuring
actual DO (etc) loops (which is the job of the Converter).

The Data Handler seems to have been an internal housekeeping program,
handling the details of overlapped I/O, look-ahead, \"re-linking\"
records after a deletion or insertion, and so on.

It was possible to make changes to the program by \"modifying\" the
flowchart (the Program Modifier). This was achieved with commands (input
on punched cards); the following is a subset:

SELECT [Block Identifier]{.underline}.

INSERT [BLock Identifier]{.underline} IN PATH ***\_\_***.

EXIT PATH ***\_\_*** TO [Block Identifier]{.underline}.

DATA [Flow chart symbol]{.underline},[Size]{.underline},[Data
Block]{.underline}.

If the inserted block was a subroutine: RETURN PATH ***\_*** TO [Block
Identifier]{.underline}. (Subroutines seemed to have multiple exits in
those days.)

DELETE [Block Identifier]{.underline}.

DELETE PATH ***\_\_***.

Flow chart modification affected only the intermediate form.

[]{#Intermediate_Form} Intermediate Form
----------------------------------------

Intermediate Form is the high level intermediate representation. It was
designed with the following languages as likely targets: FORTRAN,
[COBOL](COBOL){.twikiLink}, ALGOL, JOVIAL, and PL/1. To give a flavour,
here are some of the codes:

[Mathematical Symbols]{.underline}

    001  Plus                010  Reciprocal
    002  Minus               011  Exponent
    003  Unary minus         012  Boolean OR
    004  Inverse subtract    013          AND
    005  Multiply            014          EXTRACT
    006  Divide              015          EXCLUSIVE OR
    007  Inverse divide      016          EQUIVALENT
    020  Equals              017          CONDITIONAL

[Internal Functions]{.underline}

    140 I/O      Subfields
                 01  Test        10  Input
                 02  Position    20  Close
                 04  Output      40  Open

    040  Round               050  Modulo
    041  Normalise           051  Remainder
    042  Adjoin              052  Absolute value
    043  Largest integer     053  Set ON (-,1)
    044  Smallest integer    054  Set OFF (+,0)
    045  Maximum
    046  Minimum
    100  Test
    101  Compare             Subfield
    102  Search              01  Match
    103  Sort                02  Mismatch
    104  Enter               03  Max value in array
    105  Move                04  Min value in array
                             05  Greater than comparand
                             06  Greater or equal to comparand
                             07  Less or equal to comparand
                             10  Between limits of 2 comparands
                             11  Next lower than comparand
                             12  Next higher than comparand
    120 Internal procedure
    130 External procedure

Operand types:

    01    Constant
    02    Literal
    04    Variable
    05    Subscripted variable
    06    Subscript
    10    Function
    11-16 Parameters as 01-06 above
    20    I/O list
    30    Format list

[]{#The_Converter_phase} The Converter phase
--------------------------------------------

This phase wrote the high level language. Apparently there were so many
dialects of [COBOL](COBOL){.twikiLink} in those days, that they
suggested that the Converter should handle all the variations. They
wrote \"skeletal converters\" for FORTRAN and [COBOL](COBOL){.twikiLink}
(they claim that most of their effort was spent on the analysis phase).

[]{#Conclusion} Conclusion
--------------------------

ALthough this appears to have been a genuine attempt at a flexible,
general system, it seems to have assumed many characteristics of
machines common in its day, but not common now. It is a real shame that
it was never properly finished (as far as I can tell), e.g. that more
interpreter phases were never written.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 07 Jul 2003

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
