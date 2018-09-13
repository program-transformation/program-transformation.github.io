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
    Page](http://www.program-transformation.org/edit/Stratego/QuineInStratego?t=1536825661)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/QuineInStratego)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/QuineInStratego)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/QuineInStratego?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/QuineInStratego?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/QuineInStratego?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/QuineInStratego)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/QuineInStratego?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/QuineInStratego?template=oopsmore&param1=1.1&param2=1.1)
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
Quine In Stratego {#quine-in-stratego .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

After GPCE/OOPSLA in Vancouver Tijs van der Storm challenged me to write
a Stratego program that prints its own source. So I set to work, with
the following result. I\'ll make it educational and reconstruct the
design process.

### []{#The_basic_idea} The basic idea

The core of a self printing program is that it should contain its own
source and duplicate that. The following program implements this idea,
but with \'prefix\' and \'suffix\' instead of the

    ----------------------------------
    module quine 
    imports lib
    strategies
      main =
        !["prefix", "suffix"]
        ; \ [x, y] -> [x, x, y, y] \ 
        ; concat-strings
        ; <print>(stdout, [<id>])
        ; <exit> 0
    -----------------------------------

Compiling and running this program produces:

    prefixprefixsuffixsuffix

### []{#Quoting_the_source} Quoting the source

Next we replace \'prefix\' and \'suffix\' by the prefix and suffix of
the program with respect to the list. Note that we don\'t bother with
the layout of the quoted fragment. Note that the backslashes of the
anonymous rewrite rule need to be escaped in the string.

    ------------------------------------------------------------------------------------------
    module quine 
    imports lib
    strategies
      main =
        !["module quine imports lib strategies main = ![", 
          "]; \\ [x, y] -> [x, x, y, y] \\; concat-strings; <print>(stdout, [<id>]); <exit> 0"]
        ; \ [x, y] -> [x, x, y, y] \ 
        ; concat-strings
        ; <print>(stdout, [<id>])
        ; <exit> 0
    ------------------------------------------------------------------------------------------

The output of this program is

    ------------------------------------------------------------------
    module quine imports lib strategies main = ![module quine 
    imports lib strategies main = ![]; \ [x, y] -> [x, x, y, y] \; 
    concat-strings; <print>(stdout, [<id>]); <exit> 0]; \ [x, y] -> 
    [x, x, y, y] \; concat-strings; <print>(stdout, [<id>]); <exit> 0
    ------------------------------------------------------------------

which is starting to look good, but not quite there, since it doesn\'t
compile.

### []{#Getting_the_quotes_right} Getting the quotes right

What we have to do now is introduce quotes in the printed program, such
that the pieces of code in the list are actually parsed as strings.

    ------------------------------------------------------------------------------------------
    module quine 
    imports lib
    strategies
      main =
        !["module quine imports lib strategies main = ![\"", 
          "\"]; \\ [x, y] -> [x, x, y, y] \\; concat-strings; <print>(stdout, [<id>]); <exit> 0"]
        ; \ [x, y] -> [x, x, "\",\"", y, y] \ 
        ; concat-strings
        ; <print>(stdout, [<id>])
        ; <exit> 0
    ------------------------------------------------------------------------------------------

The output of this program is

    ------------------------------------------------------------------
    module quine imports lib strategies main = !["module quine 
    imports lib strategies main = !["",""]; \ [x, y] -> [x, x, y, y] \; 
    concat-strings; <print>(stdout, [<id>]); <exit> 0"]; \ [x, y] -> 
    [x, x, y, y] \; concat-strings; <print>(stdout, [<id>]); <exit> 0
    ------------------------------------------------------------------

which still does not compile because of the doublequotes embedded in the
string.

### []{#Getting_the_quotes_more_right} Getting the quotes more right

We need to escape the embedded strings. This can be achieved easily by
using the `escape` strategy from the library, which escapes doublequotes
and backslashes.

    ------------------------------------------------------------------------------------------
    module quine 
    imports lib
    strategies
      main =
        !["module quine imports lib strategies main = ![\"", 
          "\"]; \\ [x, y] -> [x, <escape>x, \"\\\",\\\"\", <escape>y, y] \\; concat-strings; <print>(stdout, [<id>]); <exit> 0"]
        ; \ [x, y] -> [x, <escape>x, "\",\"", <escape>y, y] \ 
        ; concat-strings
        ; <print>(stdout, [<id>])
        ; <exit> 0
    ------------------------------------------------------------------------------------------

This produces (without the newlines)

    -----------------------------------------------------------------------------
    module quine imports lib strategies main = !["module quine imports 
    lib strategies main = ![\"","\"]; \\ [x, y] -> [x, <escape>x,
     \"\\\",\\\"\", <escape>y, y] \\; concat-strings; <print>(stdout
    , [<id>]); <exit> 0"]; \ [x, y] -> [x, <escape>x, "\",\"", <escape>y, y] \; 
    concat-strings; <print>(stdout, [<id>]); <exit> 0
    -----------------------------------------------------------------------------

### []{#Bootstrapping} Bootstrapping

Now the last program is not exactly the same as its predecessor, but if
we compile and run it, it produces its own source literally.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
