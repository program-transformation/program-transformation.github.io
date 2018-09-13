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
    Page](http://www.program-transformation.org/edit/Stratego/XtArchive?t=1536825543)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/XtArchive)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/XtArchive)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/XtArchive?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/XtArchive?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/XtArchive?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/XtArchive?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/XtArchive?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/XtArchive)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/XtArchive?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/XtArchive?template=oopsmore&param1=1.2&param2=1.2)
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
Xt Archive {#xt-archive .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Some ideas for making advanced Stratego features more accessible to new
users.

[]{#Goals} Goals
----------------

-   Easy to define a syntax for language X and implement a source-to-?
    or source-to-source transformation for it.

<!-- -->

-   Easy to define a transformation for language X, which is already
    supported by some package (e.g. java-front).

<!-- -->

-   Easy to reuse existing syntax definitions. Languages should be
    \'components\' that more or less hide their internal implementation.

[]{#XT_Archives_Tool_and_File_Integr} XT Archives: Tool and File Integration
----------------------------------------------------------------------------

One of the problems of XT is that there are many file types for a single
subject language. These file types are used by several tools. The users
needs to know how to generate all these files and he needs to pass these
files explicitly to all the tools.

xtar (xt archive) is a solution to this problem. xtar collects the
standard set of files for a specific language into a single zip archive
(compare to a jar file). This archive can then be passed to all the XT
tools and they just take out the files that they need. The user doesn\'t
need to know what specific files a tool need.

The only input of xtar tool is an [SDF](SDF){.twikiLink} module. It
takes a -i argument for this module and probably should accept the
include flags of pack-sdf. xtar will integrate the following tools:

-   pack-sdf
-   sdf2table
-   sdf2rtg
-   rtg2sig
-   ppgen

The resulting xtar will contain all the files related to a language: a
A.def, A.tbl, A.rtg (A.rtg-nf), A.str (A.rtree) and A.pp (A.pp.af).
Hence, the xtar contains all the files required to implement a
transformation for language A. Furthermore, the archive might contain
meta information (compare the a jar manifest).

Components of this archive, in particular the .pp, must be overrideable.

------------------------------------------------------------------------

Below are some more adventurous and unclear ideas. These are not
directly related to the idea of XT Archives.

------------------------------------------------------------------------

[]{#Flexible_Composition_of_XTC_Repo} Flexible Composition of [XTC](XTC){.twikiLink} Repositories
-------------------------------------------------------------------------------------------------

Problem: users more or less need to be in an Autoconf/Automake
environment if they need to do composition.

The [XTC](XTC){.twikiLink} repository mechanism should be more flexible.
Most important: a tool should be able to locate resources from multiple
repositories. Also, repositories should be more dynamic: currently
repositories are only constructed at install-time.

The configuration of the [XTC](XTC){.twikiLink} repositories to use
should be more flexible. It should be possible to extend the resources
visible to [StrategoXT](StrategoXT){.twikiLink} components, without
difficult repository construction.

Ideas:

-   Automatically load repositories in a /home/fred/.xtc directory.
    Packages could provide an \'activate\' tool that adds their
    repository to this directory.

<!-- -->

-   Use a \":\" separated environment variable \'XTC\_REPOS\'. This
    variable can contain multiple [XTC](XTC){.twikiLink} repositories,
    which are all loaded.

<!-- -->

-   On-request extension of the [XTC](XTC){.twikiLink} bindings. The zip
    archive of language specific files should for example be accepted by
    the Stratego compiler. These files are registered and the entries
    refer to the files in the zip file.

(Karl) I specifically suggest some configuration guidelines for the
[XTC](XTC){.twikiLink} tools:

-   Every [XTC](XTC){.twikiLink} tool will perform a fixed search for
    dynamic configuration settings, starting with searching for
    \${prefix}/etc/xtc/xtc.conf, then \${HOME}/.xtc/config (or
    .xtc.conf), then any environment variables, such as XTC\_REPOS.
    Settings will be overriden upon rediscovery.

<!-- -->

-   Easy programmatic inspection of the [XTC](XTC){.twikiLink}
    repository, and xtars, allowing for searching, e.g.: xtc-query
    Java.sdf will find all available Java.sdfs, and explain the
    precedence order. (User may have his own experimental stuff in
    \~/.xtc/myjavastuff.xtar that inadvertently takes precedence over
    /usr/share/xtc/myjavastuff.xtar).

Also:

-   Documentation; inasmuch as this exists, it should either be in the
    xtar bundle itself, or referenced in a way that allows for easy
    queries and subsequent display in a web browser.

In this way, the \'language archive\' can be used completely
transparantly by the Stratego compiler and other tools.

[]{#Include_Resources_in_Executable} Include Resources in Executable
--------------------------------------------------------------------

Transformation tools should be more or less self-contained, at least
they should contain their data files to avoid all the problems in
locating this data.

At least, all external files can be packed into one xtar, which is
bundled along with the binary. If all auxiliary tools know how to deal
with xtars, we have reduced the deployment from binary + heaploads of
extra stuff to binary + data, which is already a big improvement.

-   Parse-tables could be included in the binary. They can be written to
    a temporary file, or libsglr can be used.

<!-- -->

-   Transformation tools created in this way should not have a built-in
    default repository: they should be portable the .xtc mechanism can
    be used as a default a repository.

<!-- -->

-   In-program resources (such as the parse table) should be registered
    in [XTC](XTC){.twikiLink} and can be used as ordinary
    [XTC](XTC){.twikiLink} resources.

<!-- -->

-   [XTC](XTC){.twikiLink} compositions can be written in a non-automake
    enviroment.

[]{#Inline_Meta_Files} Inline Meta Files
----------------------------------------

This is all just an extension of the existing [XTC](XTC){.twikiLink}
mechanism. Another thing we would like to change is the .meta file.
Defining meta information in the program itself is more comprehensible
for new users, and it is easier to move files around. The solution is to
add a header to a Stratego module. This header will be read separately
and the real body will be parsed with the specified syntax. Preferably,
this header should be in a concrete syntax.

Example:

        meta
          syntax = StrategoJava

        module foo
        imports
          Java
          java-xtc-tools

        strategies
          main =
            xtc-io-wrap(
              xtc-parse-java
            ; do-my-stuff
            ; xtc-pp-java
            )

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
