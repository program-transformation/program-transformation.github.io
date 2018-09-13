::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/RigiFAQ?t=1536826552)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RigiFAQ)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RigiFAQ)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RigiFAQ?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RigiFAQ?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/RigiFAQ?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/RigiFAQ?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/RigiFAQ?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/RigiFAQ?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/RigiFAQ?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/RigiFAQ?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RigiFAQ)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RigiFAQ?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/RigiFAQ?template=oopsmore&param1=1.7&param2=1.7)
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
Rigi FAQ {#rigi-faq .twikiTopicTitle}
========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Rigi Q&A**

In this document the following tools are frequently mentioned:

-   `sortrsf` (See [SortRSF](SortRSF){.twikiLink})
-   `htmlrsf` (See [HtmlRSF](HtmlRSF){.twikiLink})
-   `rigiedit` (See [RigiEdit](RigiEdit){.twikiLink})

------------------------------------------------------------------------

*Q:* `rigiedit` is dog-slow on my machine. Everyting takes for ever.
(E.g., it takes a couple of seconds before a node gets selected when I
click on it. \-- [HolgerKienle](HolgerKienle){.twikiLink}

*A:* This is a problem with Rigi and modern window managers (KDE,
gnome). I have no idea, how to fix this problem. With KDE 1, you could
get the original speed by hiding the start bar, but that doesn\'t work
with KDE 2 any more. If you need Rigi at top speed, use an old window
manager or non at all (or fix Rigiedit). \--
[JohannesMartin](JohannesMartin){.twikiLink}

*A2:* I was using fvwm2, which was fine with Red Hat 7.1 and Debian
(potato?) (apart from a little trickery with getting the right versions
of two libraries), but that hasn\'t been working with Red Hat 7.2 or
7.3. However, windowmaker (command \"wmaker\") and twm do work under Red
Hat 7.2. \--EvavanEmden

------------------------------------------------------------------------

*Q:* When I load a graph (i.e., an [RSF](RSF){.twikiLink} file) in
`rigiedit`, I get funny error messages, such as \"Unknown arc type
(xxx)\".

*A:* You trying to load an [RSF](RSF){.twikiLink} file in the wrong
domain. For example, if the [RSF](RSF){.twikiLink} file has been
generated with `cparse`, you first have to select the *cparse* domain in
`rigiedit` before loading. See also [RigiRSF](RigiRSF){.twikiLink}. \--
[HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

*Q:* When I load a graph (i.e., an [RSF](RSF){.twikiLink} file) in
`rigiedit`, I get error messages on the console that look as follows:

``

-   -   rigiedit alert: [RSF](RSF){.twikiLink} file is missing \"Root\"
        as root node.
    -   rigiedit alert: Reading file as unstructured
        [RSF](RSF){.twikiLink}.
    -   rigiedit alert: Readrsf(), arctype \"uml-sample.cc,1,7\" unknown
    -   \...

*A:* You are trying to load an [RSF](RSF){.twikiLink} file that is in
the wrong format. `rigiedit` cannot read \"4-tuple unstructured
[RSF](RSF){.twikiLink}\". See [RigiRSF](RigiRSF){.twikiLink} for an
explanation of the file formats. \--
[HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

*Q:* What is the difference between the domain c and *cparse*? \--
[HolgerKienle](HolgerKienle){.twikiLink}

*A:* The c domain is obsolete. Back in 1996 I started fixing the C
parser and that made it necessary to change the domain. So not to cause
any compatibility problems, we created a new domain. \--
[JohannesMartin](JohannesMartin){.twikiLink}

------------------------------------------------------------------------

*Q:* I want to use the feature in `rigiedit` that enables me to see
source code displayed as [HTML](HTML){.twikiLink} file. If I choose
\"Open [URL](URL){.twikiLink}\" in `rigiedit` nothing happens. \--
[HolgerKienle](HolgerKienle){.twikiLink}

*A:* You need to know the following:

-   You first have to generate the [HTML](HTML){.twikiLink} files. See
    [HtmlRSF](HtmlRSF){.twikiLink} for how to do this.
-   You have to set `$WEBROOT` to point to the directory that contains
    the [HTML](HTML){.twikiLink} files. `rigiedit` prepends this
    configuration variable to all [URLs](URL){.twikiLink}. The setting
    of this variable is typically something like
    `file:///home/kienle/mysources/`.
-   You have to set `$WEBBROWSER`. The browser to be called is specified
    using this variable. There seems to be some bug in Rigi (maybe
    caused by the changeover to tcl/tk 8.x) that appends a `-catch`
    parameter to the command line. Also netscape -remote (the default
    setting) does not seem to work properly any more. The following
    works seems to work: `konqueror %s ; exec echo` (Linux) or
    `netscape %s ; exec echo`. (The latter might produce a netscape
    error message, which can be ignored, push OK). It takes a long time
    for netscape to start up. A more convenient way is to use `lynx`.
    For this, use the following setting: `xterm -e lynx %s ; exec echo`.
-   Once this is done, you should be able to use the feature by
    selecting \"Open [URL](URL){.twikiLink}\" from the Node/Arc menu.
    See [RigiUserManual](RigiUserManual){.twikiLink} Sections 4.10.8 and
    4.11.6.
-   See also <http://home.netscape.com/newsref/std/x-remote.html> \--
    [JohannesMartin](JohannesMartin){.twikiLink} /
    [HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

*Q:* How can I open up the corresponding source code from Rigiedit? \--
Carlos Loria Saenz

*A:* Rigi shows an additional menu option \"Edit source\" in the context
window of a node when the following conditions are satisfied:

-   the node has a \"file\" attribute naming the source file
-   that source file exists in the directory `SRCDIR` where `SRCDIR` is
    specified in the Rigi configuration

The Rigi configuration setting `TEXTEDITOR` specifies the command that
is used to open the source file.

Using the optional `lineno` attribute, you can specify at which
linenumber the file should be opened. The string `%d` in the
`TEXTEDITOR` setting will be replaced by the line number on invocation
of the editor.

As an alternative, you can also specify a [URL](URL){.twikiLink} to open
when a node is double-clicked. Details can be found in this FAQ. \--
[JohannesMartin](JohannesMartin){.twikiLink}

------------------------------------------------------------------------

*Q:* In the C and C++ [HTML](HTML){.twikiLink} documentation there is a
section \"Node Names\" that says that they should look like `xx^yy^zz`,
but when I look at my [RSF](RSF){.twikiLink} file I do not see names
like that. \-- [HolgerKienle](HolgerKienle){.twikiLink}

*A:* This has recently been changed. You are probably looking at an old
[RSF](RSF){.twikiLink} file. These new names are now consistently
generated by `cparse` and `vacppparse`.

The benefit of this naming scheme is that filtering is much easier. For
example, you can remove all the standard library nodes by using
`rcl_grep`.

BTW, `rigiedit` does not \"unparse\" the names to obtain information
about the source file, line number etc. This information is still
obtained with the `lineno` and `file` attribute (if present). \--
[JohannesMartin](JohannesMartin){.twikiLink} /
[HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

*Q:* What does it mean if an arc type is defined without source and
target nodes? For example, in the *cparse* domain there are 3 such arcs:
`level`, `composite`, and `multiarc`.

*A:* This means that source and destination can have any type. The
following two lines seem to be equivalent:

-   -   `someArc`
    -   `someArc Unknown Unknown`

See [RigiUserManual](RigiUserManual){.twikiLink}, Section 4.4.1. (The
explanations there are not really enlightning\...) \--
[JohannesMartin](JohannesMartin){.twikiLink} /
[HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

*Q:* The Rigi C++ parser ( `vacppparser` ) generates 4-tuple
unstructured [RSF](RSF){.twikiLink}. When I try to load such a file into
`rigiedit`, it complains because it does not understand this format.
What should I do? \-- [HolgerKienle](HolgerKienle){.twikiLink}

*A:* Simple, once you know that `sortrsf` transforms 4-tuple
unstructured [RSF](RSF){.twikiLink} into (3-tuple) unstructred
[RSF](RSF){.twikiLink} as a side effect of the sorting. `rigiedit`
unstands this format. Simply run `sortrsf < in.4.rsf > out.3.rsf`. (When
you load `out.3.rsf` in `rigiedit`, it gives a warning at the command
line, which can be ignored.) \--
[HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

*Q:* I want to transform a file from 4-tuple unstructured
[RSF](RSF){.twikiLink} to (3-tuple) unstructured [RSF](RSF){.twikiLink}.
I know that I can use `sortrsf` to do this, but is has the side effect
that the file gets sorted and duplicate entries get reomoved. I do not
want that! \-- [HolgerKienle](HolgerKienle){.twikiLink}

*A*: Well, from what I understand, this transformation simply means to
drop the 4th component of the [RSF](RSF){.twikiLink} file. Thus, use a
bit of Unix magic:

-   `out -f1-3 < in.4.rsf > out.3.rsf`

\-- [HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

*Q:* Why is so much postprocessing of the [RSF](RSF){.twikiLink} files
necassary that the parser? Shouldn\'t this take already place in
`vacppparser` resp. `cparse`? (See [RigiRCL](RigiRCL){.twikiLink}) \--
[HolgerKienle](HolgerKienle){.twikiLink}

*A:* No. The preprocessing takes away detail and creates a specific
structure in the graph. It is the structure and content that **we** are
usually interested in, but other people might be interested in other
stuff. For example, we filter out all of the standard library, but other
people might be interested in what parts of the standard library are
used. \-- [JohannesMartin](JohannesMartin){.twikiLink}

------------------------------------------------------------------------

*Q:* When I load a (unstructured) [RSF](RSF){.twikiLink} file in
rigiedit, I get error messages such as the following one:

    rigiedit alert: fscans(), buffer overflow, contents are
    ...(huge name)...

What\'s wrong? \-- [HolgerKienle](HolgerKienle){.twikiLink}

*A:* This is currently the expected behaviour. (The parser creates very
long names, especially when templates are involved; Rigi doesn\'t like
that). It is \'safe\' to ignore these errors. \--
[JohannesMartin](JohannesMartin){.twikiLink}

------------------------------------------------------------------------

*Q:* Why aren\'t my node id\'s coming out right? If I define a node like
this: type 23!name Class it shows up in Rigi exactly that way.
\--EvavanEmden

*A:* Sorry, that\'s an omission in the [RSF](RSF){.twikiLink}
documentation. I just fixed that.

You need to start your rsf file with the definition of the root node,
and then connect your root node to every node on the top level of the
graph using a level arc (i.e. to all other nodes if you have a flat
graph).

Example:

    type    10!Root Function
    type    14!a    Function
    level   10!Root 14!a
    type    15!a    Function
    level   10!Root 15!a
    calls   14!a    15!a

\--JohannesMartin

In other words, you can\'t have any node id\'s in your rsf unless it\'s
structured rsf, in which case you have to have a root node defined and
level relationships for all your nodes. \--EvavanEmden

------------------------------------------------------------------------

*Q:* I can get a filter effect by using rcl\_filter\_nodetype method on
the command line, but it doesn\'t apply until I hit apply on the node
filter dialog box. How can I get rcl\_filter\_apply to work?
\--EvavanEmden

*A:*

rcl\_filter\_nodetype \"nodetype\" \"nnn\", where \"nodetype\" specifies
the node type (case sensitive), and \"nnn\" specifies window number

rcl\_filter\_apply \"nnn\" \[arc\|node\|any\] where \[arc\|node\|any\]
specifies which filters to apply, and \"nnn\" specifies window number

Example

            rcl_filter_nodetype Function 1

            rcl_filter_apply 1 node

\--JohannesMartin

------------------------------------------------------------------------

*Q:* I\'m finding rigiedit (version 5.5.0 for Linux) crashes
unpredictably on repeated node creation. \--EvavanEmden

*A:* [JohannesMartin](JohannesMartin){.twikiLink} found and fixed the
bug that was apparently causing this and sent me a new binary. Should be
included in the next version I imagine. \--EvavanEmden

------------------------------------------------------------------------

*Q:* I\'m running up against the 500 node limit for my layout again.
I\'m sure my machine can handle some more nodes without a totally
impossible delay\... is there any possibility of changing this? How did
they get around this for the SQL demo? \--EvavanEmden

*A:* As far as I know, the 500-node limit applies only to the sugiyama
layout. The spring layout should work with larger graphs, too (and
that\'s the layout that was used for the SQL demo).

The 500-node limit for the sugiyama layout was introduced not only for
memory/speed but also a visualization contraint. With so many nodes, the
graph just doesn\'t show you a whole lot any more. You might be better
off breaking it down before you try the visualization.

Anyways, you should be able to increase the limit by changing the SIZE
constant in plugins/sugiyama/def.h. \--JohannesMartin

Follow-up: Changing the above value and recompiling worked. If anyone
else wants to do something similar, the Rigi source code is available by
special request. \--EvavanEmden

------------------------------------------------------------------------

*Q:* When I run a RCL (or tcl) command in `rigiedit` I cannot see the
output it generates. For example, `rcl_env_get RIGILIB` shows me
nothing. How can I see the output? \--
[HolgerKienle](HolgerKienle){.twikiLink}

*A:* Send the output to a message window with
`demo_msg [rcl_env_get RIGILIB]` or to stdout with
`puts [rcl_env_get RIGILIB]`. \--
[HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

*Q:* When I run `rigiparse` I get the error \"rsx not found, DPMI not
supported by emx\". I\'m using Windows 2000.

*A:* You need to download the RSX runtime environment, available from
<http://www.rigi.csc.uvic.ca/pub/rigi/windows95/>

The file RSX.EXE needs to be in your [PATH](PATH){.twikiLink}, or you
need to set the RSX environment variable to contain the path and name of
the RSX.EXE file, for example: set RSX=C:\\RSX\\BIN\\RSX.EXE.

For more information on RSX, consult the RSX homepage at
<http://www.mathematik.uni-bielefeld.de/~rainer/> \--JohannesMartin

------------------------------------------------------------------------

*Q:* When I try to load a Tcl file into [RigiEdit](RigiEdit){.twikiLink}
with `source C:\mytclfile`, I get an error message. However, I know that
the file is there!

*A:* So you are working under Windows, eh? In Tcl, you have two options:

-   use Unix notation: `C:/mytclfile`
-   escape the backslash: `C:\\mytclfile`

(Actually, `\` is Tcl\'s escape character I believe. So, in the wrong
path above Tcl expands the path to `C:mytclfile`.) \--
[HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

*Q:* When I execute an RCL script I get an error message \"couldn\'t
execute \'X\': permissing denied\" (X could be `gel-spring` ).

*A:* The the Tcl error message can be misleading. Most likely it means
that the program X cannot be found. Make sure that X\'s directory is in
the `PATH`.

------------------------------------------------------------------------

*Q:* Selecting incoming/outgoing nodes in Rigiedit does not seems to
work.Nothing ever happens\...

*A:* Select incoming/outgoing nodes selects only along arcs of the type
chosen in the \"arctype\" selection box on the left side of the rigi
workbench. This is usually set to \"level\", which doesn\'t match any
arcs in a regular Rigi view. If you set the selection to \"any\", you
should get the result you expect. \--
[JohannesMartin](JohannesMartin){.twikiLink}

------------------------------------------------------------------------

*Q:* When I try to use the Filter menu,the dialog boxes for filtering
nodes and arcs do not provide any checkboxes. What is the problem?

*A:* This is a Tcl/Tk bug that seems to show up in Windows XP and Vista
only. In fact, with this bug all checkboxes in all dialogs are gone!

As a workaround you can type in the corresponding Tcl commands in the
Rigi Command Language (RCL): `rcl_filter_nodetype` and then
`rcl_filter_apply`. Here is an example to for how this can be done for
filtering:

-   Start rigiedit
-   Go to Demo -\> List
-   Click OK
-   Click OK
-   Now you should see a window of a tree view. This window has the
    heading \"Overview - 2 Rigi\"
-   In the Rigi Workbench type in the following RCL Commands:

<!-- -->

    rcl_filter_nodetype Data 2
    rcl_filter_apply node

As a result two yellow nodes should disappear in the view.
Unfortunately, this workaround is rather inconvenient and slows down
interactive work. \-- [HolgerKienle](HolgerKienle){.twikiLink}

------------------------------------------------------------------------

[CategoryRigi](CategoryRigi){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
