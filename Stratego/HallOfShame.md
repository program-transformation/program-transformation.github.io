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
    Page](http://www.program-transformation.org/edit/Stratego/HallOfShame?t=1536825586)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/HallOfShame)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/HallOfShame)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/HallOfShame?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/HallOfShame?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/HallOfShame?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/HallOfShame?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/HallOfShame?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/HallOfShame)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/HallOfShame?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/HallOfShame?template=oopsmore&param1=1.2&param2=1.2)
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
Hall Of Shame {#hall-of-shame .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

This is an overview of the most horrible Stratego code that has been
written. Feel free to add your own code! ;)

[]{#Tuples_and_Concrete_Object_Synta} Tuples and Concrete Object Syntax
-----------------------------------------------------------------------

If you don\'t want anyone to understand your code:

-   don\'t use whitespace,
-   use tuples, preferable in combination with Snd and Fst,
-   switch from quotation to anti-quotation as much as possible

<!-- -->

      ![ %>[ <%, <[ !%><a href=<% Snd %>><% Fst %></a><% | map(!%>| <a href=<% Snd %>><% Fst %></a><%) ]> ,%> ]<% ]

(author: [RobVermaas](../Main/RobVermaas){.twikiLink})

[]{#Combining_Term_wrap_and_Term_pro} Combining Term wrap and Term project
--------------------------------------------------------------------------

To transform a java method term to a string using term wraps and term
projections:

    <?Id(<!String([Chars(<id>)])>)>fname

(author: [ReneDeGroot](../Main/ReneDeGroot){.twikiLink})\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
