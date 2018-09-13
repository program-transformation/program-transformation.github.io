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
    Page](http://www.program-transformation.org/edit/Stratego/NewName?t=1536825601)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/NewName)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/NewName)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/NewName?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/NewName?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/NewName?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/NewName?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/NewName?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/NewName?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/NewName?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/NewName?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/NewName)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/NewName?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/NewName?template=oopsmore&param1=1.4&param2=1.4)
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
New Name {#new-name .twikiTopicTitle}
========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The `newname` strategy is a variant of the `new` strategy, which
generates a new unique string. Newname generates unique strings, just
like new, but it also accepts a prefix that will be part of the
generated string. By default, the numbering is also done per prefix. For
example, if you apply `newname` three times to the string `"foo"`, then
the results will be `"foo_0"`, `"foo_1"` and `"foo_2"`. If `newname` is
applied to `"bar"` after this, then the result will be `"bar_0"`, not
`"bar_4"`. Thus, The `newname` strategy is very useful for generating
more user-friendly, unique names in a program transformation.

The library strategy `newname` trims any trailing digits up to the
rightmost \'\_\'. Hence, repeated application of `newname` will not
result in mutiple numeric postfixes (for example `a_0_0`)

Example

      <newname> "a"        // produces "a_0"
    ; <newname> "b"        // produces "b_0"
    ; <newname> "b_1"      // produces "b_2"
    ; <newname> "b_1729"   // produces "b_3"
    ; <newname> "b_a"      // produces "b_a_0"

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
