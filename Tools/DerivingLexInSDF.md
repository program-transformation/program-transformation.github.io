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
    Page](http://www.program-transformation.org/edit/Tools/DerivingLexInSDF?t=1536826787)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/DerivingLexInSDF)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/DerivingLexInSDF)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/DerivingLexInSDF?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/DerivingLexInSDF?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Tools/DerivingLexInSDF?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/DerivingLexInSDF?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/DerivingLexInSDF?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/DerivingLexInSDF?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/DerivingLexInSDF?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/DerivingLexInSDF)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/DerivingLexInSDF?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Tools/DerivingLexInSDF?template=oopsmore&param1=1.3&param2=1.3)
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
Deriving Lex In SDF {#deriving-lex-in-sdf .twikiTopicTitle}
===================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

This is one of the XT
[UserStories[^?^](http://www.program-transformation.org/edit/Tools/UserStories?topicparent=Tools.DerivingLexInSDF)]{.twikiNewLink
style="background : #FFFFCE;"}.

    -----------------------------------------------------------------------------

    RECOVERY OF SYNTAX DEFINITION FOR LEX

    -----------------------------------------------------------------------------

    No syntax definition for LEX was available in the grammar-base. In
    order to further automate the translation of LEX/YACC grammars to SDF2
    syntax definitions, such a syntax definition is needed. In this file I
    report the steps I took to get LEX in SDF2.

    -- Eelco Visser 2001/09/29

    -----------------------------------------------------------------------------

    [Step 1] Locate the sources

       ftp://ftp.gnu.org/non-gnu/flex/

    [Step 2] Inspect the source

       cd flex-2.5.4
       less parse.y 

    [Step 3] Copy source to grammar base

       cp parse.y ~/res/XT/gb/grammars/lex.0

    [Step 3] Parse the YACC (Bison) source

    >    parse -l yacc -i lex.y -I -o lex.af 

    =>    Error: charliteral '\n' not recognized. Repair syntax definition of
       YACC.

    [Step 4] Translate to AbstractSDF

    >   parse -l yacc -i lex.y -I -o lex.af 
       yacc2sdf -i lex.af -o lex.asdf 

    [Step 5] Pretty-print syntax definition and inspect

    >   sdf-bracket -i lex.asdf | pp -a -l sdf -o lex.def -v 2.1 
       less lex.def    

    [Step 6] Regularize the syntax definition

    >   parse -l yacc -i lex.y -I -o lex.af 
       yacc2sdf -i lex.af -o lex.asdf 
       sdf-regularize -i lex.asdf -o lex.reg.asdf 
       sdf-bracket -i lex.reg.asdf | pp -a -l sdf -o lex.def -v 2.1 
       less lex.def    

    [Step 7] Generate constructors

    >   parse -l yacc -i lex.y -I -o lex.af 
       yacc2sdf -i lex.af -o lex.asdf 
       sdf-regularize -i lex.asdf -o lex.reg.asdf 
       sdf-cons -i lex.reg.asdf -o lex.reg.cons.asdf
       sdf-bracket -i lex.reg.cons.asdf | pp -a -l sdf -o lex.def -v 2.1 
       less lex.def   

    [Step 8] Edit the definition to define lexical syntax and improve constructors

    [Step 9] Unpack the definition to create separate SDF modules. Make check can then
       be used to generate lex.def and automatically parse various example files.
       Before doing this change the names of the modules Lexical and Generated into
         Lex-Symbols and Lex, respectively.

    >   unpack-sdf lex.def

    [Step 10] Further edit the modules to define lexical syntax.

    =>    It turns rather hard to parse complete lex files. The lexical syntax
       is very tricky. Instead I decide to reduce the problem by editing lex
       files by hand to remove all irrelevant stuff and only leave definitions
       of the form |name re| and rules of the form |re return id;|. Newlines
       cannot be used as general layout, but are used to delimit definitions
       and rules. No superfluous newlines are allowed.

    =>    Succeed in parsing stratego.mod.l, a modified version of the stratego lexical
       syntax in lex.

    [Step 11] Improve the syntax definition to get good abstract syntax. Start with
       unfolding literals.

    >   parse -l sdf -v 2.1 -I -i lex.def -o lex.adef
       unfold-literal -i lex.adef -o lex.unf.adef
       sdf-bracket -i lex.adef | pp -a -l sdf -o lex.def -v 2.1 
       less lex.def   

    =>    Automatic application does not work, do it manually. (come back and
       repair unfold-literal later)

    [Step 12] Abstract syntax looks good. Install parse table such that it can be used with the
       parse tool of the grammar base.

    >    make install
       parse -l lex -i data/stratego.mod.l -I


    [Step 13] Project finished. 

    =>    Future work: 
       - parse full lex definitions
       - generate a signature from the syntax definition

------------------------------------------------------------------------

[CategoryXT[^?^](http://www.program-transformation.org/edit/Tools/CategoryXT?topicparent=Tools.DerivingLexInSDF)]{.twikiNewLink
style="background : #FFFFCE;"} \|
[CategoryUserStory[^?^](http://www.program-transformation.org/edit/Tools/CategoryUserStory?topicparent=Tools.DerivingLexInSDF)]{.twikiNewLink
style="background : #FFFFCE;"} \| \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 29 Sep 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
