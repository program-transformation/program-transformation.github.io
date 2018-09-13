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
    Page](http://www.program-transformation.org/edit/Transform/NeliacDecompiler?t=1536826521)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/NeliacDecompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/NeliacDecompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/NeliacDecompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/NeliacDecompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Transform/NeliacDecompiler?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/NeliacDecompiler?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/NeliacDecompiler?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/NeliacDecompiler?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/NeliacDecompiler?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/NeliacDecompiler?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/NeliacDecompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/NeliacDecompiler?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Transform/NeliacDecompiler?template=oopsmore&param1=1.5&param2=1.5)
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
Neliac Decompiler {#neliac-decompiler .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Tom Moran wrote:

-   A working decompiler for
    [NELIAC](http://cuiwww.unige.ch/cgi-bin/langlist?isindex=NELIAC&style=dl),
    an Algol 58 derivative language not too unlike C, is described
    (including source listing) in Appendix D in \"Machine-Independent
    Computer Programming\" by Maurice H. Halstead, copyright 1962 and
    undoubtedly long out of print. It cites a Navy Electronics
    Laboratory Technical Memorandum \#427 by Joel Donnelly which might
    conceivably still be available.

<!-- -->

-   Halstead saw a decompiler as useful for 1) understanding/modifying a
    program to which you no longer had source code, and 2) porting such
    a program to a new machine by decompiling it and then recompiling
    for the new machine.

Tom Moran\'s first project, as a summer student worker and novice
programmer, was to assist Joel Donnelly with porting this decompiler to
the CDC 1604.

Anecdotes by [Bill Caudle](http://home.att.net/~caudle/careerto.htm) on
his work with [Maurice Halstead](FatherOfDecompilation){.twikiLink}
(1962-1978).

------------------------------------------------------------------------

NELIAC stands for Navy Electronics Laboratory International ALGOL
Compiler. So it really is supposed to be recognisably Algol.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 04 Feb 2005

------------------------------------------------------------------------

The following is from the book:

    Maurice H. Halstead,
    "Machine-Independent Computer Programming"
    Spartan Books,
    Washington DC 1962.

Note how programs are displayed in octal, not even indisassembled form.

### []{#Decompiling_with_D_Neliac} Decompiling with D-Neliac

For several years it has been apparent that those computer programs
written in machine-dependent languages represented large investments in
time which were lost whenever a change in computers was required. Even
though a change to a machine-independent language was made, all programs
written before the change still require complete rewriting if they are
to remain in use.

If, however, such programs could be computer-converted to the Neliac
language, then they would be in a form adaptable to recompilation upon
any other computer having a Neliac compiler. Furthermore, if the
translator were to be capable of accepting the machine-language programs
of a given computer as input, then it would not matter whether the
program had originally been written in machine language, in an assembly
system, or any possible problem-oriented compiler system.

While it would be premature to infer that this objective can be met with
complete satisfaction, the Donnelly D-Neliac system \[15\] as as
produced by J. K. Donnelly and Herman Englander has already established
that such an approach is highly feasible, and preliminary versions now
exist for both the Remington Rand Univac M-460 Countess computer and for
the Control Data Corporation 1604 computer. A recent version of the
former is given in complete detail in Appendix D.

To understand the workings of a decompiler, consider the following case,
in which Example 69 shows the source material, a machine-language
version of a program which has been written, tested, and rendered
operational on the M-460 Countess.

\[15\] J. K. Donnelly, \"A Decompiler for the Countess Computer,\" *Navy
Electronics Laboratory Technical Memorandum 427* , Sept., 1960.

Click [here for Example 69](DNeliacExample69){.twikiLink}.

As can be seen from a study of Appendix D, in the event that a
machine-language combination is encountered for which no decompilation
instructions have been written it can still convert them to the Neliac
machine-language form, and then continue. Strangely enough, working with
decompilers has emphasized one of the limitations in the bit-handling
capabilities of the Neliac language. This limitation consists of the
inability to specify any but contiguous bits in a part word, a feature
sometimes used in masking for logical operations.

In addition to its primary mission of translating non-Neliac programs
into the Neliac language, D-Neliac has also proved useful in another
way. This secondary use has been in the area of error detection. Since a
program will appear in different words, and with several of the details
handled differently if it is decompiled after having been compiled, the
paraphrased version is sometimes helpful in the detection of errors in
logic. A classic example is a case in which an occasionally used
regression-analysis program was found to fault in certain circumstances.
Since the program had originally been coded in machine language by a
mathematician no longer available, the fault was so subtle that it had
not been found, even after considerable searching. Upon decompilation,
however, it was immediately apparent that a misuse of an index occasion-
ally occurred.

A final pair of examples will show the decompilation of one of the
utility routines long in use on the Countess for loading flexo- writer
coded punched tape. This particular routine calls upon other subroutines
outside the area being decompiled, so that while the decompiler named
them, it obviously could record only their locations, and not their
contents. The numerical values for the Flexowriter codes in Table III
correspond with results in this case, too, of course. The first example
shows the raw program as fed to the D-Neliac program, the second shows
the Neliac program which it produced, while the third shows the Name
List which it also furnished.

Click [here for Example 72](DNeliacExample72){.twikiLink}.

Click [here for the Univac M460](UnivacM460){.twikiLink} instruction
set.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
