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
    Page](http://www.program-transformation.org/edit/Transform/BinaryTranslationProcessors?t=1536826434)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/BinaryTranslationProcessors)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/BinaryTranslationProcessors)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/BinaryTranslationProcessors?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/BinaryTranslationProcessors?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/BinaryTranslationProcessors?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/BinaryTranslationProcessors?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/BinaryTranslationProcessors?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/BinaryTranslationProcessors?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/BinaryTranslationProcessors?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/BinaryTranslationProcessors?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/BinaryTranslationProcessors)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/BinaryTranslationProcessors?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/BinaryTranslationProcessors?template=oopsmore&param1=1.4&param2=1.4)
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
Binary Translation Processors {#binary-translation-processors .twikiTopicTitle}
=============================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

-   [Transmeta](http://www.transmeta.com)\'s first processor the Crusoe
    (see their [white
    paper](http://www.transmeta.com/crusoe/download/pdf/crusoetechwp.pdf))
    implements the pentium architecture on a VLIW processor. They have a
    few hardware assists, and the current processor achieves a very low
    power requirement.

<!-- -->

-   [Elbrus](http://www.elbrus.ru) appears to be a Russian attempt at a
    Transmeta type chip, i.e. implementing an X86 chip on a VLIW
    processor, using binary translation.

<!-- -->

-   [IBM](http://www.ibm.com)\'s
    [DAISY](http://www.research.ibm.com/daisy) is a dynamic binary
    translator of PowerPC to VLIW code. The translator uses a fast
    technique to parallelise ordinary code (PowerPC or other
    architectures), and is being made available for
    [download](http://www-124.ibm.com/developerworks/opensource/daisy)
    under an open source license.

<!-- -->

-   IBM\'s experimental Binary-translation Optimized Architecture (BOA)
    aims at producing a very high frequency VLIW processor (or
    processors on one chip). Like Transmeta, the underlying processor is
    not visible to the programmer, in user or supervisor mode, and may
    change over time. See the [IEEE](IEEE){.twikiLink}
    \"[Computer](http://www.computer.org)\" article [Dynamic and
    Transparent Binary
    Translation](http://citeseer.nj.nec.com/423478.html).

<!-- -->

-   [Alchemy Semiconductors](http://www.alchemysemi.com) has an
    [agreement](http://www.transitives.com/pr_oct_15_01b.htm) with
    [Transitive Technologies](http://www.transitives.com) to use their
    binary translation technology to run ARM programs on their family of
    low power MIPS processors.

<!-- -->

-   [Intel](http://www.intel.com)\'s [Pentium
    4](http://www.intel.com/home/pentium4) processor, with the
    [NetBurst\[tm](http://developer.intel.com/pentium4/download/netburst.pdf)\]
    microarchitecture, has a level 1 execution trace cache which can
    store 12K of previously translated micro-ops. There is even a
    facility to perform loop unrolling into the trace cache. See this
    early article from [Real World
    Technologies](http://www.realworldtech.com/page.cfm?section=news&AID=RWT030300000001&p=4),
    the [Intel developer pages](http://developer.intel.com/pentium4),
    and [The Microarchitecture of the Pentium® 4
    Processor](http://developer.intel.com/technology/itj/q12001/articles/art_2.htm)
    (as
    [.pdf](http://developer.intel.com/technology/itj/q12001/pdf/art_2.pdf)).

<!-- -->

-   [Sun](http://www.sun.com)\'s
    [MAJC](http://www.sun.com/microelectronics/MAJC) processor
    (Microprocessor Architecture for Java Computing) was supposed to be
    an ideal target for
    [JavaDynamicCompilers](JavaDynamicCompilers){.twikiLink}. It seems
    to have been cancelled.

[]{#HardwareAssistance}

-   Hardware assistance
    -   [Nazomi](http://www.nazomi.com)\'s
        [JSTAR](http://www.nazomi.com/html/technology_overview.html)
        technology is a coprocessor, designed to work with any standard
        microprocessor, that provides a sort of hardware JIT compiler.
        The JSTAR coprocessor would be integrated onto the
        microprocessor chip, and consumes no power when not executing
        Java programs. When running, the coprocessor feeds native
        instructions into the host processor, which can be anything from
        8 to 64 bits, any endianness, etc. Handles any VM as well, since
        the microcode can be in RAM. The JVM has to be modified to be
        \"JSTAR aware\". Performance increases of about 10x are claimed,
        with 30x less power when running Java applications.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 13 Dec 2001\
[CategoryBinaryTranslation](CategoryBinaryTranslation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
