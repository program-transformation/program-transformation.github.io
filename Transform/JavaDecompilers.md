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
    Page](http://www.program-transformation.org/edit/Transform/JavaDecompilers?t=1536826292)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/JavaDecompilers)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/JavaDecompilers)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/JavaDecompilers?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/JavaDecompilers?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    24](http://www.program-transformation.org/view/Transform/JavaDecompilers?rev=1.24)
    [(diff 23)](http://www.program-transformation.org/rdiff/Transform/JavaDecompilers?rev1=1.24&rev2=1.23)
-   [Rev
    23](http://www.program-transformation.org/view/Transform/JavaDecompilers?rev=1.23)
    [(diff 22)](http://www.program-transformation.org/rdiff/Transform/JavaDecompilers?rev1=1.23&rev2=1.22)
-   [Rev
    22](http://www.program-transformation.org/view/Transform/JavaDecompilers?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Transform/JavaDecompilers?rev1=1.22&rev2=1.21)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/JavaDecompilers)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/JavaDecompilers?template=oopsmore&param1=1.24&param2=1.24)
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
    \...](http://www.program-transformation.org/oops/Transform/JavaDecompilers?template=oopsmore&param1=1.24&param2=1.24)
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
Java Decompilers {#java-decompilers .twikiTopicTitle}
================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

::: {.twikiToc}
-   [Java Bytecode
    Decompilers](JavaDecompilers#Java_Bytecode_Decompilers)
-   [Comparison of Java Bytecode
    Decompilers](JavaDecompilers#Comparison_of_Java_Bytecode_Deco)
-   [Java Decompiler Articles](JavaDecompilers#Java_Decompiler_Articles)
-   [Java Decompilation Books](JavaDecompilers#Java_Decompilation_Books)
-   [Java Decompiler Papers](JavaDecompilers#Java_Decompiler_Papers)
-   [Decompiler front ends](JavaDecompilers#Decompiler_front_ends)
-   [Java Decompiler Links](JavaDecompilers#Java_Decompiler_Links)
:::

[]{#Java_Bytecode_Decompilers} Java Bytecode Decompilers
--------------------------------------------------------

Decompilers that read Java bytecode programs usually decompile to Java,
since that is the language that the majority of such programs are
written in. However, the source language could have been any of a large
number of languages; see [\[other languages for the Java
VM](http://c2.com/cgi/wiki?OtherLanguagesForTheJavaVm%5D).

-   [Jdec](http://jdec.sourceforge.net) is a Java decompiler. It can be
    used to decompile the bytecodes present in a .class file to produce
    a Java source file which can be nearly correct or equivalent (due To
    different interpretations) to the original Java source. It also has
    a good UI. It is hosted on [SourceForge](http://sourceforge.net).
    Currently Jdec is licenced under [GPL](GPL){.twikiLink}. Visit the
    [home site](http://jdec.sourceforge.net) for any updates and current
    status.

<!-- -->

-   [JODE](http://jode.sourceforge.net) is an open source Java
    decompiler and obfuscator. Hosted on
    [SourceForge](http://sourceforge.net) under the
    [GPL](GPL){.twikiLink} license. The core decompiler is under the
    LGPL, meaning that you can use it in a commercial decompiler.
    Written in Java. For tests see
    [DecompilationJodeTest](DecompilationJodeTest){.twikiLink}.

<!-- -->

-   [Jad](http://kpdus.tripod.com/jad.html) (Jad - the fast JAva
    Decompiler) is a decompiler that is free for non commercial use.
    Source code is not provided. Its decompilation engine is used in
    numerous graphical front ends, including [FrontEnd
    Plus](http://www.reflectonus.pwp.blueyonder.co.uk/download.htm),
    [Decafe Pro](http://decafe.hypermart.net), [DJ Java
    Decompiler](http://members.fortunecity.com/neshkov/dj.html), and
    [Cavaj](http://sureshot.virtualave.net/cavaj). For tests see
    [DecompilationJadTest](DecompilationJadTest){.twikiLink}.

<!-- -->

-   [Dava](DecompilationDava){.twikiLink} is a research decompiler that
    recovers types well and has been tested against non-Java bytecode
    programs.

<!-- -->

-   The [Mocha](http://www.brouhaha.com/~eric/computers/mocha.html)
    decompiler for Java .class files. You can use crema to scramble
    symbolic information in the .class files.

<!-- -->

-   [SourceTec Java Decompiler](http://www.srctec.com/decompiler.htm)
    (formerly the Jasmine Java Decompiler) is a patch to Mocha, a well
    known decompiler. It is now very old; it only works on Java 1.1
    classfiles. For tests see
    [DecompilationStTest](DecompilationStTest){.twikiLink}.

<!-- -->

-   [JReversePro](JReversePro){.twikiLink} is an open source Java
    decompiler written in Java.

<!-- -->

-   [SourceAgain](SourceAgain){.twikiLink} is one of the better known
    commercial Java decompilers.

<!-- -->

-   [ClassCracker 3](http://mayon.actewagl.net.au/index.html) is another
    commercial Java decompiler.

<!-- -->

-   Decaf was a decompiler for Java .class files written in Ada95.
    Decompilers to Ada95 and Smalltalked were planned. The page was at
    <http://ourworld.compuserve.com/homepages/teleobjet/decaf.htm>. You
    may be able to access an archived copy at
    [archive.org](http://www.archive.org).

<!-- -->

-   [DCompiler](http://sourceforge.net/projects/dcompiler) (also known
    as JADO) is yet another Sourceforge open source decompiler; this one
    is in *very* alpha status. It will not decompile even the simplest
    test programs, so no tests have been performed.

<!-- -->

-   [WingSoft](http://www.wingsoft.com) have a decompiler called WingDis
    and an obfuscator called WingGuard (see their
    [products](http://www.wingsoft.com/products.shtml) page).

<!-- -->

-   The JReveal decompiler ([www.jreveal.org](http://www.jreveal.org))
    seems to be the Jasmine decompiler (version 1.1 of Mocha), with a
    web based GUI front end. I could not get the decompiler to work for
    me (Jan 2003), but you may have better luck. There is a small online
    paper and some examples; it looks like a really handy tool.

[]{#Comparison_of_Java_Bytecode_Deco} Comparison of Java Bytecode Decompilers
-----------------------------------------------------------------------------

-   See [Java Decompiler Tests](JavaDecompilerTests){.twikiLink}

[]{#Java_Decompiler_Articles} Java Decompiler Articles
------------------------------------------------------

-   [Java World](http://www.javaworld.com) has an article [Java
    decompilers
    compared](http://www.javaworld.com/javaworld/jw-07-1997/jw-07-decompilers.html),
    where they compare DejaVu, Mocha, and WingDis.

<!-- -->

-   [Java Decompilers and are they worth worrying
    about](http://www.andromeda.com/people/ddyer/java/decompiler-table.html).
    This article also compares the above three decompilers.

<!-- -->

-   \"Decompile Once, Run Anywhere\": [new.architect
    magazine](http://www.newarchitectmag.com) have an archive of the
    classic article by Godfrey Nolan [Decompile Once, Run
    Anywhere](http://www.newarchitectmag.com/documents/s=6410/new1013637873/index.html),
    which details how readily most Java programs can be decompiled.
    Godfrey has published a book titled \"Decompiling Java\".

<!-- -->

-   \"How to lock down your Java code\": [How to lock down your Java
    code (or open up someone
    else\'s)](http://www-106.ibm.com/developerworks/java/library/j-obfus/?loc=crtheme).
    Subtitle: *Your complete guide to the decompilation and obfuscation
    of Java code*, by Greg Travis, May 2001. From IBM Developerworks
    Java articles.

[]{#JavaDecompilerBooks}

[]{#Java_Decompilation_Books} Java Decompilation Books
------------------------------------------------------

-   \"Decompiling Java\": a book by Godfrey Nolan; ISBN 1590592654,
    APRESS August 2004.
    [Amazon](http://www.amazon.com/exec/obidos/tg/detail/-/1590592654/104-9575356-9027145?v=glance)
    page. Note that some websites still refer to the old ISBN
    (0079137679); I believe that this version was never published. See
    also <http://www.artima.com/chapters/book.jsp?num=62427>. An early
    version of this book was available on the web. There is a whole
    chapter on defeating decompilers, one on decompiler design, and one
    on the implementation of a simple decompiler. There is little in the
    way of theory, e.g. structuring goto riddled code into readable Java
    loops and conditionals.

<!-- -->

-   \"Covert Java: Techniques for Decompiling, Patching, and Reverse
    Engineering\", Alex Kalinovsky. Chapter 2 is on decompiling
    bytecode. [Amazon
    page](http://www.amazon.com/exec/obidos/tg/detail/-/0672326388/ref=cm_custrec_gl_acc/104-9575356-9027145?v=glance&s=books).
    ISBN 0672326388.

[]{#Java_Decompiler_Papers} Java Decompiler Papers
--------------------------------------------------

Katsumata and Ohori published a paper describing a decompiler from
bytecodes to a PCF-like language (simply typed functional language). For
example, an iterative implementation of the factorial program becomes as
shown below. The work is proof-directed and very theoretical, though
they did build a decompiler (but not to Java, as shown below).

            fact(e0) =
              L12(e0, 1)
            L12(e0, e1) =
              if (1 < e0) then
                L12(e0 - 1, e1 * e0)
              else
                return e1

-   S. Katsumata and A. Ohori. Proof-directed De-compilation of
    Low-Level Code. In *European Symposium on Programming*, volume 2028
    of *Lecture Notes in Computer Science*, pages 352-366.
    Springer-Verlag, 2001.
-   Alan Mycroft. Comparing Type-Based and Proof-Directed Decompilation.
    In *Proceedings of the Working Conference on Reverse Engineering*,
    pages 362-367, Stuttgart, Germany, 2001. [IEEE](IEEE){.twikiLink}
    CS-Press.
-   [Programmer-friendly Decompiled
    Java](http://www.sable.mcgill.ca/publications/techreports/#report2006-2),
    Nomair A. Naeem and Laurie Hendren. Technical report number
    SABLE-TR-2006-2, [Sable Research Group](http://www.sable.mcgill.ca),
    [McGill University](http://www.mcgill.ca), 2006. This report is
    about making the Dava decompiler produce more readable output.

The Krakatoa Java decompiler appears to have a quite good structuring
algorithm, according to the following paper, but the decompiler not
publically available.

-   Todd A. Proebsting and Scott A. Watterson. [Krakatoa: Decompilation
    in Java (Does bytecode reveal
    source?)](http://research.microsoft.com/pubs/view.aspx?pubid=39). In
    Conference on Object-Oriented Technologies and Systems (COOTS \'97),
    pages 185-197. The [USENIX](USENIX){.twikiLink} Association, 1997.

[]{#Decompiler_front_ends} Decompiler front ends
------------------------------------------------

Some decompilers are just GUI front-ends for a console (text) based
decompiler. Some are listed in this table.

  [Front end (GUI) decompiler](JavaDecompilers@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Back end decompiler (engine)](JavaDecompilers@sortcol=1&table=1&up=0#sorted_table "Sort by this column")
  --------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------
  Cavaj                                                                                                     Jad
  Decafe Pro                                                                                                Jad
  DJ Java Decompiler                                                                                        Jad
  Frontend Plus                                                                                             Jad
  [JadClipse](http://sourceforge.net/projects/jadclipse) (Eclipse plugin)                                   Jad
  BTJ (Back To Java)                                                                                        JODE
  jEdit\'s JavaInsight plugin                                                                               JODE

[]{#JavaLinks}

[]{#Java_Decompiler_Links} Java Decompiler Links
------------------------------------------------

-   See also the [dmoz open directory](http://dmoz.org) page [Computers
    / Programming / Languages / Java / Development Tools / Translators /
    Decompilers and
    Disassemblers](http://dmoz.org/Computers/Programming/Languages/Java/Development_Tools/Translators/Decompilers_and_Disassemblers).
-   <http://www.updated.com/search/?text=decompiler>
-   [Programming Languages for the Java Virtual
    Machine](http://flp.cs.tu-berlin.de/~tolk/vmlanguages.html) is a
    page by Robert Tolksdorf for all sorts of languages that can be
    compiled to bytecodes, or translated to Java source. There are well
    over a hundred entries.
-   The Linux
    [Java-Decompiler-HOWTO](http://www.tldp.org/HOWTO/Java-Decompiler-HOWTO.html).
    Some parts not to be taken too seriously (e.g. how to trust your
    decompiler).
-   <http://java-decompiler.com> has many links to Java decompilers,
    disassemblers, assemblers, obfuscators, etc.
-   [The New
    Obfuscation](http://www.preemptive.com/documentation/NewObfuscation.html)
    details developements in code security and Java obfuscation.
-   The Java Code Engineering pages seem to be gone forever. It had
    comprehensive details on Java disassemblers, decompilers, and more.
    The last copy of it that I am aware of is
    [here](http://web.archive.org/web/20011121083507/http://www.meurrens.org/ip-Links/Java/CodeEngineering/decomp.html)
    (from <http://web.archive.org>).

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
