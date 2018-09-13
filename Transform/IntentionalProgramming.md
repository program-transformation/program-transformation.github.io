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
    Page](http://www.program-transformation.org/edit/Transform/IntentionalProgramming?t=1536826325)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/IntentionalProgramming)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/IntentionalProgramming)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/IntentionalProgramming?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/IntentionalProgramming?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/IntentionalProgramming?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/IntentionalProgramming?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/IntentionalProgramming?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/IntentionalProgramming?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/IntentionalProgramming?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/IntentionalProgramming?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/IntentionalProgramming)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/IntentionalProgramming?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/IntentionalProgramming?template=oopsmore&param1=1.7&param2=1.7)
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
Intentional Programming {#intentional-programming .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Description**

Intentional programming developed at Microsoft Research \[Ait98\] is a
method for extending a language with new constructs or *intentions*. The
meaning of intentions is defined by means of transformation rules. A
rule transforms an intention into an expression built of more primitive
intentions.

The method is supported by a C library for tree manipulation that can be
used to express transformation rules. Rules have to explicitly
deconstruct and reconstruct trees with awareness of pointers. No support
for pattern matching seems to be provided. A detailed knowledge of the
implementation details of the abstract syntax seems to be required to be
able to write or understand transformation rules.

An ordering of application of rules (strategy) is derived from
dependencies between rules.

From \[Ait98\] it is not clear at what level intentions are defined.
Does the programmer extend a program with new intentions that are used
in the same program? Or are intentions defined at the meta-level of the
language definition, which is thus made extensible?

------------------------------------------------------------------------

Remarks by [OegeDeMoor](OegeDeMoor){.twikiLink} on July 13, 2001. The
intentions are defined at the meta-level of language definition.

The first two references below describe obsolete designs. More
up-to-date descriptions are provided by the latter two. The talk for the
British Computer Society is aimed at a general audience.

------------------------------------------------------------------------

References 3. and 4. make it clear that *modular language design* is a
key point of intentional programming.

Several of the aims of and techniques used in intentional programming
are very similar to those of the
[ASFandSDFMetaEnvironment](ASFandSDFMetaEnvironment){.twikiLink}. An
original goal was to have one description of a generic while statement,
for example, which would be reusable for different languages (e.g., C,
Pascal, and Cobol). This way of modularization, however, turned out to
be not feasible, due to the differences in existing languages. I believe
the modular design aspects of intentional programming are not so much in
describing *existing* languages, but in having \"intentions\" (language
features) that are reusable across different domains, so IP may be
successful in this respect.

I think some interesting related approaches include the Jargons of
Lucent by Nakatani and the work on interactive language design by Uwe
Karstens (for both, see the
[DSLAnnotatedBibliography](DSLAnnotatedBibliography){.twikiLink}). Also
related is the (newer) work on language design assistants by
[JanHeering](JanHeering){.twikiLink}.

\-- [ArieVanDeursen](ArieVanDeursen){.twikiLink} - 13 Aug 2001\

------------------------------------------------------------------------

**References**

1.  Chapter 11 of
    [GenerativeProgrammingBook](GenerativeProgrammingBook){.twikiLink}
2.  \[Ait98\] William Aitken, Brian Dickens, Paul Kwiatkowski, Oege de
    Moor, David Richter, Charles Simonyi, \"Transformation in
    Intentional Programming,\" In Proceedings of the 5th Int. Conf. on
    [SoftwareReuse](SoftwareReuse){.twikiLink},
    [IEEE](IEEE){.twikiLink}, 1998. See
    <http://research.microsoft.com/copyright/accept.asp?path=/ip/overview/TrafoInIP.pdf&pub=IEEE>
    (describes a now obsolete design)
3.  [OegeDeMoor](OegeDeMoor){.twikiLink}. Intentional Programming.
    Lecture for the British Computer Society. See
    <http://web.comlab.ox.ac.uk/oucl/work/oege.demoor/talks/ip.pdf.gz>
4.  [OegeDeMoor](OegeDeMoor){.twikiLink},
    [GaneshSittampalam](GaneshSittampalam){.twikiLink} and Eric van Wyk.
    Intentional Programming: a host of language features. Technical
    report, Oxford University Computing Laboratory. See
    <http://web.comlab.ox.ac.uk/oucl/work/eric.van.wyk/Papers/ip.ps>

**See Also**

-   [TransformationSystems](TransformationSystems){.twikiLink}
-   <http://www.c2.com/cgi/wiki?IntentionalProgramming>
-   <http://www.aisto.com/roeder/active>
    -   (The original link <http://research.microsoft.com/ip/> is dead)

------------------------------------------------------------------------

[CategorySystem](CategorySystem){.twikiLink} \| Contributions by
[OegeDeMoor](OegeDeMoor){.twikiLink},
[ArieVanDeursen](ArieVanDeursen){.twikiLink},
[EelcoVisser](EelcoVisser){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
