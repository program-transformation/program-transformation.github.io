::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/CodeBoost?t=1536825372)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/CodeBoost)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/CodeBoost)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/CodeBoost?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/CodeBoost?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/CodeBoost?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/CodeBoost?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/CodeBoost?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/CodeBoost?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/CodeBoost?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/CodeBoost)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/CodeBoost?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/CodeBoost?template=oopsmore&param1=1.3&param2=1.3)
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
Code Boost {#code-boost .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[CodeBoost](CodeBoost){.twikiLink} is a tool for source-to-source
transformation and optimisation of C++ programs. It is intended to be
used as a testbed for various high-level optimisations; the traditional
textbook optimisations are assumed to be handled by the C++ compiler.
The [CodeBoost](CodeBoost){.twikiLink} optimiser will attempt to bridge
the gap between a human-friendly coding style and current
compiler/optimiser implementations. The C++ framework forms the basis
for the optimiser, but may also be useful for more general C++
transformation\--it has already been used in an experimental
instrumentation/profiling tool.

[CodeBoost](CodeBoost){.twikiLink} is part of the Sophus\[1\] project,
which explores the use of high-level abstractions for numerical
applications. This has great advantages in terms of easier programming
and maintenance, but poor performance has hindered the adoption of these
techniques in HPC. Current compilers have proven unable to optimise
sufficiently, partly due to low demand for such optimisations, and
partly because some of the most effective optimisations are in conflict
with the C++ standard. For [CodeBoost](CodeBoost){.twikiLink}, three
optimisations are on the way, and more are planned for the future.

The first optimisation is motivated by the use of operator overloading
in C++, which greatly improve the readability of complex expressions
involving user defined types. For instance, we can write A = A + B \* c,
instead of something like mul(B, c, t); add(A, t, A); (possibly with the
function bodies hand-inlined). Unfortunately, this programmer-friendly
style is bad for performance; the result must be copied, and each
operator call involves the creation of a new temporary. This might be
fine with only a few bytes of data, but unacceptable when working with
many megabytes. If the optimiser knows that A += B means the same as A =
A + B, it can rewrite the expression to use only one temporary, and
eliminate copying of the result. This is what the C++ compiler does for
built-in types, but it can\'t do it for user-defined types, because the
standard forbids assuming any relation between + and +=. If we demand
that this relation holds, or allow the user to specify it for each case,
we can perform the optimisation.

But even if we do this optimisation, we are left with another
performance problem; the operators are typically defined in terms of
loops, thus the computation is done in several passes over the data.
This causes unnecessary cache misses and index computations. A smart
optimiser can inline the operators, and use loop fusion to fold
consecutive loops into a single loop. Your compiler might actually do
loop fusion in some cases, but most likely it won\'t look for this case,
and miss the opportunity.

Inlining a function eliminates the function-call overhead, and allows
for further optimisations\--such as loop fusion. C++ provides the inline
keyword as a hint to the compiler that a function can be inlined, but
this is merely a hint; the compiler is free to ignore it. Depending on
the compiler, seemingly easy-to-inline code may run a lot slower than
hand-inlined code. With proper inlining, we can use functions actively,
and get better readability, maintainability and flexibility.

The [CodeBoost](CodeBoost){.twikiLink} framework is limited to
processing a simplified version of the C++ language. Many irrelevant
features, such as namespaces, pointers to functions, and inheritance,
have been ignored to keep the implementation concise and managable. New
features are added as the need arises. The restrictions are motivated
not only by implementation concerns, but also by good coding practice
and assumptions made by the [CodeBoost](CodeBoost){.twikiLink}
optimiser.

The implementation is based on standard compiler design, with clearly
seprarate parts for each step in the process. A modified version of
[OpenCpp](../Transform/OpenCpp){.twikiLink} is used for parsing,
everything else is written in Stratego. Stratego is a language for
specifying program transformations; the transformations are described by
a combination of concise rewrite rules, and strategies allowing precise
application of the rules based on context.

Intermediate output from [CodeBoost](CodeBoost){.twikiLink} is in the
Tools.ATerm format, and is primarily useful for Stratego programs, but
is also accessible from C, C++ and Java, and is easily parsable. The
final output is readable C++ code.

**See also**

-   [CodeBoostDownload](CodeBoostDownload){.twikiLink}
-   [CodeBoostPublications[^?^](http://www.program-transformation.org/edit/Stratego/CodeBoostPublications?topicparent=Stratego.CodeBoost)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [CodeBoostContributors](CodeBoostContributors){.twikiLink}
-   [CodeBoostLinks[^?^](http://www.program-transformation.org/edit/Stratego/CodeBoostLinks?topicparent=Stratego.CodeBoost)]{.twikiNewLink
    style="background : #FFFFCE;"}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
