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
    Page](http://www.program-transformation.org/edit/Tools/FromStrategoInYaccToStrategoInSDF?t=1536826226)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/FromStrategoInYaccToStrategoInSDF)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/FromStrategoInYaccToStrategoInSDF)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/FromStrategoInYaccToStrategoInSDF?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/FromStrategoInYaccToStrategoInSDF?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/FromStrategoInYaccToStrategoInSDF?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/FromStrategoInYaccToStrategoInSDF?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/FromStrategoInYaccToStrategoInSDF?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/FromStrategoInYaccToStrategoInSDF)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/FromStrategoInYaccToStrategoInSDF?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/FromStrategoInYaccToStrategoInSDF?template=oopsmore&param1=1.2&param2=1.2)
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
From Stratego In Yacc To Stratego In SDF {#from-stratego-in-yacc-to-stratego-in-sdf .twikiTopicTitle}
========================================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

This is one of the XT
[UserStories[^?^](http://www.program-transformation.org/edit/Tools/UserStories?topicparent=Tools.FromStrategoInYaccToStrategoInSDF)]{.twikiNewLink
style="background : #FFFFCE;"}

    ----------------------------------------------------------------------

    RECOVERING A SYNTAX DEFINITION FOR STRATEGO

    ----------------------------------------------------------------------

    This directory contains a syntax definition in SDF2 of the Stratego
    language. This file describes step by step how the syntax definition
    was obtained from the YACC source in the source tree of the Stratego
    Compiler SC.  Including the search for tools, their usage, repair if
    necessary and the occasional implementation of a missing tool.

    -- Eelco Visser 1/10/2001

    ----------------------------------------------------------------------

    [step 1] Copy the YACC file

    >   cp ../../sc/spec/syn/stratego.grm .   

    [step 2] Parse the YACC file

    >   parse -l yacc -i stratego.grm -I -o stratego.af 

    [step 3] Translate YACC to SDF

    >   yacc2sdf -i stratego.af -o stratego.asdf   
      
    [step 4] Pretty-print the syntax definition

    >   pp -l sdf -i stratego.asdf -o stratego.def 

    [step 4a] Find out what is wrong

    >   pp -h  

    =>    -a switch should be used to indicate that input is 
       abstract syntax

    [step 4c] Pretty-print the syntax definition with -a 

    >   pp -a -l sdf -i stratego.asdf -o stratego.def
       No pp entry found for: ["Definition"]
       rewriting failed 

    =>    wrong pretty-print table              

    [step 4d] Pretty-print the syntax definition with -a and sdf version 2.1

       pp -a -l sdf -i stratego.asdf -o stratego.def -v 2.1 

    [step 5] Inspecting the generated syntax definition

    >   less stratego.def   

    =>    No templates for lexicals have been included. I remember that
       these were generated automatically from the %token declarations
       in the YACC file.
       
    =>    Yes, yacc2sdf is broken; the signature of trees produced
       by the parse has been changed. Repair
       this.

    =>    Problem was due to change in generation of constructors by
       sdf-cons. Adapted Yacc syntax definition; inlined injection
       Nmno* -> Nlist.

    [Step 6] Repeat steps 1 - 5

    >   parse -l yacc -i stratego.grm -I -o stratego.af 
       yacc2sdf -i stratego.af -o stratego.asdf 
       pp -a -l sdf -i stratego.asdf -o stratego.def -v 2.1  
       less stratego.def    

    =>    Each template rule for token is put in its own lexical
       syntax section; merge these. Adapt yacc2sdf

    [Step 7] Repeat step 6

    >   parse -l yacc -i stratego.grm -I -o stratego.af 
       yacc2sdf -i stratego.af -o stratego.asdf 
       pp -a -l sdf -i stratego.asdf -o stratego.def -v 2.1  
       less stratego.def    

    =>    Lexicals are now merged

    =>    No list detection and transformation is done by
       yacc2sdf. Which tool does achieve that? 
        There used to be a deyaccification tool, which I can
       no longer find. 
        Write a new tool: sdf-regularize which achieves this.
       Add it to the sdf-tools package.

    =>    sdf-regularize recognizes various kinds of lists and
       optional constructs and translates them into regular 
       expressions. The sorts representing these regular expressions
       are then superfluous. By inlining their definitions the
       sorts are removed and the syntax definition is shortened.

    [Step 8] Add application of sdf-regularize and sdf-bracket

    >   parse -l yacc -i stratego.grm -I -o stratego.af 
       yacc2sdf -i stratego.af -o stratego.asdf 
       sdf-regularize -i stratego.asdf -o stratego.reg.asdf 
       sdf-bracket -i stratego.reg.asdf \
          | pp -a -l sdf -o stratego.def -v 2.1  
       less stratego.def  

    =>    The syntax definition looks good now, with much
       fewer productions. No definition for lexical syntax
       exists yet, however.

    [Step 9] Generate constructor annotations

    >   parse -l yacc -i stratego.grm -I -o stratego.af 
       yacc2sdf -i stratego.af -o stratego.asdf 
       sdf-regularize -i stratego.asdf -o stratego.reg.asdf 
       sdf-cons -i stratego.reg.asdf -o stratego.reg.cons.asdf
       sdf-bracket -i stratego.reg.cons.asdf \
          | pp -a -l sdf -o stratego.def -v 2.1 
       less stratego.def    

    =>    This produces bad results, since the heuristics are
       based on the literals in the productions; we need
       to add in the literals. Can this be done automatically?

    [Step 10] Find the LEX file

    >   cp ../../sc/spec/syn/stratego.lx . 

    =>    This looks like it could be translated into SDF2 mostly
       automatically.
       Let's find a Lex grammar. There is none in the grammar base.
       I guess we'll have to reverse engineer it.

    =>    Created a syntax definition for a subset of LEX that can deal
       with stripped files that only contain definitions and rules,
       but not arbitrary C code. The file stratego.mod.l contains
       the stripped off lex file for stratego.

    =>   The syntax definition for lex has been installed in the
       grammar base. We can now use the parse tool to parse stratego.mod.l

    [Step 11] Parse the LEX file

    >   parse -l lex -i stratego.mod.l -o stratego.mod.af -I  

    [Step 12] Translating LEX to SDF2

    =>    There is no tool for this yet. We'll have to write it.

    =>    lex2sdf is new tool, implemented in grammar-recovery/src/yacc2sdf/

    >   parse -l lex -i stratego.mod.l -o stratego.mod.af -I  
       lex2sdf -i stratego.mod.af -o stratego.mod.asdf 
       sdf-bracket -i stratego.mod.asdf \
          | pp -a -l sdf -o stratego.mod.sdf -v 2.1 
       less stratego.mod.sdf    

    =>    This provides a good lexical syntax. Note that layout is missing.

    [Step 13] Recapitulation. The following actions were taken to derive
       the SDF2 definition so far. Note that the source file names
       have been renamed

    >   mv stratego.grm stratego.l
       mv stratego.mod.l stratego.l

    =>    Context-free syntax

    >   parse -l yacc -i stratego.y -I -o stratego-cfg.af 
       yacc2sdf -i stratego-cfg.af -o stratego-cfg.asdf 
       sdf-regularize -i stratego-cfg.asdf -o stratego-cfg.reg.asdf 
       sdf-bracket -i stratego-cfg.reg.asdf \
          | pp -a -l sdf -o stratego-cfg.def -v 2.1 
       less stratego-cfg.def

    =>   Lexical syntax

    >   parse -l lex -i stratego.l -o stratego-lex.af -I  
       lex2sdf -i stratego-lex.af -o stratego-lex.asdf 
       sdf-bracket -i stratego-lex.asdf \
          | pp -a -l sdf -o stratego-lex.def -v 2.1
       less stratego-lex.def

    [Step 14] Combine lexical and context-free syntax

    =>   edit: remove module Lexical from stratego-cfg.def

    >    unpack-sdf stratego-cfg.def
        unpack-sdf stratego-lex.def

    =>   edit: repair error in definition of Backslash

    >    pack-sdf -i Main.sdf -I ./. -dep stratego.af

    [Step 14] Unfold literals; replace token names by their definitions.

    >    pack-sdf -i Main.sdf -I ./. -dep stratego.af -o stratego.af
       pp -A -l sdf -i stratego.af -o stratego.def -v 2.1
       
    >   parse -l sdf -v 2.1 -i stratego.def -o stratego.af -I
       unfold-literal -i stratego.af -o stratego.unf.af
       sdf-bracket -i stratego.unf.af \
          | pp -a -l sdf -o stratego.unf.def -v 2.1
       less stratego.unf.def

    =>    unfold-literals did not work for all cases. Rewrote the tool using
       dynamic rules, which made the specification much shorter.

    =>    Use the result as the new Lexical.sdf and Stratego.sdf modules

    >    unpack-sdf stratego.unf.def 

    [Step 15] Clean up Lexical.sdf and Stratego.sdf manually

    =>   Fill in missing lexical syntax
       - layout definitions (in particular definition of literate comments)

    =>    Improve abstract syntax
       - unfold Optvarlist in StrategyDef
       - observations: often better to unfold optionals if the optional can
       also be expressed in terms of the 
       - example: the condition |where id| is equivalent to a rule without condition
       - example: the strategy definition |f = s| is equivalent to |f() = s|, i.e.,
         with an empty list of arguments
       - therefore the latter can be desugared into the former allowing uniform treatment
         without having to deal with None and Some constructors.
       - this is at the cost of extra productions, however, the *core* syntax is
         smaller

    =>   Add constructors

    >   make check

    =>    Stratego files get parsed correctly it seems

    [Step 16] Compatability with parse-mod. To use the parser based on the SDF2 definition
       it should be compatible with the existing YACC based parser.

    =>    Set up a test script that checks compatability between SDF and YACC based parsers

    =>   In order to achieve this abstract syntax trees should be desugared. 

    =>    In order to implement a desugarer we need the signature of trees produced by
       the new parser.

    [Step 17] Derive the signature of Stratego from the syntax definition

    >    parse -l sdf -v 2.1 -I -i stratego.def -o stratego.adef
        sdf2sig -i stratego.adef -o stratego.ar
        ast2abox -p /home/visser/res/app/tiger/tmp/front-tiger-0.2/sig/stratego.pp -i  stratego.ar -o stratego.ar.abox
        abox2text -i stratego.ar.abox -o stratego.r
        unpack stratego.r r                         
       less stratego.r                    

    =>    Inspecting the signature unveiled a couple of wrong constructor names (forgot about
       Var and SVar)

    [Step 18] Added reject rules for reserved words

    =>    The performance of generated parsers was not very good and that time was spent
       filtering syntax trees. It occurred to me that I had not declared the reserved 
       words of the Stratego. Added productions of the from |"keyword" -> Id {reject}|
       for all reserved words.

    =>    Module names used in import sections are allowed to be reserved words except
       for "rules", "strategies", "signature", and "overlays". Created separate lexical
       sort ModName to reflect this.

    [Step 19] Add stratego.0.6.2 to the grammar base.

    [Step 20] Project finished. Future work:

    =>   Improve the pretty-print table to obtain beautyfier for Stratego specifications.

------------------------------------------------------------------------

[CategoryXT[^?^](http://www.program-transformation.org/edit/Tools/CategoryXT?topicparent=Tools.FromStrategoInYaccToStrategoInSDF)]{.twikiNewLink
style="background : #FFFFCE;"} \|
[CategoryUserStory[^?^](http://www.program-transformation.org/edit/Tools/CategoryUserStory?topicparent=Tools.FromStrategoInYaccToStrategoInSDF)]{.twikiNewLink
style="background : #FFFFCE;"} \| \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 01 Oct 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
