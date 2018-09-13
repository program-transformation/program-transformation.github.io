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
    Page](http://www.program-transformation.org/edit/Transform/BinaryOptimisers?t=1536826433)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/BinaryOptimisers)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/BinaryOptimisers)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/BinaryOptimisers?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/BinaryOptimisers?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Transform/BinaryOptimisers?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/BinaryOptimisers?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/BinaryOptimisers?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/BinaryOptimisers?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/BinaryOptimisers?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/BinaryOptimisers?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/BinaryOptimisers)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/BinaryOptimisers?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Transform/BinaryOptimisers?template=oopsmore&param1=1.5&param2=1.5)
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
Binary Optimisers {#binary-optimisers .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Binary Optimisers** are sometimes called \"Post Link optimisers\".
These products can be viewed as \"X to X binary translators\". Another
name is Binary Rewriting systems.

-   [HP](http://www.hp.com)\'s
    [Dynamo](http://www.hpl.hp.com/cambridge/projects/Dynamo) is pretty
    much the leader in this field

<!-- -->

-   Wiggins/Redstone is an experimental dynamic optimiser that uses a
    novel combination of hardware sampling and software instrumentation
    to dynamically collect hot path information. It is unpublished as of
    2001, but there is a series of slides from a presentation at Hot
    Chips 11, entitled [Wiggins/Redstone: An On-line Program
    Specializer](http://world.std.com/~gorton/professional/deaver.pdf).

<!-- -->

-   [Microsoft](http://www.research.microsoft.com)\'s Mojo is a research
    dynamic optimiser for Windows. See the paper [Mojo: A Dynamic
    Optimization
    System](http://www.ece.wisc.edu/~jes/902/papers/mojo.pdf). Results
    to date are not good (most programs slow down), but they have
    directions for future improvements.

<!-- -->

-   [Software Optimization at Link-time And Run-time
    (SOLAR)](http://www.cs.arizona.edu/solar/index.html) at the
    University of Arizona. From their web page: *The SOLAR project is
    developing binary rewriting techniques for flexible link-time and
    run-time code optimizations. We are exploring a variety of
    applications, architectures, and optimization metrics. Applications
    include traditional sequential programs, parallel scientific
    programs that use a message passing library such as MPI, and mobile
    computing applications. We have developed link-time optimizers for
    the Compaq Alpha and Intel IA-32 (Pentium) architectures, and are
    building one for the Intel/HP IA-64 (Itanium) architecture.*

**Optimisers Requiring Source Code** (link time or post link). Although
these are static optimisers, they rely on special information (profile
information or object files) that are not available without the source
code to the program being optimised, and so are not really binary
translators. They are somewhat related, so they are mentioned here.

-   [Compaq](http://www.compaq.com)\'s spike (see [Tru64 Unix
    Programmer\'s
    Guide](http://www.tru64unix.compaq.com/dtk/misc_docs/prog_gd) and
    search for \"spike\") is actually a static (but post link) optimiser
    that can take advantage of profile information. Thus, it\'s not
    really a binary translator.

<!-- -->

-   [Alto](http://www.cs.arizona.edu/alto) is a link time optimiser. It
    is therefore able to see all of the code at once (including
    libraries). Again, not a binary translator.

**Binary program compactors**. These systems compact programs to deal
with the fact that hard disks are increasing in speed slower than
processors are, or that embedded devices often have limited memory.

-   [Innaworks](http://www.innaworks.com)\'
    [mBooster](http://www.innaworks.com/mBooster.html) is the first
    commercial recompiler for J2ME midlets and iAppli applications.
    mBooster is actually an optimizing recompiler. It takes J2ME
    bytecode and recompiles using agressive compiler-based optimization
    techniques to generate optimized J2ME bytecode. Common J2ME mobile
    phones today have very tight size constraints: 64kB is the norm.

<!-- -->

-   [Squeeze](http://www.cs.arizona.edu/squeeze) at the University of
    Arizona, is a project aimed at reducing the memory footprint for
    executables on palm sized devices.

<!-- -->

-   [Squeeze++](http://www.elis.rug.ac.be/~brdsutte/squeeze++) is an
    evolution of Sqeeze. It is an example of binary compaction, applying
    aggressive whole-program optimization and code abstraction
    techniques on binary programs. Squeeze++ compacted programs are up
    to 70% smaller and at the same time 20% faster. Squeeze++ is a
    binary rewriter rather than a binary translator.

------------------------------------------------------------------------

[CategoryBinaryTranslation](CategoryBinaryTranslation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
