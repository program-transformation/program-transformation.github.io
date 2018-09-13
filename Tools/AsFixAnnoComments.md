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
    Page](http://www.program-transformation.org/edit/Tools/AsFixAnnoComments?t=1536825773)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AsFixAnnoComments)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AsFixAnnoComments)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AsFixAnnoComments?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AsFixAnnoComments?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/AsFixAnnoComments?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/AsFixAnnoComments?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/AsFixAnnoComments?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AsFixAnnoComments)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AsFixAnnoComments?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/AsFixAnnoComments?template=oopsmore&param1=1.2&param2=1.2)
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
As Fix Anno Comments {#as-fix-anno-comments .twikiTopicTitle}
====================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Description} Description
----------------------------

An asfix to asfix tool that reserves comments that were of the input
source code by putting them in annotations of the AST.

It is difficult to decide what a comment actually comments on. The tool
uses the heuristic that a comment is usually about the next construct.
Therefore, it adds the comment to the first term with a constructor in
the the subtree of the next symbol in the production rule. If this next
symbol is a literal, then the comment will not be preserved.

[]{#Example} Example
--------------------

This simple tool works remarkably well. Let me illustrate this with an
example input that I used during the development of this tool.

      /**
       * Voodoo
       */
      class Voodoo
      {
        /**
         * Bla bla
         */
        public void foo(/*let me explain this */ int x)
        {
          // just return
          return /* foo */ x;
        }
      }

An example fragment of the AST:

      Param([], Int, Id("x")){(Comment, "/*let me explain this */")}

The [JavaFront](../Stratego/JavaFront){.twikiLink} pretty-printer has
been extended to support these Comment annotations. The following pipe:

      sglr -2 -s CompilationUnit -p ~/wc/java-front/syn/v1.5/Java-15.tbl 
         -i ~/Foo.java
      | ./asfix-anno-comments
      | implode-asfix
      | pp-java

produces the following output:

      /**
       * Voodoo
       */
      class Voodoo
      {
        /**
         * Bla bla
         */
        public void foo(/*let me explain this */ int x)
        {
          // just return
          return /* foo */ x;
        }
      }

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
