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
    Page](http://www.program-transformation.org/edit/Tools/ATermToXml?t=1536825865)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/ATermToXml)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/ATermToXml)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/ATermToXml?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/ATermToXml?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tools/ATermToXml?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/ATermToXml?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/ATermToXml?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/ATermToXml?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/ATermToXml?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/ATermToXml?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/ATermToXml)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/ATermToXml?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tools/ATermToXml?template=oopsmore&param1=1.4&param2=1.4)
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
ATerm To Xml {#aterm-to-xml .twikiTopicTitle}
============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Summary} Summary
--------------------

Converts an ATerm to a comparable XML document.

[]{#Description} Description
----------------------------

The tools [aterm2xml](ATermToXml){.twikiLink} and
[xml2aterm](XmlToATerm){.twikiLink} support the conversion from ATerm to
XML and vice versa. Since applications have different needs, there are
three conversion modes available: implicit, explicit, and very explicit.

-   The explicit mode is the default mode and supports a roundtrip for
    almost all ATerms (that is, an ATerm can be converted to XML and
    back without changing its structure).

<!-- -->

-   The implicit mode does not support such a roundtrip, but the XML is
    usually more attractive. Use this mode if you only want to export
    some ATerm to an XML application. The name \'implicit\' is related
    to the more implicit structure in the resulting XML.

<!-- -->

-   The very explicit mode supports a roundtrip for all ATerms. This
    mode is the way to go if you need the guarantee that a roundtrip
    preserves the structure of all your ATerms.

The structure of the XML documents in the very explicit mode is generic:
there are no language specific elements in these XML documents. The
structure is described a [RELAX NG
schema](https://svn.cs.uu.nl:12443/repos/StrategoXT/trunk/StrategoXT/xml-front/doc/very-explicit.rnc).

[]{#Future_Work} Future Work
----------------------------

In a future release we will add support for a round trip in the implicit
mode, based on schema/rtg information. This has already been
implemented, but needs to be updated and refactored.

[]{#Examples} Examples
----------------------

The following invocations illustrate how to invoke the tools:

::: {style="margin-left: 2em"}
    $ aterm2xml -i foo.trm                  # convert to explicit xml
    $ aterm2xml -i foo.trm | xml2aterm      # convert to explicit xml and back
    $ aterm2xml -i foo.trm --implicit       # convert to implicit xml
    $ aterm2xml -i foo.trm --very-explicit  # convert to very explicit xml
:::

The following tables explain the differences between the three explicity
modes that are support by aterm2xml.

### []{#Explicit_XML} Explicit XML

ATerm
:::
:::
:::
:::

Explicit XML

Back to ATerm

    foo

    <foo xmlns:at="http://aterm.org"/>

    foo

    foo(1)

    <foo xmlns:at="http://aterm.org">
      <at:int>1</at:int>
    </foo>

    foo(1)

    1

    <at:int xmlns:at="http://aterm.org">1</at:int>

    1

    "abc"

    <at:string xmlns:at="http://aterm.org">abc</at:string>

    "abc"

    ()

    <at:tuple xmlns:at="http://aterm.org"/>

    ()

    (1, 2)

    <at:tuple xmlns:at="http://aterm.org">
      <at:int>1</at:int>
      <at:int>2</at:int>
    </at:tuple>

    (1,2)

    []

    <at:list xmlns:at="http://aterm.org"/>

    []

    [1, 2]

    <at:list xmlns:at="http://aterm.org">
      <at:int>1</at:int>
      <at:int>2</at:int>
    </at:list>

    [1,2]

    fred([foo, bar])

    <fred xmlns:at="http://aterm.org">
      <at:list>
        <foo/>
        <bar/>
      </at:list>
    </fred>

    fred([foo,bar])

    fred(None, [foo, bar])

    <fred xmlns:at="http://aterm.org">
      <None/>
      <at:list>
        <foo/>
        <bar/>
      </at:list>
    </fred>

    fred(None,[foo,bar])

    fred(Some(barney), [foo, bar])

    <fred xmlns:at="http://aterm.org">
      <Some>
        <barney/>
      </Some>
      <at:list>
        <foo/>
        <bar/>
      </at:list>
    </fred>

    fred(Some(barney),[foo,bar])

    fred("foo", "bar")

    <fred xmlns:at="http://aterm.org">
      <at:string>foo</at:string>
      <at:string>bar</at:string>
    </fred>

    fred("foo","bar")

    foo{fred}

    <foo xmlns:at="http://aterm.org">
      <at:anno>
        <fred/>
      </at:anno>
    </foo>

    foo{fred}

### []{#Very_Explicit_XML} Very Explicit XML

ATerm

Very Explicit XML

Back to ATerm

    foo

    <at:appl xmlns:at="http://aterm.org" at:fun="foo"/>

    foo

    foo(1)

    <at:appl xmlns:at="http://aterm.org" at:fun="foo">
      <at:int>
        <at:value>1</at:value>
      </at:int>
    </at:appl>

    foo(1)

    1

    <at:int xmlns:at="http://aterm.org">
      <at:value>1</at:value>
    </at:int>

    1

    "abc"

    <at:string xmlns:at="http://aterm.org">
      <at:value>abc</at:value>
    </at:string>

    "abc"

    ()

    <at:tuple xmlns:at="http://aterm.org"/>

    ()

    (1, 2)

    <at:tuple xmlns:at="http://aterm.org">
      <at:int>
        <at:value>1</at:value>
      </at:int>
      <at:int>
        <at:value>2</at:value>
      </at:int>
    </at:tuple>

    (1,2)

    []

    <at:list xmlns:at="http://aterm.org"/>

    []

    [1, 2]

    <at:list xmlns:at="http://aterm.org">
      <at:int>
        <at:value>1</at:value>
      </at:int>
      <at:int>
        <at:value>2</at:value>
      </at:int>
    </at:list>

    [1,2]

    fred([foo, bar])

    <at:appl xmlns:at="http://aterm.org" at:fun="fred">
      <at:list>
        <at:appl at:fun="foo"/>
        <at:appl at:fun="bar"/>
      </at:list>
    </at:appl>

    fred([foo,bar])

    fred(None, [foo, bar])

    <at:appl xmlns:at="http://aterm.org" at:fun="fred">
      <at:appl at:fun="None"/>
      <at:list>
        <at:appl at:fun="foo"/>
        <at:appl at:fun="bar"/>
      </at:list>
    </at:appl>

    fred(None,[foo,bar])

    fred(Some(barney), [foo, bar])

    <at:appl xmlns:at="http://aterm.org" at:fun="fred">
      <at:appl at:fun="Some">
        <at:appl at:fun="barney"/>
      </at:appl>
      <at:list>
        <at:appl at:fun="foo"/>
        <at:appl at:fun="bar"/>
      </at:list>
    </at:appl>

    fred(Some(barney),[foo,bar])

    fred("foo", "bar")

    <at:appl xmlns:at="http://aterm.org" at:fun="fred">
      <at:string>
        <at:value>foo</at:value>
      </at:string>
      <at:string>
        <at:value>bar</at:value>
      </at:string>
    </at:appl>

    fred("foo","bar")

    foo{fred}

    <at:appl xmlns:at="http://aterm.org" at:fun="foo">
      <at:anno>
        <at:appl at:fun="fred"/>
      </at:anno>
    </at:appl>

    foo{fred}

### []{#Implicit_XML} Implicit XML

ATerm

Implicit XML

Back to ATerm

    foo

    <foo xmlns:at="http://aterm.org"/>

    foo

    foo(1)

    <foo xmlns:at="http://aterm.org">1</foo>

    foo("1")

    1

not possible

not possible

    "abc"

not possible

not possible

    ()

not possible

not possible

    (1, 2)

not possible

not possible

    []

not possible

not possible

    [1, 2]

not possible

not possible

    fred([foo, bar])

    <fred xmlns:at="http://aterm.org">
      <foo/>
      <bar/>
    </fred>

    fred(foo,bar)

    fred(None, [foo, bar])

    <fred xmlns:at="http://aterm.org">
      <foo/>
      <bar/>
    </fred>

    fred(foo,bar)

    fred(Some(barney), [foo, bar])

    <fred xmlns:at="http://aterm.org">
      <barney/>
      <foo/>
      <bar/>
    </fred>

    fred(barney,foo,bar)

    fred("foo", "bar")

    <fred xmlns:at="http://aterm.org">foobar</fred>

    fred("foobar")

    foo{fred}

    <foo xmlns:at="http://aterm.org">
      <at:anno>
        <fred/>
      </at:anno>
    </foo>

    foo{fred}

\
[]{#TopicEnd}

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
