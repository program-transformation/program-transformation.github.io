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
    Page](http://www.program-transformation.org/edit/Stratego/LayoutGuidelines?t=1536825596)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/LayoutGuidelines)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/LayoutGuidelines)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/LayoutGuidelines?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/LayoutGuidelines?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/LayoutGuidelines?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/LayoutGuidelines?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/LayoutGuidelines?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/LayoutGuidelines)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/LayoutGuidelines?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/LayoutGuidelines?template=oopsmore&param1=1.2&param2=1.2)
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
Layout Guidelines {#layout-guidelines .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Good layout is important for the readability and hence maintainability
of programs. This holds for any programming language. Stratego aims at
not only providing a language for *programming* program transformations,
but also doing so in an understandable way. Refactoring is an important
tool to create readable specifications, but good layout is a good
starting point.

Layout is not significant for the semantics. Stratego does *not* use the
offside rule. This means that you can be liberal with placing newlines.

Of course, layout is determined by taste, but experience suggests
several conventions that lead to readable specifications. This page
discusses some conventions. Actual situations may call for other
decisions.

### []{#Principles} Principles

Specifications should be layed out such that they

-   can be printed on standard paper
-   fit on a 80 character display (editor, browser)

### []{#Rules} Rules

Short rules are better than long ones.

Put a short rule on a single line:

       AZ : Plus(Int(0), x) -> x

Split a longer rule into a line with the label and a line with the
left-hand side and right-hand side:

      TrCx : 
        Cx(e, t, f) -> CJUMP(NE, e, CONST(0), t, f)

Indent the label of a rule with two spaces and the left-hand side with
another two. More is a waste of space.

Putting the label on a line by itself makes it stand out, making it
easier to locate. Also it makes the appearance of the text more regular
if all left-hand sides start at the same indentation.

Split long rule over multiple lines

     TrExp : 
        If(e1, e2, e3) ->
        ESEQ([Cx(e1, t, f),
              LABEL(t),
              MOVE(TEMP(tmp), e2),
              JUMP(NAME(done), [done]),
              LABEL(f),
              MOVE(TEMP(tmp), e3),
              LABEL(done)],
             TEMP(tmp))
        where new => t; new => f; new => done; new => tmp

### []{#Strategy_Definitions} Strategy Definitions

For strategies similar guidelines apply.

Put a short definition on a single line.

For a longer definition put the body on the line after the name operator
name

      tr-stm(s, e) =
        MOVE(e,e) + EXP(e) + JUMP(e,id) + CJUMP(id,e,e,id,id) +
        SEQ(s,s) + SEQ(list(s)) + NUL + LABEL(id) + LET(id, e)

### []{#Strategy_Expressions} Strategy Expressions

Organize a long sequential composition (pipeline of transformations)
vertically

      canonicalize-body =
        !SEQ(<id>);
        simplify-ir;
        linearize;
        listify;
        ?SEQ(<id>);
        commute-args;
        basic-blocks;
        trace-schedule;
        clean-up-traces

Sometimes the structure can be clarified by prefixing the semicolon
separator:

      canonicalize-body =
        !SEQ(<id>)
      ; simplify-ir
      ; linearize
      ; listify
      ; ?SEQ(<id>)
      ; commute-args
      ; basic-blocks
      ; trace-schedule
      ; clean-up-traces

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 28 Apr 2002\

------------------------------------------------------------------------

[StrategoGlossary](StrategoGlossary){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
