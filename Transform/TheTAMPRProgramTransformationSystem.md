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
    Page](http://www.program-transformation.org/edit/Transform/TheTAMPRProgramTransformationSystem?t=1536826578)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/TheTAMPRProgramTransformationSystem)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/TheTAMPRProgramTransformationSystem)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/TheTAMPRProgramTransformationSystem?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/TheTAMPRProgramTransformationSystem?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/TheTAMPRProgramTransformationSystem?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/TheTAMPRProgramTransformationSystem)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/TheTAMPRProgramTransformationSystem?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/TheTAMPRProgramTransformationSystem?template=oopsmore&param1=1.1&param2=1.1)
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
The TAMPRProgram Transformation System {#the-tamprprogram-transformation-system .twikiTopicTitle}
======================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**The [TAMPR](TAMPR){.twikiLink} Program Transformation System:
Simplifying the Development of Numerical Software**

by J. M. Boyle, T. J. Harmer and V. L. Winter

In E. Arge, A.M. Bruaset and H.P. Langtangen (eds.) *Modern Software
Tools in Scientific Computing* pp 353-372, Birkhäuser, 1997

------------------------------------------------------------------------

**Summary**

[TAMPR](TAMPR){.twikiLink} stands for *Transformation Assisted Multiple
Program Realisation System*. The [TAMPR](TAMPR){.twikiLink} system,
which has been in use since the seventies, is designed for the
derivation of efficient implementations from a specification through
transformations, in particular in the domain of numerical programming.

A [TAMPR](TAMPR){.twikiLink} specification consists of a series of
rewrite rules. The [TAMPR](TAMPR){.twikiLink} rewrite engine applies
rewrite rules exhaustively to reach a canonical form. The problem of
non-termination caused by rules that are each others inverses is solved
in [TAMPR](TAMPR){.twikiLink} by organizing a large transformation into
a sequence of consecutive canonicalizations under different sets of
rewrite rules. Typically such a sequence starts with several preparatory
steps that bring the program in the right form, followed by the pivotal
step which achieves the actual transformation, followed by some
post-processing.

In the paper this is illustrated with the transformation from a
polynomial in `y`:

      (x^2 + 2x + 1)y^2 + (x^2 - 9)y - (20x^2 + 18x - 18)

to the equivalent polynomial in `x`

      (y^2 + y - 20)x^2 + (2y^2 - 18)x + (y^2 - 9y + 18)

This is achieved by means of the following pipeline of
canonicalizations:

      sum-of-monomonials;   
      x-commuted-to-right;
      like-powers-collected;
      x-factored-out

(Note that the paper uses a different notation for this.) The
`sum-of-monomonials` transforms the polynomial into

      x^2y^2 + 2xy^2 + y^2 + x^2y -9y -20x^2 - 18x + 18

By commuting the multiplications, the `x-commuted-to-right` canonical
form is achieved:

      y^2x^2 + 2y^2x + y^2 + yx^2 -9y -20x^2 - 18x + 18

The `like-powers-collected` canonical form commutes the additions to
bring monomonials with the same power of \$x\$ together:

      y^2x^2 + yx^2 - 20x^2 + 2y^2x - 18x + y^2 -9y + 18

Finally, by factoring out the powers of `x`, the desired form is
reached.

------------------------------------------------------------------------

[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 07 May 2001\

------------------------------------------------------------------------

[CategoryReview](CategoryReview){.twikiLink},
[CategoryTransformation](CategoryTransformation){.twikiLink} \|
Contributions by [EelcoVisser](../Main/EelcoVisser){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
