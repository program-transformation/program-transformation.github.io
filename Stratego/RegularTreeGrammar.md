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
    Page](http://www.program-transformation.org/edit/Stratego/RegularTreeGrammar?t=1536825662)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/RegularTreeGrammar)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/RegularTreeGrammar)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/RegularTreeGrammar?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/RegularTreeGrammar?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/RegularTreeGrammar?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/RegularTreeGrammar?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/RegularTreeGrammar?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/RegularTreeGrammar?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/RegularTreeGrammar?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/RegularTreeGrammar?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/RegularTreeGrammar)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/RegularTreeGrammar?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/RegularTreeGrammar?template=oopsmore&param1=1.4&param2=1.4)
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
Regular Tree Grammar {#regular-tree-grammar .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A regular tree grammar defines a regular tree language. Regular tree
grammars are widely applied as tools in formal reasoning, but in
practice the basic formalism is hidden in languages designed at human
users. The **RTG** language is a little language that just contains the
constructs of the clean formalism. The language is probably best
introduced by a tiny example:

    regular tree grammar
    start Exp
    productions
      Var -> Var   (<string>)
      Exp -> Int   (<int>)
           | Times (Exp, Exp)
           | Plus  (Exp, Exp)
           | Call  (Var, ExpList)

      ExpList -> <cons> (Exp, ExpList)
           | <nil> ()

A regular tree grammar consists of a list of start non-terminals and a
list of productions. The list of start non-terminals defines what
non-terminals are allowed at the root of tree in the language defined by
this RTG. The productions specify the terms that can be produced for a
certain non-terminal. The left-hand-side of a production is
non-terminal, the right hand side is a term that can contain
non-terminals.

Formally, a regular tree grammar consists of:

-   An unranked alphabet of non-terminals: N
-   A ranked alphabet of terminals: T
-   A set of start symbols S, which is a subset of N
-   A set of productions of the form N -\> t, where t is an element of
    the set of ground terms over T union N.

For more formal discussion on tree grammars and tree languages see [Tree
Automata Techniques and
Applications[^?^](http://www.program-transformation.org/edit/Stratego/Thttpwwwgrappauniv-lille3frtata?topicparent=Stratego.RegularTreeGrammar)]{.twikiNewLink
style="background : #FFFFCE;"} or [Connecting XML Processing and Term
Rewriting with Tree
Grammars](ConnectingXMLProcessingAndTermRewritingWithTreeGrammars){.twikiLink}.

Notice that the regular tree grammar shown above contains a few
constructs between angle brackets: `<cons>`, `<nil>`, `<string>`, and
`<int>`. The first two are built-in *terminals* for representing lists.
The last two are built-in non-terminals for strings and integers.

See also:

-   [stratego-regular](StrategoRegular){.twikiLink} (the subpackage of
    StrategoXT that implements RTG)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
