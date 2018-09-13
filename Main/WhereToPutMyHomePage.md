::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[WebHome](WebHome){.twikiLink}**\
[Transformation](../Transform/WebHome){.twikiLink}\
[GPCE](../Gpce/WebHome){.twikiLink}\
\
[Stratego/XT](../Stratego/WebHome){.twikiLink}\
[Tiger](../Tiger/WebHome){.twikiLink}\
[Tools](../Tools/WebHome){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Main/WhereToPutMyHomePage?t=1536826357)
-   [Rename
    Page](http://www.program-transformation.org/rename/Main/WhereToPutMyHomePage)
-   [Attach
    File](http://www.program-transformation.org/attach/Main/WhereToPutMyHomePage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Main/WhereToPutMyHomePage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Main/WhereToPutMyHomePage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Main/WhereToPutMyHomePage?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Main/WhereToPutMyHomePage?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Main/WhereToPutMyHomePage?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Main/WhereToPutMyHomePage?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Main/WhereToPutMyHomePage?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Main/WhereToPutMyHomePage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Main/WhereToPutMyHomePage?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Main/WhereToPutMyHomePage?template=oopsmore&param1=1.3&param2=1.3)
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
Where To Put My Home Page {#where-to-put-my-home-page .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Program-Transformation.Org
:::

OK, I have to ask this now.

Should my home page ([MikeVanEmmerik](MikeVanEmmerik){.twikiLink}) be in
web Main or web Transform? Everyone elses seems to have been created in
Transform, but when I registered (just after the Sep 2001 upgrade), I
ended up in Main.

It seems to be a nuisance; I have to call myself Main.MikeVanEmmerik,
and I can\'t seem to become a member of
[CategoryPeople](../Transform/CategoryPeople){.twikiLink}.

If I need to move, is there an easy way to do this?

\-- [MikeVanEmmerik](MikeVanEmmerik){.twikiLink} - Tue, 27 Nov 2001

The problem is caused by the way TWiki deals with user registrations.
When registering as a *user* in
[TWikiRegistration](../TWiki/TWikiRegistration){.twikiLink} the
registration script creates a new page in the Main web. Registration
will fail when a page with the user name already exists, since it will
assume that the user registered before.

On the other hand we want to create pages *about* people in the
[ProgramTransformation](../Transform/ProgramTransformation){.twikiLink}
field. If we would put these pages in the Main web they would not be
able to join the twiki as a user later.

The list in [CategoryPeople](../Transform/CategoryPeople){.twikiLink}
only contains `CategoryPeople` pages in the Transform web. This could be
improved.

The current approach is to put a page in the Transform web as well and
let that one point to your Main page.

\-- [EelcoVisser](EelcoVisser){.twikiLink} - 27 Nov 2001\

------------------------------------------------------------------------

[CategoryWiki](../Transform/CategoryWiki){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
