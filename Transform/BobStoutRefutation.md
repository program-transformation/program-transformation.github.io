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
    Page](http://www.program-transformation.org/edit/Transform/BobStoutRefutation?t=1536826297)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/BobStoutRefutation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/BobStoutRefutation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/BobStoutRefutation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/BobStoutRefutation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/BobStoutRefutation?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/BobStoutRefutation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/BobStoutRefutation?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/BobStoutRefutation?template=oopsmore&param1=1.1&param2=1.1)
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
Bob Stout Refutation {#bob-stout-refutation .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This page is my refutation of a Frequently Asked Question answer on
decompilation. The original page is difficult to find now in its
complete form, so I have archived it
[here](BobStoutOnDecompilation){.twikiLink}. As with the other
[refutation page](DecompilationFaqRefutation){.twikiLink}, I sincerely
mean no disrespect to Bob Stout, Jeremy Coffin, or other commentators.
This sort of attitude to decompilation is unfortunately common.
Ultimately, the naysayers may be correct in a very broad sense, i.e. it
may be that machine code decompilers will never be easy enough to use to
become mainstream. However, they are wrong in many technical details, so
I\'ll use this opportunity to correct the facts. The reader can decide
whether machine code decompilation will eventually become useful to
them.

Text from the FAQ answer (the text I\'m refuting) will appear in red ;
my refutation will be in ordinary text.

G.3.17 decompil.txt

+++Date last modified: 05-Jul-1997

Question:

Is there any hope of a decompiler that would convert an executable
program into C/C++ code?

Answer:

Don\'t hold your breath. Think about it\... For a decompiler to work
properly, either 1) every compiler would have to generate substantially
identical code, even with full optimization turned on,

If you are expecting the original source code back, certainly that is
impossible. Even the original source code with comments removed and
generic variable and function names is impossible. But why demand the
original source code? Surely any equivalent source code will do just as
well. The more readable the source code, the better. It is conveivable
that a decompiler could produce source code that is more readable than
the original source code, if it was poorly written in the first place.

There are indeed many ways that compilers can express the semantics of a
source program; for correct compilations, all of these will be
equivalent. A correct decompiler will produce equivalent source code.
Very likely, the source code produced from an optimised version of a
program will be different from the source code generated from an
unoptimised binary file. Ironically, optimised binary code is easier to
deal with in some ways (e.g. less dead code to eliminate).

or 2) it would have to recognize the individual output of every
compiler\'s code generator.

You seem to be assuming that a decompiler has to \"reverse\" the
operation of the compiler. That is certainly one approach, but general
decompilers don\'t work with patterns in the compiled code. Instead,
they apply a series of program transformations. The original executable
file is a program, albeit one expressed in a binary, human unfriendly
language. Some transformations (e.g. recovering parameters) require
extensive analysis. Others, e.g. converting a goto statement into a
do-while loop, are very standard graph transformations that are
routinely applied to source code.

A few of these transformations will depend on patterns in the input
executable; these are \"idioms\". These are constructions where the
meaning is not readily derived from their semantics, e.g. using subtract
with carry to effect a min() or max() function. These are usually not
specific to a particular compiler or optimisation level, however.
(However you are more or less likely to see some of these at different
optimisation levels).

If the first case were to be correct, there would be no more need for
compiler benchmarks since every one would work the same.

Agreed. So that\'s not the case.

For the second case to be true would require in immensely complex
program that had to change with every new compiler release.

No, again, this is assuming that decompilers have to reverse the
operation of compilers, with each compiler and optimisation level as a
separate case.

OK, so what about specific decompilers for specific compilers - say a
decompiler designed to only work on code generated by, say, BC++ 4.52?
\...

Again, this is still making an invalid assumption.

OK, let\'s simplify further and specify that you only want to support
one specific compiler and you want to decompile to the most logical
source code without trying to interpret the optimization. What then?

You\'ve actually touched on a valid consideration here: what does the
\"most logical source code\" really mean? The shortest? The most
readable? The \"nicest\"? Without being able to measure the quality of
decompiled output, it\'s difficult to measure progress. You could also
look at it this way: any valid source code will do. Just use source to
source transformations (programmers do this all the time, they refactor
their code), add comments, rename variables and functions, until it is
as pretty as you need.

A good optimizer can and will substantially rewrite the internals of
your code, so what you get out of your decompiler will be, not only
cryptic, but in many cases, riddled with goto statements and other
no-no\'s of good coding practice. At this point, you have decompiled
source, but what good is it?

Again, a good point, but the details are incorrect. Certainly, optimised
machine code can be more difficult for a human to read (e.g. as a
disassembly), but that doesn\'t necessarily imply that my the time it is
decopiled it is any harder to read. A good decompiler will (without
specifically trying to do this) \"unoptimise\" the code. As a trivial
example, a subexpression kept in a register will be replace with the
original subexressions by expression propagation. The original
assignment to the register will disappear with dead code elimination.

As for gotos, that\'s a structuring issue. Structuring is a largely
solved problem. You can eliminate gotos in any code, including
unstructured code, at the cost of either code duplication or adding
booleans. The exact same thing applies at the source code level. Even
the worst spaghetti source code with gotos can be transformed into
something without gotos. In a few rare cases, it may be clearer to leave
a few gotos there. You can parameterise the structuring stage of a
decompiler to generate any of these three options (i.e. allow duplicate
code, generate booleans, or allow limited gotos to remain).

Code quality is very important, and quality can deteriorate for a
variety of reasons, but these aren\'t the right reasons. It is my (as
yet unproven) belief that reasonable quality code can be generated for
almost any program. You can of course always construct a program that
will defeat any particular decmpiler. Can that decompiler always be
modified to accept all existing accepted programs plus this constructed
one? I suspect so, but there are presumably an infinite number of
programs that could be constructed to break decmpilers, so there will
never be a perfect decompiler.

Also note carefully my reference to source modules. One characteristic
of C is that it becomes largely unreadable unless broken into easily
maintainable source modules (.C files). How will the decompiler deal
with that? It could either try to decompile the whole program into some
mammoth main() function, losing all modularity, or it could try to place
each called function into its own file. The first way would generate
unusable chaos and the second would run into problems where the original
source had files with multiple functions using static data and/or one or
more functions calling one or more static functions. A decompiler could
make static data and/or functions global but only at the expense or
readability (which would already be unacceptable).

You can generate one large source program with all functions in it (not
just one large main function, that\'s just crazy). Humans can chop the
large file into pieces, copying appropriate pieces into appropriately
named header files.

Indeed, I don\'t see this as being impossible to automate, either. It\'s
just a book-keeping problem. Computers are good at that. So I don\'t see
this as any kind of show-stopper.

Also, remember that commercial applications often code the most
difficult or time-critical functions in assembler which could prove
almost impossible to decompile into a C equivalent.

Again, this seems to be assuming that you are reversing the operation of
a compiler. Hand written machine code is almost indistinguishable from
compiled C code in the input binary, and decompiles just the same. In
fact, parts of the original program can be written in a variety of
procedural languages (e.g. C, C++, Pascal, Modula, Ada) and all these
pieces can be decompiled into a suitably expressive language (e.g. C).
Decompiling declarative or functional programming code is a different
matter.

Closely related to the issue of modularity is that of library code.
Consider the ubiquitous \"Hello world\" program. After compilation it
contains about 10 bytes of compiled source, about a dozen bytes of data,
and anywhere from 5-10K (depending on compiler, target, memory model,
etc.) of start up and library code.

Yes, this is a problem, but it is solvable. In this case, you
unfortunately do have to be compiler specific, and recognise sttically
compiled library functions as binary patterns. The commercial
disassmbler IDA Pro does this already, showing that is is practical to
do. The dcc decompiler applied this technique also.

Again, the situation with C++ would be orders of magnitude more complex
trying to make sense of the compiled code once the O-O structures and
relationships had been compiled into oblivion. Even if you take the
simple approach and decompile C++ into C, would anyone like to try and
trace through the source to figure out a cout call which adds another
7-10K of overhead vis-a-vis a printf() call? I sure wouldn\'t!!!

C++ certainly adds more library functions, and there is the issue of
name mangling, which is compiler specific. All solvable.

More problematic are templates. I believe that this can be solved with
code clone analysis (a standard source code technique), plus some high
level pattern matching. User templates could similarly be handled with
clone analysis.

So what do your have? For a small program, you\'d wind up trying to
decipher what is mostly library source. For a large program, you\'d wind
up with either 1) one humonguous main(), or 2) lots of arbitrary
single-function modules from which all notions of static data and
functions would have been lost (contributing to a vast pool of global
data), which would still include decompiled source for all the library
objects as well. In any scenario, is any of this useful? Probably not.

With the recognition of static library functions (which incidentally is
a valuable source of type information) and the clone analysis etc, you
would not have any (or very little) library source. Not decompiling the
library code means not seeing data specific to the libraries, as well.

While we\'ve touched on the topic of library code, here\'s yet another
reason that C and C++ are particularly difficult to de-compile: macros.

For instance, if I have something like:

        while (EOF != ( ch = getchar())) {
            if (isupper(ch))
                putchar(ch);

getchar, EOF, putchar and isupper are all typically macros, something
like:

    #define EOF -1
    #define isupper(x) (__types[(unsigned char)x+1] && __UPPER)
    #define getchar()  (getc(stdin))
    #define putchar(c) (putc((c),stdout)

    #define getc(s) ((s)->__pos<(s)->__len?     \
        (s)->__buf[__pos++]:                    \
          filbuf(s))
    #define putc(c,s) ((s)->__pos<(s)->__len?   \
        (s)->__buf[__pos++]=(c):                \
        putbuf((s),(c)))

Yes, this is a nuisance. Note that a correct decompiler will produce
correct, working source code, so that\'s something. The common cases can
be covered with high level pattern matching. Decompilers already have to
recognise a lot of patterns (e.g. X + 0 =\> X), so this is just a few
more high level patterns to add to the list. It is my belief that a good
decompiler has to have these \"rules\" organised in an easy to read
file, so that the list can readily be extended.

Finally, stdin and stdout are generally just items in an array of FILE
pointers something like:

    FILE __iobuf[20];

    FILE *stdin = __iobuf;      // This part is done silently by the
    FILE *stdout = __iobuf + 1; // compiler, without actual source code
    FILE *stderr = __iobuf + 2;

Even if you just expand the macros and never actually compile the code
at all, you end up with something that\'s basically unreadable. However,
this is what actually gets fed to the compiler, so it\'s also absolute
best you could ever hope for from a perfect de-compiler.

Again, only if you assume that you have to reverse the compiler. I
believe that these can be handled with a few more high level patterns.
Note that these high level patterns are not compiler specific; they
should work for all compilers, so you only have to fix it once.

C++ of course adds in-line functions and after an optimizer runs across
things, the code from the in-line function may well be mixed in with
surrounding code, making it nearly impossible to extract the function
from the code that calls it.

I believe that clone analysis handles this issue. Compilers already do
something similar when they inline the code; they have to change
parameters into variables, for example. Maintainers of legacy code
regularly look for clones, and convert them into parameterised calls. I
can\'t believe that inlining can\'t be undone.

Inlining is acually a help when it is applied to constructors; it helps
to find the virtual table for a function call, and hence the class that
the callee belongs to, and hence the type of the object pointer.

Removing calls to constructors and destructors (when added automatically
by the compiler) is another issue. I suspect it can be solved with
language dependent high level patterns.

There are only a few formats in use for vtables, which would help in
preserving virtual functions, but inline functions would be lost, so
you\'d typically end up with hundreds of times that code would be
directly accessing variables in other classes.

Virtual function calls are a significant problem, but they can be
analysed with techniques such as expression propagation and data flow
analysis. Assuming that clone analysis can convert inlined calls back to
standard calls, you would end up with either of two things:

1\) if there are virtual calls to the same callee, it would be recognised
as a class member function, as you would want.

2\) if there are no virtual calls to that callee, you would end up with a
non-class function that takes a member of that class as its first
parameter. That would be trivial to convert to a member function
(automatically or manually).

Like I said, don\'t hold your breath. As technology improves to where
decompilers may become more feasible, optimizers and languages (C++, for
example, would be a significantly tougher language to decompile than C)
also conspire to make them less likely.

I don\'t believe that optimisation poses a problem for decompilers, so I
certainly don\'t believe that compilers will \"stay a jump ahead\" of
decompilers for that reason.

For years Unix applications have been distributed in shrouded source
form (machine but not human readable \-- all comments and whitespace
removed, variables names all in the form OOIIOIOI, etc.), which has been
a quite adequate means of protecting the author\'s rights. It\'s very
unlikely that decompiler output would even be as readable as shrouded
source.

Yes, and there is also obfuscated source code, e.g. see the annual
obfuscated C code contest. Certainly, I have myself generated source
code that is much easier to read than obfuscated or shrouded code.

There is a big difference between obfuscated code and automatically
generated code. With obfuscated code, you use deliberately crazy
techniques such as compressing strings, passing negative integers as the
first parameter of main, and so on. With automatically generated code,
it (can be) just the same as real source code, just with generic names
and no comments. Perhaps in the far future, machines will be able to
generate more useful names, and add useful comments. Presumably, these
names will always be consistent, and the comments always correct, unlike
human written source code.

Shrouded code seems to me to be readily converted into more readable
forms; I\'ve never tried. A \"pretty printer\" program would convert it
into well indented code. If they have done nothing else to obfuscate the
code, then pretty printed srounded code would presumably look similar to
automatically decompiled code.

What\'s so wrong with that? Sure, it\'s hard to read; a lot of real
source code is hard to read. You can compile it, so that opens up a
whole range of applications right there (e.g. port to other
architecture, optimise, make minor changes, fix bugs, scan more readily
for vulnerability issues, etc). Plus, you have the opportunity to make
the code maintainable, by adding comments, changing names, etc. You
could not realistically do this with the binary program.

Despite it not being a magic bullet, there are plenty of applications
for machine code decmpilation.

A general purpose decompiler is the Holy Grail of tyro programmers.

This is probably true; novice programmers do dream of a general purpose
machine code decompiler. But it\'s a dream that could well come true; I
happen to believe that it\'s only a matter of time and hard work.
Perhaps I could reply in a similar vein that ill conceived answers such
as I have refuted above are the result of rookie investigators of the
surprisingly complex subject of decompilation.

\[by Bob Stout & Jerry Coffin\]

Refuation by [MikeVanEmmerik](MikeVanEmmerik){.twikiLink}.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
