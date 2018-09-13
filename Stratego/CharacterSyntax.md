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
    Page](http://www.program-transformation.org/edit/Stratego/CharacterSyntax?t=1536825568)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/CharacterSyntax)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/CharacterSyntax)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/CharacterSyntax?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/CharacterSyntax?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/CharacterSyntax?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/CharacterSyntax)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/CharacterSyntax?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/CharacterSyntax?template=oopsmore&param1=1.1&param2=1.1)
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
Character Syntax {#character-syntax .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A few months ago I proposed to introduce character literals in Stratego
as syntactic sugar for the integer ASCII value of the character. I would
like to raise this issue again ;-) .

My proposal was to introduce the widely used \'c\' syntax to represent a
character in Stratego. The stratego compiler can desugar this to the
integer ASCII representation of the character, what we use to work with
characters right now. The implementation is trivial, it requires no
changes to the backend, it requires no special ATerm types.

Advantages:

-   You don\'t need an ASCII table when your programming string
    manipulations in Stratego.

<!-- -->

-   String processing code like in string.r and char.r in the ssl will
    become much more clearer.

<!-- -->

-   It is tempting to explode string literals (even of length 1) at
    runtime so you don\'t have to look up the character codes. Character
    literals will improve performance in this case.

Disadvantages:

-   The disadvantage Eelco Visser mentioned when I proposed it before:
    what if the result of a Stratego transformation will contain
    characters. The user will see integer values instead of the
    character literal in this case. I think that this is not a huge
    problem because: (1) characters are not likely to occur in the
    result of a program: they are often used in String manipulation,
    where the string will be rebuild (imploded) later. (2) In another
    Stratego applications the integer value can still be matched against
    a pattern with a character literal because a character literal is
    simply an int. (3) concrete syntax already makes the resulting
    aterms more difficult to compare with the Stratego code. I think the
    added distance between Stratego terms and ATerms is negligible.
-   The single quote (apostrophe) is allowed in an identifier. This is a
    problem if the charachter in the literal is also an allowed
    charachter in an identifier. This introduces an ambiguity. However,
    an identifier like \'c\' is very unlikely to occur and could be
    rejected by the [SDF](SDF){.twikiLink} grammar.

I\'m currently writing strategies to rewrite XML entities and character
references. I\'m using overlays right now. This is already an
improvement, but quite verbose.

    ------------------------
    rules

    unescape-amp :
       [c_amp(), c_a(), c_m(), c_p(), c_semicolon() | cs] -> [c_amp() | cs]
    unescape-lt :
       [c_amp(), c_l(), c_t(), c_semicolon() | cs] -> [c_lt() | cs]
    unescape-gt :
       [c_amp(), c_g(), c_t(), c_semicolon() | cs] -> [c_gt() | cs]

    overlays

       c_space() = 32
       c_quote() = 34
       c_amp()   = 38
       c_apos()  = 39
       c_0()     = 48
       c_9()     = 57
       c_semicolon() = 59
       c_numbersign() = 35
    ------------------------

This would be possible with characters in Stratego:

    -----------------------------------
    unescape-amp : ['&', 'a', 'm', 'p', ';' | cs] -> ['&' | cs]
    unescape-lt  : ['&', 'l', 't', ';' | cs] -> ['<' | cs]
    unescape-gt  : ['&', 'g', 't', ';' | cs] -> ['>' | cs]
    -----------------------------------

Of course (un)escaping is an example where the usefulness of character
literals is huge. In general you won\'t use character literals a lot in
Stratego. Because of the simplicity of the implementation I think that
it is still worth the effort.

I would like to hear your opinion :-) .

\-- Martin Bravenboer - 07 Dec 2002

Ok. I have added the following to the [SDF](SDF){.twikiLink} definition
of Stratego:

    ----------------------------------------------------------------------
      lexical syntax
        "\'" CharChar "\'"      -> Char
        ~[\']         -> CharChar
        [\\] [\'ntr\ ]      -> CharChar
        Char          -> Id {reject}
     
      context-free syntax
        Char              -> Term {cons("Char")}
    ----------------------------------------------------------------------

and the following desugaring rules to stratego-desugar:

    ----------------------------------------------------------------------
      Desugar :
        Char(c) -> Int(i)
        where <DesugarChar <+ explode-string; DesugarCharGeneric> c => i

      DesugarCharGeneric :
        [39, i, 39] -> i
      DesugarChar :
        "'\\''" -> 39
      DesugarChar :
        "'\\n'" -> 10
      DesugarChar :
        "'\\t'" -> 9
      DesugarChar : // carriage return
        "'\\r'" -> 13
      DesugarChar : // space
        "'\\ '" -> 32
    ----------------------------------------------------------------------

Note that the desugaring is done at the syntactic level as part of
parsing. This means that characters are pretty-printed as integers. This
can be improved later by shifting the desugaring until later in the
process. This requires deeper embedding of this notion in Stratego,
though.

Are any other escapes needed? Note that this will break existing
specifications with identifiers of the form \'c\' (which I have never
seen).

These changes are available in
[StrategoRelease09](StrategoRelease09){.twikiLink} (beta7).

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 21 Dec 2002\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
