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
    Page](http://www.program-transformation.org/edit/Stratego/NamingConventions?t=1536825601)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/NamingConventions)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/NamingConventions)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/NamingConventions?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/NamingConventions?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/NamingConventions?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/NamingConventions?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/NamingConventions?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/NamingConventions)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/NamingConventions?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/NamingConventions?template=oopsmore&param1=1.2&param2=1.2)
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
Naming Conventions {#naming-conventions .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Naming conventions are important in any platform. If the naming
conventions are followed in the library and by the developers of a
project, you can remember the name of method, variable or whatever much
better. This increases you productivity and the joy in your work, which
is of course the most important thing in life.

Checking the name of a method in the documentation or source-code is
quite tiresome. If you know the naming-scheme you only have to know the
\'semantic\' name of a method and you don\'t have to worry about the
concrete syntax, which you can compose from the semantic name and the
convention of the platform you are using.

[]{#Syntax} Syntax
------------------

### []{#Strategies_and_rules} Strategies and rules

[Naming conventions](NamingConventions){.twikiLink} can be separated in
conventions for the syntax of a name and conventions for the scheme of a
name for a specific type of strategy. The conventions for the syntax of
a name deal with the usage of dashes, underscores, lowercase, uppercase
and so on. The conventions of the names themselves deal with standard
name construction, indicating the \'kind\' of the item (like is, set and
get in the library of the
[JavaLanguage[^?^](http://www.program-transformation.org/edit/Stratego/JavaLanguage?topicparent=Stratego.NamingConventions)]{.twikiNewLink
style="background : #FFFFCE;"})

In Stratego there are two important conventions for the syntax of names:

-   Names of strategies are written in lowercase where indiviual words
    of the name are separated by dashes. Examples: `int-to-string`,
    `map`, `eval-exp`.
-   Names of rules are written in
    [CamelCase[^?^](http://www.program-transformation.org/edit/Stratego/CamelCase?topicparent=Stratego.NamingConventions)]{.twikiNewLink
    style="background : #FFFFCE;"}. Examples: `EvalExp`, `Desugar`,
    `Inline`, `TcExp`

An exception to the strategy naming convention are strategies that
merely alias or collect rules and do not perform a very interesting
traversal. These strategies may just as well follow the convention for
rule names. Example:\
`ElimDead = ElimDeadFun + ElimDeadRec`\
(where `ElimDeadFun` and `ElimDeadRec` are (possibly
[dynamic](DynamicRule){.twikiLink}) rules).

Futhermore overlays are written like constructors, which are written in
[CamelCase[^?^](http://www.program-transformation.org/edit/Stratego/CamelCase?topicparent=Stratego.NamingConventions)]{.twikiNewLink
style="background : #FFFFCE;"}. Examples: `BinOp`, `VarDec`, `Call`.

### []{#Modules} Modules

to do.

[]{#Naming_scheme} Naming scheme
--------------------------------

A naming scheme is helpful because it is a first indication of the task
of a strategy. For any language holds: be precise and clear but prevent
being to verbose.

### []{#Test_strategies} Test-strategies

The first task that comes in mind is testing. Test-strategies verify
whether the current term satisfies some condition or not.
Test-strategies fail when the term doesn\'t satisfy the condition and
leave the current term untouched otherwise. Test-strategies should be
called `is-*`. Examples: `is-int`, `is-list`, `is-Exp`, `is-Declared`.

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 05 May
2002\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
