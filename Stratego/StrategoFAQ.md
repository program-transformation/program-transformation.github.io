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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoFAQ?t=1536825674)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoFAQ)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoFAQ)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoFAQ?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoFAQ?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/StrategoFAQ?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/StrategoFAQ?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/StrategoFAQ?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/StrategoFAQ?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoFAQ?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoFAQ?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoFAQ)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoFAQ?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoFAQ?template=oopsmore&param1=1.4&param2=1.4)
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
Stratego FAQ {#stratego-faq .twikiTopicTitle}
============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Q: Can I get Stratego/XT running on Windows?

A: We do not currently provide a pre-built binary of 0.17 on Windows at
the moment. You can compile Stratego/XT on Windows using Cygwin,
provided you install the necessary libraries in advance. In particular,
remember to install `util-linux` in order to get `getopt` (required for
`sdf2-bundle`). For the previous stable release, 0.16, we have binary
releases.

Q: Can I get Stratego/XT running on OSX?

A: This is Unix! I know this! (Yes, by either installing it through Nix
or compiling from sources.)

Q: What\'s the difference between `spinetd` and `oncetd`?

A: The spine topdown traversal applies a strategy parameter at every
aterm on a spine from the root to a leaf. The once topdown strategy
applies its strategy parameter at only a single location.

    signature

     constructors
        A : Term -> Term
        A : Term * Term -> Term
        A : Term * Term * Term -> Term
        A : Term * Term * Term * Term -> Term
        B : Term -> Term
        B : Term * Term -> Term

    strategies

        main = !A(0,1,B(2,3),4) ; spinetd((not(int) ; debug(!"> ") <+ fail))

Running `main` gives you this:

    > A(0,1,B(2,3),4)
    > B(2,3)
    A(0,1,B(2,3),4) 

Q: Why does `sdf2table`
([SdfChecker[^?^](http://www.program-transformation.org/edit/Stratego/SdfChecker?topicparent=Stratego.StrategoFAQ)]{.twikiNewLink
style="background : #FFFFCE;"}) always complain that the Main module is
not defined?

A: When you run `sdf2table` in the present (0.17) Stratego/XT, e.g.

    $ sdf2table -i Expression.def -o Expression.tbl -m Expression

you will always get the error message that the Main module is undefined:

    SdfChecker:error: Main module not defined 

This is a known bug. Ignore it. It\'s been fixed upstream already, and
will trickle into newer Stratego/XT releases.

Technical details: The `sdf2table` script first does a check of the
grammar using `sdfchecker` before it applies the generator,
`parsetablegen`. `sdfchecker` is the one emitting the error message.
Since `parsetablegen` is the tool responsible for actually generating
the .tbl file, it doesn\'t matter that `sdfchecker` is being
unreasonably cranky.

If this annoys you unbearably, name your main module `Main.sdf`.

Q: Where is this \"alt\" stuff coming from?

A: Don\'t use alternatives in your [SDF](SDF){.twikiLink}, i.e. don\'t
use productions of the form

       "foo" (A | B) "bar" -> C

Instead, write

       "foo" AorB "bar" -> C
       A                -> AorB
       B                -> AorB

This is really equivalent, since the [SDF](SDF){.twikiLink} normalizer
transforms the first production to

       "foo" (A | B) "bar" -> C
       A                   -> (A | B)
       B                   -> (A | B)

However, `asfix-implode` interprets the latter to include `alt`
constructors. This is needed to cover cases such as

       "foo" ("a" A | "b" B) "bar" -> C

such that the alternatives can be reconstructed (e.g. when
pretty-printing). Since the alternatives need to be named to
distinghuish them, this is better written as

      "foo" AorB "bar" -> C {cons("Foo")}
      "a" A            -> AorB {cons("A")}
      "b" B            -> AorB {cons("B")}

so that you can actually control the names used.

Q: Where can I find documentation for [SDF](SDF){.twikiLink}?

A: [SDF](SDF){.twikiLink} lives at
[syntax-definition.org](http://www.syntax-definition.org)

\-- [KarlTrygveKalleberg](../Main/KarlTrygveKalleberg){.twikiLink} - 30
Oct 2008\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
