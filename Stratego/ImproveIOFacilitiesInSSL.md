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
    Page](http://www.program-transformation.org/edit/Stratego/ImproveIOFacilitiesInSSL?t=1536825588)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ImproveIOFacilitiesInSSL)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ImproveIOFacilitiesInSSL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ImproveIOFacilitiesInSSL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ImproveIOFacilitiesInSSL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ImproveIOFacilitiesInSSL?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ImproveIOFacilitiesInSSL?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ImproveIOFacilitiesInSSL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ImproveIOFacilitiesInSSL?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ImproveIOFacilitiesInSSL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ImproveIOFacilitiesInSSL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ImproveIOFacilitiesInSSL?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/ImproveIOFacilitiesInSSL?template=oopsmore&param1=1.3&param2=1.3)
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
Improve IOFacilities In SSL {#improve-iofacilities-in-ssl .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](ImproveIOFacilitiesInSSL#Introduction)
-   [Problem](ImproveIOFacilitiesInSSL#Problem)
-   [Solution](ImproveIOFacilitiesInSSL#Solution)
    -   [Representing a
        stream](ImproveIOFacilitiesInSSL#Representing_a_stream)
    -   [File descriptor](ImproveIOFacilitiesInSSL#File_descriptor)
    -   [File paths](ImproveIOFacilitiesInSSL#File_paths)
    -   [Signature](ImproveIOFacilitiesInSSL#Signature)
-   [Existing code](ImproveIOFacilitiesInSSL#Existing_code)
    -   [Overview](ImproveIOFacilitiesInSSL#Overview)
:::

[]{#Introduction} Introduction
------------------------------

We need to improve the IO facilities in the SSL. Because the oldest
strategies are to abstract, many different implementations have been
created in the past. The structure is now very unclear. Especially
internally (in the native part of the SSL) it is quite a mess.
[EelcoVisser](EelcoVisser){.twikiLink} started on improving the IO
facilities a while ago by providing some basic POSIX functions in the
SSL.

[]{#Problem} Problem
--------------------

The most important problem is to find a suitable representation of an
open file where you can write data to. This used to be a complete mess
in Stratego:

1.  an internal table saves references from file names to ints. The ints
    are in fact FILE\* , but ints are not a suitable representation
    pointers.
2.  You can pass the same Int representation of a FILE\* around in
    Stratego.
3.  A file descriptor is also an Int \...
4.  All native primitives repeat the process of converting from terms to
    streams and back. Not all implementations handle all the cases.

Now this is not really a problem if you just write io-wrap applications,
but when you are doing more serious IO stuff (for example in
[StrategoNetworking](StrategoNetworking){.twikiLink} ) the current
strategies turn out to be incomplete and clumsy.

[]{#Solution} Solution
----------------------

We need to be able to use a stream *in* Stratego. In fact we need three
different kinds of \'files\':

-   file locator (char\* in C)
-   file descriptor (int in C)
-   stream (FILE\* in C)

Choosing a representation for the first two is easy: just invent some
nifty constructors that describe the required data and your finished.
The stream is a problem: the internal structure of a FILE shouldn\'t be
used and a pointer is difficult to represent in an ATerm.

### []{#Representing_a_stream} Representing a stream

First of all hiding the internal structure is a good idea: applications
shouldn\'t need to worry what data is needed to describe a stream.
Therefor the represention (whatever it will be) is packaged in `Stream`
constructor. The only child of the Stream constructor is defined as
implementation dependent and the internal structure of this term should
never be used in your application or the SSL. This makes the SSL more or
less back-end independent.

A FILE\* can be described by a
[ATermBlob[^?^](http://www.program-transformation.org/edit/Stratego/ATermBlob?topicparent=Stratego.ImproveIOFacilitiesInSSL)]{.twikiNewLink
style="background : #FFFFCE;"}. The size of the blob is the number of
bytes required to represent a pointer to a FILE. This is approach is
platform and processor independent.

### []{#File_descriptor} File descriptor

A file descriptor is an Int on all POSIX platforms, so we can just
define a file descriptor as a `FileDescr` constructor that takes an Int.

### []{#File_paths} File paths

A string as a file location might look nice at first sight, but in fact
we need more: stdin, stdout, stderr should be available on all levels.
In C they are file descriptors (0, 1, 2) and a stream (stdin, stdout,
stderr). In Stratego the `stdin`, `stderr` and `stdout` constructors are
used for streams as well as file locations. Because of this all
implementations that operate on streams have to handle these cases. I
want the constructors `stdin`, `stderr` and `stdout` to just be a file
location. The file descriptors and streams are available as a result of
(POSIX) strategies. You can make a stream from any file location with
`open-stream`.

File paths are represented with the `Path` constructor. A Path can be
absolute or relative. Maybe we can make more variants with a separation
of directories and filenames in the future.

### []{#Signature} Signature

      signature
        constructors
          Stream    : ImplDep -> Stream
          FileDescr : Int -> FileDescr

          Path      : String -> FileLoc
          stdin     : FileLoc
          stdout    : FileLoc
          stderr    : FileLoc

Maybe the stdin, stdout and stderr constructs can even be replaced by
overlays for a Stream. This will probably not break existing code,
except for native code in the SSL that cannot Stream constructs.

      overlays
        stdin  = Stream(<prim("SSL_stdin_stream")> ())
        stdout = Stream(<prim("SSL_stdout_stream")> ())
        stderr = Stream(<prim("SSL_stderr_stream")> ())

[]{#Existing_code} Existing code
--------------------------------

Now we have a stream representation in Stratego, things get much more
easy and powerful for both library users and library implementors. A
complete switch to this style will lead to an enormous reduction of the
amount of native code in the SSL part of the SRTS. I\'ve rewritten some
code and most native implementation are reduced by more than 50%.

I suggest to rewrite all existing code that operate on streams and file
descriptors. These strategies are relatively new, are just used by Eelco
and me and are not used in legacy code. Most of the existing code will
not break because it doesn\'t matter a lot to client code how streams
and file descriptors are represented.

For strategies that operate on file names, this is of course not
acceptable. `open-file` is for example widely used. Some of these
strategies could be implemented on top of the new IO facilities because
the new facilities are more atomic. There is one big problem: the evil
file table. The new IO solution with fds, streams and file locations
requires you to actually use the result of open-file, which will be a
Stream. Currently open-file just returns the filename. This encourages a
style where you just open the file and just work with the filename later
in the program. If we rewrite open-file, this will break existing (and
very old) code.

So we should leave the real legacy strategies alone for now. Most
strategy names are not in the way because the new facilities prefer the
name \"stream\" over \"file\" and POSIX procedure names for operations
on them. In the future we could deprecate the old IO strategies or
define them in terms of the new facilities. The open file table should
be removed in the future.

### []{#Overview} Overview

-   All strategies should specify whether they operate on:
    -   file paths \-- text based name
    -   file descriptors \-- int
    -   streams \-- platform dependent structure
-   If strategies accept different kinds of file representations,
    overloading should happen in Stratego, not in the native code.
-   Represent stream ( `FILE*` ) by
    [ATermBlob[^?^](http://www.program-transformation.org/edit/Stratego/ATermBlob?topicparent=Stratego.ImproveIOFacilitiesInSSL)]{.twikiNewLink
    style="background : #FFFFCE;"} in constructor (Stream) instead of
    \'int\' pointer.
-   Remove \'open file\' table in io.c
-   Represent file descriptor in constructor
-   Make POSIX process and file procedures available in the SSL
-   Merge with IO facilities of [XTC](XTC){.twikiLink}

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 24 Mar
2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
