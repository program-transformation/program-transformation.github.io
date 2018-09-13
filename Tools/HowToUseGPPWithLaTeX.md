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
    Page](http://www.program-transformation.org/edit/Tools/HowToUseGPPWithLaTeX?t=1536826733)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/HowToUseGPPWithLaTeX)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/HowToUseGPPWithLaTeX)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/HowToUseGPPWithLaTeX?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/HowToUseGPPWithLaTeX?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Tools/HowToUseGPPWithLaTeX?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/HowToUseGPPWithLaTeX?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tools/HowToUseGPPWithLaTeX?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/HowToUseGPPWithLaTeX?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/HowToUseGPPWithLaTeX?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/HowToUseGPPWithLaTeX?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/HowToUseGPPWithLaTeX)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/HowToUseGPPWithLaTeX?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Tools/HowToUseGPPWithLaTeX?template=oopsmore&param1=1.5&param2=1.5)
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
How To Use GPPWith La Te X {#how-to-use-gppwith-la-te-x .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Task**

How to use pretty-printed documents in LaTeX.

**Description**

The back-end [abox2latex](AboxToLaTex){.twikiLink} produces LaTeX code
according to the formatting defined in a [Box](BoxLanguage){.twikiLink}
term. In order to process this LaTeX code by latex, the \`boxenv\' style
file is required.

The location of this style file depends on your [GPP](GPP){.twikiLink}
installation but [abox2latex](AboxToLaTex){.twikiLink} includes a
comment section in the generated LaTeX code that tells you where to find
the style file.

A generated LaTeX file can be incorporated in a larger LaTeX document as
follows:

1.  Determine the location of the boxenv style file by inspecting the
    comments at the beginning of example.tex.

<!-- -->

1.  Add this location to your TEXINPUTS environment variable.

<!-- -->

1.  Add \`\\usepackage{boxenv}\' to the preamble of main.tex.

<!-- -->

1.  Import the generated LaTeX file using \`\\input\'.

<!-- -->

1.  Process the file by latex.

The paper [A LaTeX Style File For Formatting BOX
Expressions](http://www.cs.uu.nl/groups/ST/twiki/bin/view/Merijn/PaperALaTeXStyleFileForFormattingBOXExpressions)
contains detailed information about the boxenv style file and its use.

**Changing Fonts**

You can change how text is displayed by LaTeX by redefining macros in a
configuration file \'box-fonts.def\'. The following macros can be
defined:

 KWf:
:   Defines how keywords are formatted (default \'\\textbf{\...}\')

 VARf:
:   Defines how variables are formatted (default \'\\textit{\...}\')

 NUMf:
:   Defines how numbers are formatted (default \'\\textrm{\...}\')

 MATHf:
:   Defines how mathematical symbols are formatted (default
    \'\\ensuremath{\...}\')

 COMMF:
:   Defines how to comments are formatted (default \'\\textrm{\...}\')

**Changing Symbols**

You can instruct [abox2latex](AboxToLaTex){.twikiLink} to map symbols in
an abox term to special LaTeX symbols. To that end, you create an
abbreviations table containing mappings from
[Box](BoxLanguage){.twikiLink} symbols to LaTeX symbols, and pass that
table to [abox2latex](AboxToLaTex){.twikiLink} with the \'-t\' switch.
For example, [abox2latex](AboxToLaTex){.twikiLink} uses the following
default abbreviations table:

       [
         ["->"   , "\\ensuremath{\\rightarrow}"],
         [ "\\/" , "\\ensuremath{\\vee}"],
         [ "/\\" , "\\ensuremath{\\wedge}"],
         [ "=="  , "\\ensuremath{\\equiv}"],
         [ "++"  , "\\ensuremath{+\\kern-.4em+}"]
       ]

**Examples**

The location of boxenv.sty can be appended to your TEXINPUTS environment
variable as follows:

For Bourne shells

     # TEXINPUTS=<boxenv.sty location>:${TEXINPUTS}; export TEXINPUTS

For C shells

     # set TEXINPUTS=<boxenv.sty location>:${TEXINPUTS}; setenv TEXINPUTS

Assuming that the generated LaTeX code is stored in the file
example.tex, then a typical LaTeX document that includes the file
example.tex looks like:

     \documentstyle{article}
     \usepackage{boxenv}
     
     \begin{document}
     \input{example.tex}
     \enddocument}

**Layout Preserving Pretty-Printing with [GPP](GPP){.twikiLink}**

[Abox2latex](AboxToLaTex){.twikiLink} can be used for layout preserving
pretty-printing. To that end, you have to produce an abox term with
[asfix2abox[^?^](http://www.program-transformation.org/edit/Tools/AsFix2Abox?topicparent=Tools.HowToUseGPPWithLaTeX)]{.twikiNewLink
style="background : #FFFFCE;"} and pass it the \'-c\' switch to preserve
layout in the [Box](BoxLanguage){.twikiLink} expression. Then you use
[abox2latex](AboxToLaTex){.twikiLink} with the \'\--alltt\' switch to
produce a LaTeX alltt environment:

     asfix2abox -c -i <your_file>.asfix \
     abox2latex --alltt -o <your_file>.tex

Then you include the \'alltt\' and \'boxenv\' style files in your
document, and input \'\<your\_file\>.tex:

     \documentclass{article}
     \usepackage{alltt}
     \usepackage{boxenv}

     \begin{document}
     \input{<your_file>.tex}
     \end{document}

**See Also**

[GenericPrettyPrinter](GenericPrettyPrinter){.twikiLink},
[HowToPrettyPrintAGrammar](HowToPrettyPrintAGrammar){.twikiLink},
[AboxToLaTex](AboxToLaTex){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
