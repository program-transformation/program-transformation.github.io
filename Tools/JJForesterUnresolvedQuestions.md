::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
[Home](WebHome){.twikiLink}

**XT Tools**

-   [Reference Docs](ToolReference){.twikiLink}
-   [GPP](GenericPrettyPrinter){.twikiLink}
-   [ATerm](ATermTools){.twikiLink}
-   [SDF](SdfTools){.twikiLink}
-   [AsFix](AsFixTools){.twikiLink}

**Languages**

-   [Stratego](../Stratego/WebHome){.twikiLink}
-   [SDF](../Sdf/WebHome){.twikiLink}
-   [ATerm](ATermFormat){.twikiLink}

**Software**

-   [Stratego/XT](../Stratego/StrategoDownload){.twikiLink}
-   [SDF2 Bundle](../Sdf/SdfBundle){.twikiLink}
-   [KoalaCompiler](KoalaCompiler){.twikiLink}
-   [AutoBundle](AutoBundle){.twikiLink}
-   [AutoBuild](AutoBuild){.twikiLink}
-   [DailyBuildSystem](DailyBuildSystem){.twikiLink}

[![](http://www.program-transformation.org/twiki/pub/rss.gif "RSS 1.0 feed")](http://www.program-transformation.org/twiki/bin/view/Tools/WebRss?skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tools/JJForesterUnresolvedQuestions?t=1536826790)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/JJForesterUnresolvedQuestions)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/JJForesterUnresolvedQuestions)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/JJForesterUnresolvedQuestions?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/JJForesterUnresolvedQuestions?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tools/JJForesterUnresolvedQuestions?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/JJForesterUnresolvedQuestions)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/JJForesterUnresolvedQuestions?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tools/JJForesterUnresolvedQuestions?template=oopsmore&param1=1.1&param2=1.1)
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
JJForester Unresolved Questions {#jjforester-unresolved-questions .twikiTopicTitle}
===============================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

If you are a JJForester user, we would like to know your opinion about
possible modifications to the tool. That\'s what this discussion page is
for.

**Qualified constructor classes**

Industrial application of JJForester has revealed a design flaw.
Currently, the tool puts the generated constructor classes A..Z for a
particular sort S in a subpackage S. Like:

package/sorts/S S/A \... Z

If Java would allow import statements like:

import package/\*;

then the constructor classes could be accessed with:

S.A \... S.Z

But, \.... Java does *not* allow the import of packages, only of
specific classes, or (with \*) of all classes in a package.
Consequently, one must either import all packages for all sorts
separately (leading to name ambiguities if some sorts have constructors
with the same name), or one must fully qualify each usage of a
constructor class (potentially leading to very long qualifications).

As a solution, I propose not to generate the constructor classes in
separate packages per sort anymore, but to generate constructor class
names with the sort name as prefix. As in:

package/sorts/S S\_A \... S\_Z

Consequences:

-   (+) No need for long lists of import statements.
-   (+) No name ambiguities if you import everything in the same scope.
-   ( ) Write S\_X instead of S.X.
-   (-) You can never use constructor class names unqualified anymore.

Questions:

-   Have you experienced the problem?
-   Would you be happy with my proposed soluton?
-   Can you think of a better solution?

Thanks!

\--JoostVisser

------------------------------------------------------------------------

[LeonMoonen[^?^](http://www.program-transformation.org/edit/Tools/LeonMoonen?topicparent=Tools.JJForesterUnresolvedQuestions)]{.twikiNewLink
style="background : #FFFFCE;"} suggested to provide the option between
subpackages per sort and underscores via a command line switch.

------------------------------------------------------------------------

Of course, instead of importing a package you can add it to your class
path, thus making it a root package. Then, ambiguitiy resolution with
S.X works! \--JoostVisser\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
