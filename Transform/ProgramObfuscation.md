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
    Page](http://www.program-transformation.org/edit/Transform/ProgramObfuscation?t=1536825743)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ProgramObfuscation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ProgramObfuscation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ProgramObfuscation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ProgramObfuscation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Transform/ProgramObfuscation?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/ProgramObfuscation?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/ProgramObfuscation?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/ProgramObfuscation?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/ProgramObfuscation?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/ProgramObfuscation?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ProgramObfuscation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ProgramObfuscation?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Transform/ProgramObfuscation?template=oopsmore&param1=1.5&param2=1.5)
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
Program Obfuscation {#program-obfuscation .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Obfuscation is a
[ProgramTransformation](ProgramTransformation){.twikiLink} that makes a
program harder to understand by renaming variables, inserting dead code,
etc. Obfuscation is done to hide the business rules embedded in software
by making it harder to reverse engineer the program.

The main ideas seem to revolve around control-flow and data-flow
\"encoding\". The real code is padded with \"decoy\" code, and simple
operations (like adding and subtracting) are hidden behind \"transformed
variables\". For example, by subtracting two polynomials, you can
effectively perform an addition. It is claimed that this sort of thing
becomes very difficult even for the original author to reverse engineer,
or the writers of the encoding programs.

It could turn out that this technology will render decompilation
ineffective. My opinion (and it\'s not very well informed, I admit) is
that present obfuscation and tamper resistance is largely ineffective.
My guess is that it will stay that way, but only time will tell. To get
a flavour of what it\'s about, search for \"tamper resistant software\",
or start with these sites:

-   Gregory Wroblewski\'s work seems to have a good summary of work on
    the obfuscation of binary programs. His web page is
    <http://www.mysz.org/publications.html>.
-   Christian Collberg is a pioneer in obfuscation. See his page titled
    [Robust
    Obfuscation](http://www.cs.arizona.edu/~collberg/Research/Obfuscation).
-   There are many obfuscators for Java. See for example
    [DashO](http://www.preemptive.com/products/dasho/index.html).
-   [PreEmptive
    Solutions](http://www.preemptive.com/products/dotfuscator/index.html)
    has a product called Dotfuscator for CLI/MSIL/.NET, a light version
    of which is distributed with Microsoft® Visual Studio® .NET.

I came across a paper recently that claims that general program
obfuscation is impossible, as reported by this paper:

B. Barak, O. Goldreich, R. Impagliazzo, S. Rudich, A. Sahai, S. Vadhan,
and K. Yang. [On the (Im)possibility of Obfuscating
Programs](http://www.springerlink.com/(eyvpfnqjhm5xm555kncdekrp)/app/home/contribution.asp?referrer=parent&backto=issue,1,33;journal,1522,2217;linkingpublicationresults,1:105633,1).
In *Advances in Cryptology (CRYPTO\'01)*, volume 2139 of *Lecture Notes
in Computer Science*, pp 1-18, August 2001.

See also [TamperResistantSoftware](TamperResistantSoftware){.twikiLink}.

------------------------------------------------------------------------

[CategoryTransformation](CategoryTransformation){.twikiLink} \| \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 03 May 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
