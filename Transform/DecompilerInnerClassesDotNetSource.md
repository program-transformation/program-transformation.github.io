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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerInnerClassesDotNetSource?t=1536826466)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerInnerClassesDotNetSource)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerInnerClassesDotNetSource)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerInnerClassesDotNetSource?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerInnerClassesDotNetSource?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilerInnerClassesDotNetSource?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilerInnerClassesDotNetSource?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompilerInnerClassesDotNetSource?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerInnerClassesDotNetSource)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerInnerClassesDotNetSource?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerInnerClassesDotNetSource?template=oopsmore&param1=1.2&param2=1.2)
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
Decompiler Inner Classes Dot Net Source {#decompiler-inner-classes-dot-net-source .twikiTopicTitle}
=======================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This class is also from the book [Decompiling
Java](http://www.riis.com/depile.html), this time chapter 3:

    using System;
    public class Usa {
        public String name = "Detroit";
        public class England {
            public String name = "London";
            public class Ireland {
                public String name = "Dublin";
                public void print_names() {
                    Console.WriteLine(name);
                }
            }
        }
        public static void Main(String[] args) {}
    }

Here, `England` is an inner class of `Usa`, and `Ireland` is an inner
class of `England`. The above is compiled with
[Mono](http://www.go-mono.org)\'s `mcs` for Linux (no options).

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 07 Mar 2003\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
