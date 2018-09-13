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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationFaqRefutation?t=1536826458)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationFaqRefutation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationFaqRefutation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationFaqRefutation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationFaqRefutation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Transform/DecompilationFaqRefutation?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/DecompilationFaqRefutation?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/DecompilationFaqRefutation?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DecompilationFaqRefutation?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilationFaqRefutation?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilationFaqRefutation?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationFaqRefutation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationFaqRefutation?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationFaqRefutation?template=oopsmore&param1=1.5&param2=1.5)
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
Decompilation Faq Refutation {#decompilation-faq-refutation .twikiTopicTitle}
============================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Question 38.4 of the [C++ FAQ
LITE](http://www.parashift.com/c++-faq-lite) demonstrates a typical
negative reaction to the basic question \"how can I decompile a C++
executable file?\". I don\'t mean any offense to the maintainers of this
particular FAQ, or of any of the many naysayers; this appears to be the
generally accepted wisdom. Hopefully, we can all learn something from
picking apart the arguments one by one.

The original FAQ question is [38.4 How can I decompile an executable
program back into C++ source
code?](http://www.parashift.com/c++-faq-lite/compiler-dependencies.html#faq-38.4).

Their answer is reproduced below in red; my refutation follows in
default colours.

You gotta be kidding, right?

Certainly not. There are plenty of legitimate reasons to perform
decompilation. See [WhyDecompilation](WhyDecompilation){.twikiLink}.

Here are a few of the many reasons this is not even remotely feasible:

-   What makes you think the program was written in C++ to begin with?

I don\'t have to think that at all. It doesn\'t matter what language the
original program was compiled in, within reason. The semantics of the
original program are there, all decompilation does is translate that
binary form of the program to another form, which happens to be source
code; for the purposes of refuting this FAQ answer, C++ source code.

-   Even if you are sure it was originally written (at least partially)
    in C++, which one of the gazillion C++ compilers produced it?

Again, it doesn\'t matter. Different compilers will produce different
executable output, certainly; each of these is equivalent to all the
others (assuming the compilers are competent), and each is equivalent to
the original source code.

-   Even if you know the compiler, which particular version of the
    compiler was used?

It doesn\'t matter.

-   Even if you know the compiler\'s manufacturer and version number,
    what compile-time options were used?

It doesn\'t matter. All the possible outputs are equivalent.
Optimisation usually doesn\'t hurt either; often it makes the
decompiler\'s job slightly easier because there is a little bit less
executable code to work through, and a little less of the detail in the
executable file is thrown away. Optimisation can reduce the readability
somewhat when the compiler inlines function calls. Even so, the result
is still correct and readable, just (usually) with more repetition. Such
inlining can be undone, perhaps automatically, if necessary and/or
desirable.

-   Even if you know the compiler\'s manufacturer and version number and
    compile-time options, what third party libraries were linked-in, and
    what was their version?

It doesn\'t matter, as long as the decompiler has access to the
signatures for the libraries (assuming that they are statically linked.
Dynamically linked libraries are no problem; the executable file has to
provide the name of the library function, so all the decompiler needs is
a prototype of the function, to get its parameters and return types.) If
this information is not available, then usually the library function
will get decompiled too. Not what you want, but with a little knowledge
of the original program\'s domain, it should not be difficult to figure
out a prototype for each library function.

-   Even if you know all that stuff, most executables have had their
    debugging information stripped out, so the resulting decompiled code
    will be totally unreadable.

The original comments will be missing, certainly, as will the original
variable names. So you will probably end up with generic variable names
such as local2 and global17. However, that\'s far from unreadable, if
the structure of the program is good (proper for loops, if/then/else,
switch, minimal gotos, proper data types, etc. All these can be
achieved.) Even if you call this output unreadable, if the decompiler
has done its job correctly, the output will be recompilable. This makes
a whole set of applications for decompilation possible. For example, you
can recompile the unreadable output with various optimisations specific
to your requirements. You may be able to port the program to another
platform with minimal understanding of how it works. You may find it
easier to spot malware in C++ code with no comments or labels than it is
to spot it in a disassembly with no comments or labels. And so on.

It is possible (though admittedly it seems unlikely at this stage) that
some form of artificial intelligence will be able to insert meaningful
comments and/or variable names, based on design patterns detected in the
program. Such automatically generated comments and names could in some
cases be more valuable (since they will presumably mostly be correct)
than the original comments, which in some cases are out of date and may
even be misleading. Sometimes even no information is better than wrong
information.

-   Even if you know everything about the compiler, manufacturer,
    version number, compile-time options, third party libraries, and
    debugging information, the cost of writing a decompiler that works
    with even one particular compiler and has even a modest success rate
    at generating code would be significant --- on the par with writing
    the compiler itself from scratch.

Certainly, writing a decompiler is non trivial. I would not recommend it
for those without detailed knowledge of assembly language, for example.
But why write a decompiler that is specific to one compiler,
manufacturer, etc? Machine code is a language; it just happens to be a
binary language. General program transformation techniques can be used
to transform programs written in machine language into equivalent
programs that are in C++. A good compiler doesn\'t restruct itself to a
particular version number of programmer, does it?

But the biggest question is not how you can decompile someone\'s code,
but why do you want to do this?

Again, see [WhyDecompilation](WhyDecompilation){.twikiLink}. Plus, it
doesn\'t have to be somone else\'s code, as you indicate below
(recovering your own lost source code).

If you\'re trying to reverse-engineer someone else\'s code, shame on
you; go find honest work.

Why does it have to be someone else\'s code? It\'s been estimated that
about 3% to 5% of the world\'s source code is missing. Added to that,
some of the original compilers are no longer available, or the hardware
to run them is no longer convenient. (Consider trying to run a DOS based
compiler that requires XMS memory\... could you get it to run
conveniently? It was only about 10 years ago that such compilers were in
regular use.)

However, what\'s to stop the owner of some executable from coming to me,
asking me to decompile his or her program for them? Why can\'t I provide
this service, which may save their company from bankrupcy, or save them
money by enabling them to run an old program until they have time to
develop a replacement for it?

Also, there are legal reasons to reverse engineer someone else\'s work.
Consider interoperability, like a driver that doesn\'t work on my
system. In most countries, I can reverse engineer the code to the extent
necessary for interoperability (in this case, to fix the driver). Some
countries also have provisions for studying algorithms for research
purposes, and there is also the largely untested area of abandoned
software.

Yes, decompilation can be used for illegal purposes. But compilers can
be used to compile malware, video recorders can be used to make illegal
copies of copyrighted movies, and knives can be used for unlawful
killing. Should all these things be banned too? No, because they all
have \"substantial non-infringing uses\".

If you\'re trying to recover from losing your own source, the best
suggestion I have is to make better backups next time.

So you\'ve never had a backup fail? You back up everything you think
you\'ll need? Nobody ever leaves your company? You will never get taken
over by another company? Accidents happen. Sometimes, source code isn\'t
missing, but you can\'t find the right source code to match a particular
executable. This is basically what happened to a company that approached
me.

I have a better suggestion: use backups by all means, but when they
fail, and they will from time to time, there is an option:
decompilation. Certainly, it is not perfect, certainly not yet, but
let\'s not dismiss the idea outright because you think it\'s an
inherently bad thing.

(Don\'t bother writing me email saying there are legitimate reasons for
decompiling; I didn\'t say there weren\'t.)

Good, then you agree that there are substantial non infringing uses for
decompilation. The Sony Betamax case tells us that technology with
substantial non infringing uses is legal. Yes, there are those who would
prefer to outlaw certain things, such as Peer to Peer software
distribution programs, but they seem to want to shoot the messenger
rather than address the real concerns (in the case of P2P, how to
sensibly license copyrighted materials; in the case of decompilation,
how to secure proprietary code distributed in binary form. For a long
time, they could pretend that executable programs are not readable; with
improvements in decompilation, this is no longer true.)

See also [BobStoutRefutation](BobStoutRefutation){.twikiLink}.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 07 Jul 2005;
updated 01 Sep 2005.\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
