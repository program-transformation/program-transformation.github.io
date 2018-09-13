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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerFiboDotNetSource?t=1536826465)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerFiboDotNetSource)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerFiboDotNetSource)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerFiboDotNetSource?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerFiboDotNetSource?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilerFiboDotNetSource?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilerFiboDotNetSource?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilerFiboDotNetSource?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilerFiboDotNetSource?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompilerFiboDotNetSource?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerFiboDotNetSource)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerFiboDotNetSource?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerFiboDotNetSource?template=oopsmore&param1=1.3&param2=1.3)
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
Decompiler Fibo Dot Net Source {#decompiler-fibo-dot-net-source .twikiTopicTitle}
==============================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This is a simple program, compiled with the Mono C\# compiler, no
optimisation.

Here is the original C\# source code:

    using System;

    class Fibo {
        private static int fib (int x) {
            if (x > 1)
                return (fib(x - 1) + fib(x - 2));
            else return (x);
        }

        public static int Main( String[] args) {
        int number = 0, value;

            try {
                number = Convert.ToInt32(args[0]);  
            } catch (Exception e) {
                Console.WriteLine ("Input error");
                return 1;
            }
            value = fib(number);
            Console.WriteLine ("fibonacci({0}) = {1}", number, value);
            return 0;
        }
    }

You use the program like this:

    % mono Fibo 10
    fibonacci(10) = 55
    % mono Fibo abc
    Input error
    %

The corresponding Java source code (for bytecode decompiler tests) is in
[DecompilerFiboTestSource](DecompilerFiboTestSource){.twikiLink}.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 06 Mar 2003\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
