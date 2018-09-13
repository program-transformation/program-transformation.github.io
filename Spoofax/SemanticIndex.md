::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[Spoofax](http://www.program-transformation.org/view/Spoofax/WebHome)**

\

**[Home](WebHome){.twikiLink}**

**[Tour and screenshots](Tour){.twikiLink}**

**[Documentation](Documentation){.twikiLink}**

**[Download](Download){.twikiLink}**

**[Research](Research){.twikiLink}**

**[Development](Development){.twikiLink}**

**[Support](Support){.twikiLink}**

\

\
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Spoofax/SemanticIndex?t=1536826263)
-   [Rename
    Page](http://www.program-transformation.org/rename/Spoofax/SemanticIndex)
-   [Attach
    File](http://www.program-transformation.org/attach/Spoofax/SemanticIndex)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Spoofax/SemanticIndex?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Spoofax/SemanticIndex?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Spoofax/SemanticIndex?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Spoofax/SemanticIndex?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Spoofax/SemanticIndex?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Spoofax/SemanticIndex?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Spoofax/SemanticIndex?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Spoofax/SemanticIndex)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Spoofax/SemanticIndex?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Spoofax/SemanticIndex?template=oopsmore&param1=1.3&param2=1.3)
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
Semantic Index {#semantic-index .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Spoofax
:::

[]{#Introduction} Introduction
------------------------------

The semantic index is a set of stratego libraries, java primitives and
editor extensions that provide a language-parametric framework for doing
name binding, scoping, incremental analysis and incremental compilation.

[]{#Quick_start} Quick start
----------------------------

To be able to use the index a nightly version of Spoofax is required
which can be retrieved from the following update site:

       http://spoofax.org/update/nightly

The simplest place to get an example on what the index can do and how a
project using the index looks like is generating a new Spoofax project.
Go to File-\>New-\>Project, choose \"Spoofax editor project\" and fill
in Entity as the language name. This will generate and build a Spoofax
example project for you that uses the index. To test it out open up
test/example.ent and try some things like resolving a reference, code
completion and introducing errors by changing types to types that do not
exist. These features are all provided by the index using naming
annotations in the SDF file and Stratego code to fill in some gaps in
the generic algorithm. The tutorial will go into more detail on how to
define these things yourself.

More complex examples using the index are also available. We\'ve
prototyped a mini C\# subset, a C subset without macros and the entity
language with functions and aspects using the index. To get these
examples download [this
archive[^?^](http://www.program-transformation.org/edit/Spoofax/TODOFillInLink?topicparent=Spoofax.SemanticIndex)]{.twikiNewLink
style="background : #FFFFCE;"}, extract it somewhere, import the
projects into an Eclipse workspace and build all projects (ctr+b).

[]{#Tutorial} Tutorial
----------------------

In this tutorial we will explain how the example entity language uses
the index and how to extend it with functions and simple expressions.

### []{#Analysis} Analysis

#### []{#Name_annotations} Name annotations

If you look at the entity language SDF definition below you will see
that it has naming annotations on certain terminals (Type@=, Type@, etc)
and scope annotations on productions (scope(Type)).

        "module" Module@=ID Definition*       -> Start {"Module", scope(Type)}
        "entity" Type@=ID "{" Property* "}"   -> Definition {"Entity", scope(Property)}
        Property@=ID ":" Type                 -> Property {"Property"}
        Type@ID                               -> Type {"Type"}

#### []{#Adjust_rules} Adjust rules

#### []{#Error_checking} Error checking

#### []{#Incremental_analysis} Incremental analysis

### []{#Compilation} Compilation

[]{#Inner_workings} Inner workings
----------------------------------

### []{#Extension_points} Extension points

[]{#FAQ} [FAQ](FAQ){.twikiLink}
-------------------------------

### []{#Where_can_I_find_API_documentati} Where can I find API documentation?

### []{#How_to_fix_build_error_x}[]{#How_to_fix_build_error_x_} How to fix build error x?

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
