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
    Page](http://www.program-transformation.org/edit/Tools/ToolReference?t=1536825757)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/ToolReference)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/ToolReference)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/ToolReference?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/ToolReference?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Tools/ToolReference?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Tools/ToolReference?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Tools/ToolReference?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Tools/ToolReference?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Tools/ToolReference?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Tools/ToolReference?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/ToolReference)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/ToolReference?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Tools/ToolReference?template=oopsmore&param1=1.9&param2=1.9)
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
Tool Reference {#tool-reference .twikiTopicTitle}
==============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

### []{#autoxt} autoxt

-   [autoxt](../Stratego/AutoXT){.twikiLink} \-- installs makerules and
    autoconf macros for using XT tools

### []{#Stratego_StrategoCompiler_strc}[]{#_Stratego_StrategoCompiler_strc_} [strc](../Stratego/StrategoCompiler){.twikiLink}

-   [strc](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-strc.html)

### []{#Stratego_StrategoFront_stratego}[]{#_Stratego_StrategoFront_stratego} [stratego-front](../Stratego/StrategoFront){.twikiLink}

-   [parse-stratego](../Stratego/ParseStratego){.twikiLink} \-- parses a
    Stratego module
-   [pp-stratego](../Stratego/PrettyPrintStratego){.twikiLink} \--
    pretty-prints a Stratego module
-   [meta-explode](../Stratego/MetaExplode){.twikiLink} \-- explodes
    concrete object syntax fragments to Stratego

### []{#SdfFront_sdf_front}[]{#_SdfFront_sdf_front_} [sdf-front](SdfFront){.twikiLink}

-   [pack-sdf](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-pack-sdf.html)
    \-- packs a set of SDF2 modules into a single definition
-   pp-sdf \-- pretty prints Stratego.SDF2 in abstract syntax to
    concrete syntax
-   parse-sdf-module and parse-sdf-definition \-- parse an Stratego.SDF2
    definition or module to abstract syntax
-   sdf-desugar and sdf-ensugar \-- remove or add trivial syntactic
    sugar

### []{#SdfTools_sdf_tools}[]{#_SdfTools_sdf_tools_} [sdf-tools](SdfTools){.twikiLink}

-   [parse-unit](ParseUnit){.twikiLink} \-- unit testing of SDF2 syntax
    definitions
-   [gen-renamed-sdf-module](GenRenamedSdfModule){.twikiLink} \--
    generates an SDF module that renames all sorts in an SDF syntax
    definition
-   [sdf2ast-conflicts](SdfToAstConflicts){.twikiLink} \-- generates a
    list of illegal patterns in a AST
-   [sdf2parenthesize](SdfToParenthesize){.twikiLink} \-- generates a
    tool that adds all required parentheses to an AST

### []{#AsFixTools_asfix_tools}[]{#_AsFixTools_asfix_tools_} [asfix-tools](AsFixTools){.twikiLink}

-   [implode-asfix](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-implode-asfix.html)
    \-- implodes a parse tree in AsFix2 format to an [abstract syntax
    tree](../Stratego/AbstractSyntaxTree){.twikiLink}
-   [asfix-yield](AsFixYield){.twikiLink} \-- unparses an AsFix2 parse
    tree to flat text.
-   [visamb](VisualizeAmbiguities){.twikiLink} \-- display the
    ambiguities in a parse tree represented in AsFix2
-   [asfix-anno-comments](AsFixAnnoComments){.twikiLink} \-- put
    comments in annotations of a parse tree

### []{#Stratego_StrategoRegular_strateg}[]{#_Stratego_StrategoRegular_strate} [stratego-regular](../Stratego/StrategoRegular){.twikiLink}

-   [sdf2rtg](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-sdf2rtg.html)
    \-- generates an abstract syntax definition in
    [RTG](../Stratego/RegularTreeGrammar){.twikiLink} from an SDF syntax
    definition.
-   [rtg2sig](RtgToSig){.twikiLink} \-- generates a [Stratego
    signature](../Stratego/StrategoSignature){.twikiLink} from an
    abstract syntax definition in
    [RTG](../Stratego/RegularTreeGrammar){.twikiLink}.
-   [format-check](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/format-checking.html)
    \-- Check if an ATerm is part of the language defined by an
    [RTG](../Stratego/RegularTreeGrammar){.twikiLink}.
-   [rtg2typematch](RtgToTypeMatch){.twikiLink} \-- Generates a
    duck-typing based strategy that checks if an ATerm is of a type
    defined in an [RTG](../Stratego/RegularTreeGrammar){.twikiLink}.

### []{#PtSupport_pt_support}[]{#_PtSupport_pt_support_} [pt-support](PtSupport){.twikiLink}

-   [ambtracker](AmbTracker){.twikiLink} \-- display the productions in
    a parse tree causing ambiguities
-   [implodePT](ImplodeParseTree){.twikiLink} \-- implodes an
    [AsFix2ME](AsFix){.twikiLink} parse tree to an abstact syntax tree
-   [unparsePT](UnParseParseTree){.twikiLink} \-- yields an
    [AsFix2ME](AsFix){.twikiLink} parse tree to a string
-   [addPosInfo](AddPosInfo){.twikiLink} \-- adds position information
    to an [AsFix2ME](AsFix){.twikiLink} parse tree

### []{#Sdf_PGEN_pgen}[]{#_Sdf_PGEN_pgen_} [pgen](../Sdf/PGEN){.twikiLink}

-   [sdf2table](../Sdf/SdfToTable){.twikiLink} \-- generates an sglr
    parse table from an sdf2 syntax definition

### []{#GenericPrettyPrinter_gpp}[]{#_GenericPrettyPrinter_gpp_} [gpp](GenericPrettyPrinter){.twikiLink}

-   [abox2html](AboxToHtml){.twikiLink}
-   [abox2latex](AboxToLaTex){.twikiLink}
-   [abox2text](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-abox2text.html)

<!-- -->

-   [asfix2abox](AsFixToAbox){.twikiLink}
-   [ast2abox](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-ast2abox.html)

<!-- -->

-   [ppgen](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-ppgen.html)
-   [pptable-diff](PrettyPrintTableDiff){.twikiLink}

### []{#ATermTools_aterm_tools}[]{#_ATermTools_aterm_tools_} [aterm-tools](ATermTools){.twikiLink}

-   [term-to-dot](TermToDot){.twikiLink} \-- transforms an ATerm to a
    graph in the [DotLanguage](../Transform/DotLanguage){.twikiLink}
-   [pp-aterm](PpATerm){.twikiLink} \-- pretty prints an ATerm to text
    with whitespace to show the tree structure of the ATerm.

### []{#XmlFront_xml_front}[]{#_XmlFront_xml_front_} [xml-front](XmlFront){.twikiLink}

-   [aterm2xml](ATermToXml){.twikiLink} \-- convert an ATerm to an XML
    document.
-   [xml2aterm](XmlToATerm){.twikiLink} \-- convert an XML document to
    an ATerm.

<!-- -->

-   [parse-xml-doc[^?^](http://www.program-transformation.org/edit/Tools/XmlDocParser?topicparent=Tools.ToolReference)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- parses an XML document to xml-doc
-   [pp-xml-doc[^?^](http://www.program-transformation.org/edit/Tools/XmlDocPrettyPrinter?topicparent=Tools.ToolReference)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- pretty-prints xml-doc to an XML
    document
-   [parse-xml-info](XmlInfoParser){.twikiLink} \-- parses an XML
    document to [xml-info](XmlInfo){.twikiLink}
-   [pp-xml-info](XmlInfoPrettyPrinter){.twikiLink} \-- pretty-prints
    [xml-info](XmlInfo){.twikiLink} to an XML document
-   [data2xml-doc[^?^](http://www.program-transformation.org/edit/Tools/DataToXmlDoc?topicparent=Tools.ToolReference)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- transforms an ATerm to a
    comparable XML document represented in xml-doc.
-   [xml-info2data[^?^](http://www.program-transformation.org/edit/Tools/XmlInfoToData?topicparent=Tools.ToolReference)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- transforms
    [xml-info](XmlInfo){.twikiLink} to a somewhat comparable ATerm

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.ToolReference moved from Stratego.ToolReference on 09 Feb 2004 -
14:51 by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Tools/ToolReference?newweb=Stratego&newtopic=ToolReference&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
