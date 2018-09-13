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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationPossible?t=1536826288)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationPossible)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationPossible)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationPossible?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationPossible?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    13](http://www.program-transformation.org/view/Transform/DecompilationPossible?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Transform/DecompilationPossible?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Transform/DecompilationPossible?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Transform/DecompilationPossible?rev1=1.12&rev2=1.11)
-   [Rev
    11](http://www.program-transformation.org/view/Transform/DecompilationPossible?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Transform/DecompilationPossible?rev1=1.11&rev2=1.10)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationPossible)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationPossible?template=oopsmore&param1=1.13&param2=1.13)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationPossible?template=oopsmore&param1=1.13&param2=1.13)
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
Decompilation Possible {#decompilation-possible .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Is_Decompilation_Possible}[]{#Is_Decompilation_Possible_} Is Decompilation Possible?
----------------------------------------------------------------------------------------

Almost every week requests for decompilation programs are made in
newsgroups (like [comp.lang.c](news:comp.lang.c)), and these are usually
replied with: It is not possible! People claim that decompilation is
similar to converting a hamburger back into a cow, or unscrambling an
omelette back to an egg. Here is a typical FAQ entry from
[C++-FAQ-Lite](http://www.parashift.com/c++-faq-lite/compiler-dependencies.html#faq-38.4),
and my [refutation](DecompilationFaqRefutation){.twikiLink} of it. Also
[BobStoutOnDecompilation](BobStoutOnDecompilation){.twikiLink} and its
[refutation](BobStoutRefutation){.twikiLink}. People even write [tech
report](http://citeseer.nj.nec.com/weide94reverse.html)s on the subject.
They are far from the truth.

![pigsFromSausages.jpg](../pub/Transform/DecompilationPossible/pigsFromSausages.jpg){width="700"
height="316"}

Certainly, fully automated decompilation of arbitrary machine-code
programs is not possible \-- this problem is theoretically equivalent to
the Halting Problem, an undecidable problem in Computer Science. What
this means is that automatic (no expert intervention) decompilation
cannot be achieved for all possible programs that are ever written.
Further, even if a certain degree of success is achieved, the
automatically generated program will probably lack meaningful variable
and function names as these are not normally stored in an executable
file (except when stored for debugging purposes).

However, many useful algorithms have this sort of theoretical
limitation. It is not possible to write a computer program that can
perfectly route any arbitrary printed circuit board automatically.
However, the best ones do a good job that can be improved with some
expert intervention. They save an enormous amount of work. Similarly, it
is not possible in general to solve problems as simple as the travelling
salesman problem. Despite this, salesmen continue to travel! The
interesting question is not \"can we decompile arbitrary machine code
programs?\", because the answer is no. The interesting question is
rather \"what proportion of real-world programs can be decompiled to
source code that is useful for various purposes?\". The answer to this
question is very much open at this point.

#### []{#Disassembling} Disassembling

Some people believe it is only possible to disassemble a machine code
program (recover the assembly sources; this in itself is not a trivial
problem), again, due to its equivalence to the Halting Problem. However,
in practice, there have been approaches to deal with disassembly and
decompilation. The more successful ones to date make use of extra
information (e.g. knowledge of the compiler used) or require human input
at the hard parts of the disassembly process.

It may even be possible for a decompiler to automatically (i.e. with no
human input) decompile a large fraction of real-world machine code
programs. [MikeVanEmmerik](MikeVanEmmerik){.twikiLink} has shown in his
[confirmation
report](http://www.itee.uq.edu.au/~emmerik/confirmation.html) that a
machine code disassembler (recover assembly language) has three
fundamental problems to solve, while a machine code decompiler (recover
high-level language) has seven such problems. Both require the
separation of code and data, and of pointers and constants. In effect,
decompilation is \"merely\" an extension of disassembly. If you can
produce assembly language source for a program, then you can produce
high-level language source for that program with more effort.

Note that producing assembly language source for a program is a lot
harder than just running a dumb disassembler over the machine code.
Compare saving the result from running the tool `objdump -d` (a dumb
disassembler) to running a sophisticated disassembler sich as `IDA Pro`
(an interactive disassembler), taking weeks to manually separate the
code and data, adding meaningful names, comments, etc.

It is interesting to note that the authors of [IDA
Pro](http://www.datarescue.com/idabase) do not guarantee reassembly of
the output from IDA Pro, or even believe that this is a good goal for
their tool. (Source: mainly J. C. Roberts\' comments in [this General
IDA Pro
Forum](http://www.datarescue.com/ubb/ultimatebb.php?ubb=get_topic;f=1;t=000429)
titled \"How do I translate EXE-\>ASM-\>EXE with IDA Pro?\"). There are
some technical issues like \"what do you do with Delphi forms\" and
other resources; I simply dismiss these other objects as not being part
of the source code. (You still need them to generate an equivalent
program, but there are resource rippers and other programs to perform
that task.) However, they seem to have resigned themselves to the fact
that reassembling programs disassembled with IDA Pro is just too
difficult for most people, and it would be too much work to support this
activity, so they officially discourage it.

#### []{#The_processor} The processor

Still skeptical? Consider that the processor, by executing the machine
language program, can successfully figure out what to do with any input,
to create the correct output. A machine code program is a set of
instructions, plus a set of data bytes. Each machine code instruction
has semantics - you can define precisely what each instruction does. A
high-level language is more abstract than a machine code program -
details (such as individual instructions, registers, and so on) are
abstracted away. In a way, decompilation is the judicious deleting of
unneeded information. Those individual machine semantics can be
represented in an intermediate form - that\'s what the front end of a
decompiler does. This internal representation is already a decompilation
of sorts - it is a representation of the input program. A series of
transformations can remove the machine specific aspects of the program
semantics. A technique called propagation (forward substitution) can
aggregate the individual semantics into more complex expressions. Unused
assignments can be removed. Machine code features such as individual
registers disappear with this aggregation. Finally, the intermediate
representation can be structured, replacing jump instructions with loops
and conditionals. Structuiring is a graph transformation, and is well
understood. Although the details are quite tricky, there are no
theoretical issues with this phase.

#### []{#Commercial_example} Commercial example

Perhaps the final proof is in the doing.
[Boomerang](http://boomerang.sourceforge.net) (an open source
decompiler) has already been used as an aid in real-world decompilation;
see [What Boomerang has
done](http://boomerang.sourceforge.net/cando.html#hasdone). Granted,
this was a special case, where the client already had some (out dated
and incomplete) source code, and Boomerang was not yet then capable of
doing much without a great deal of hand editing. Nevertheless, it was
useful, and gave a glimpse of a time when decompilers may well become an
indispensable tool for binary reverse engineering work.

#### []{#Results} Results

-   A [good
    example](http://www.itee.uq.edu.au/~cristina/dcc.html#example) of
    actual decompiling of X86 machine code to C is given on the [dcc
    home page](http://www.itee.uq.edu.au/~cristina/dcc.html).
-   Read [what Boomerang can
    do](http://boomerang.sourceforge.net/cando.html).
-   [FermaT](FermaT){.twikiLink}, by [Software Migrations
    Ltd](http://www.smltd.com), is an industrial strength program
    transformation system used to [migrate IBM 370 Assembler
    modules](http://www.smltd.com/migration.htm) into equivalent
    readable and maintainable [COBOL](COBOL){.twikiLink} programs.
-   [FermaT](FermaT){.twikiLink} was also used to help solve the year
    2000 problem for IBM 370 Assembler code.
-   You can read the paper \"[Pigs from Sausages? Reengineering from
    Assembler to C via FermaT
    Transformations](http://www.dur.ac.uk/martin.ward/martin/papers/migration-t.pdf)\"
    (306KB, 36pp), which reports how over half a million lines of
    assembler code (OK, not binary code) were translated automatically
    into maintainable C code.
-   And of course, most people have heard of Java bytecode decompilers
    (see [JavaDecompilers](JavaDecompilers){.twikiLink}). The best of
    these are very successful, even typing local variables correctly.

------------------------------------------------------------------------

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.DecompilationPossible moved from
Transform.DeCompilationPossible on 13 Feb 2003 - 21:54 by
[MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/DecompilationPossible?newweb=Transform&newtopic=DeCompilationPossible&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
