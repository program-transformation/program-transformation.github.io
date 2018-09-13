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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoMisc?t=1536825677)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoMisc)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoMisc)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoMisc?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoMisc?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/StrategoMisc?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/StrategoMisc?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoMisc?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoMisc?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoMisc?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoMisc)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoMisc?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoMisc?template=oopsmore&param1=1.3&param2=1.3)
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
Stratego Misc {#stratego-misc .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Introduction} Introduction
------------------------------

[stratego-misc](StrategoMisc){.twikiLink} is a small, but versatile
package of Stratego modules, implementing strategies and tools that are
not (yet) in the SSL.

It might be handy for others as well, so here it is, online.

[]{#Contained_modules} Contained modules
----------------------------------------

Currently, stratego-misc consists of the following modules:

-   **[term-color](StrategoMisc#TermColor){.twikiAnchorLink}**: Produce
    color output in your terminal, directly from Stratego! Very cool
    indeed, handy as well. Distinguish the various parts in the usually
    huge Term-dumps, while debugging, by colorizing them.
-   **[output-control](StrategoMisc#OutputControl){.twikiAnchorLink}**:
    Improved control over (debug-) output. More intuitive verbosity
    levels and nested, tree-like debug-output.
-   **[dynamic-rules-tools](StrategoMisc#DynamicRulesTools){.twikiAnchorLink}**:
    A first approach towards generalizing the various strategies that
    operate on dynamic rules and the tables behind them. Also a
    (debugging-) pretty printer for dynamic rules.

[]{#TermColor}

### []{#Module_term_color} Module term-color

Produce color output in your terminal, directly from Stratego! Very cool
indeed, handy as well. Distinguish the various parts in the usually huge
Term-dumps, while debugging, by colorizing them.

**Sample output (in a regular terminal):**\
![Screenshot of term-color
output](../pub/Stratego/StrategoMisc/screen-term-color.gif)

[]{#OutputControl}

### []{#Module_output_control} Module output-control

Improved control over (debug-) output. More intuitive verbosity levels
and nested, tree-like debug-output.

**Sample output when using so-called output-nests (in a regular
terminal):**\
![Screenshot of output-control
output](../pub/Stratego/StrategoMisc/screen-output-control.gif)

#### []{#Usage} Usage

Use `output-nest(s|text)` for entering a new output-level.

      HandleFunTpSpec =
      output-nest(
        ?FunTpSpec(f, tpF)
      ; rules(Id2Type: f -> tpF)
      | "HandleFunTpSpec")

Use `on-debug(|color, text)` instead of debug:

      <on-debug(|tc-green, "argtypes: ")> tpV'*

The equivalent of `say` is also available: `on-say(|color, text)`.

#### []{#Verbosity} Verbosity

output-control checks whether the `--verbose` flag was set, and defaults
to 0 otherwise. The possible levels are:

      lvlError     = 0    // not used
      lvlInfo      = 1    // not used
      lvlTalkative = 2    // print entering and exiting of output-nests
      lvlChatty    = 3    // id. and print input and output terms of each output-nest
      lvlDebug     = 4    // id. and show any on-debug/on-say output
      lvlVomit     = 5    // not used

#### []{#Practical_usage} Practical usage

Make sure your toplevel strategy supports the `--verbosity` flag (using
`io-wrap`, `output-wrap`, or otherwise).

When piping your program output into `less`, make sure `stderr` is
redirected into `stdout` and `less` is called with color-support:

`[adam@madras:lib>`
`parse-tfof -i test1.tfof | ./TFOF-InferTypes --verbose 4 2>&1 | less -R`

[]{#DynamicRulesTools}

### []{#Module_dynamic_rules_tools} Module dynamic-rules-tools

This has been superseded by `dynamic-rules-refactored` in the SSL, since
the introduction of the new dynamic rules in [Stratego
0.10](StrategoRelease010){.twikiLink}.

[]{#Documentation} Documentation
--------------------------------

Generated documentation by
[xdoc](ExtendibleDocumentationGenerator){.twikiLink} can be found at
<http://catamaran.labs.cs.uu.nl/docs/stratego-misc/api/>

[]{#Download_and_Installation} Download and Installation
--------------------------------------------------------

Interested in using stratego-misc yourself? You can download the latest
working distribution (tar.bz2) here:
[stratego-misc-head.tar.gz](http://losser.st-lab.cs.uu.nl/~mbravenb/dailydist/stratego-misc/src/stratego-misc-head.tar.gz)

Unpack the tarball and configure the package with the usual
\--with-strategoxt, \--with-sdf and \--with-aterm. See the INSTALL file
for detailed instructions.

\-- [ArthurVanDam](../Main/ArthurVanDam){.twikiLink} - 02 Feb 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
