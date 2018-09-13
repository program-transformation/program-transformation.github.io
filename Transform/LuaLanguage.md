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
    Page](http://www.program-transformation.org/edit/Transform/LuaLanguage?t=1536826514)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/LuaLanguage)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/LuaLanguage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/LuaLanguage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/LuaLanguage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/LuaLanguage?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/LuaLanguage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/LuaLanguage?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/LuaLanguage?template=oopsmore&param1=1.1&param2=1.1)
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
Lua Language {#lua-language .twikiTopicTitle}
============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Lua_the_Programming_Language} Lua the Programming Language
==============================================================

Lua is a powerful light-weight programming language designed for
extending applications. Lua is also frequently used as a
general-purpose, stand-alone language. Lua is free software.

Lua combines simple procedural syntax with powerful data description
constructs based on associative arrays and extensible semantics. Lua is
dynamically typed, interpreted from bytecodes, and has automatic memory
management with garbage collection, making it ideal for configuration,
scripting, and rapid prototyping.

A fundamental concept in the design of Lua is to provide meta-mechanisms
for implementing features, instead of providing a host of features
directly in the language. For example, although Lua is not a pure
object-oriented language, it does provide meta-mechanisms for
implementing classes and inheritance. Lua\'s meta-mechanisms bring an
economy of concepts and keep the language small, while allowing the
semantics to be extended in unconventional ways. Extensible semantics is
a distinguishing feature of Lua.

Lua is a language engine that you can embed into your application. This
means that, besides syntax and semantics, Lua has an
[API](API){.twikiLink} that allows the application to exchange data with
Lua programs and also to extend Lua with C functions. In this sense, Lua
can be regarded as a language framework for building domain-specific
languages.

Lua is implemented as a small library of C functions, written in ANSI C,
and compiles unmodified in all known platforms. The implementation goals
are simplicity, efficiency, portability, and low embedding cost. The
result is a fast language engine with small footprint, making it ideal
in embedded systems too.

Lua is designed and implemented by a team at Tecgraf, the Computer
Graphics Technology Group of PUC-Rio (the Pontifical Catholic University
of Rio de Janeiro in Brazil). Tecgraf is a laboratory of the Department
of Computer Science.

<http://www.lua.org/> \| [lua wiki](http://lua-users.org/wiki/) \|
[Reference manual for Lua 5.0](http://www.lua.org/manual/5.0/) \|
[history](http://www.lua.org/history.html)

[]{#articles_papers_references} articles / papers / references
--------------------------------------------------------------

-   \"Lua: an Extensible Embedded Language\" A few metamechanisms
    replace a host of features <http://www.lua.org/ddj.html>
    -   DDJ article Reprint from Dr. Dobb\'s Journal 21 \#12 (Dec 1996)
        26-33. Copyright © 1996 Miller Freeman, Inc.
-   \"Lua-an extensible extension language\"
    <http://www.lua.org/spe.html>
    -   SPE paper Reprint from Software: Practice & Experience 26
        \#6 (1996) 635-652. Copyright © 1996 John Wiley & Sons, Ltd.

### []{#game_specific} game-specific

-   Lua:LuaVersusPython
-   [GBALua](http://www.gatesboy.com/Lua/Documentation/FAQ.html) GBALua
    is a development environment that enables users to develop
    applications for GBA using Lua or a mixture of both Lua and C/C++.
    This environment is mainly intended for two types of users groups.
    First group is the beginner programmers that have none or limited
    C/C++/Asm knowledge but still would like the try creating some
    simple gba stuff. The other group is those that would like to use it
    as an simple and quick prototyping environment on the GBA.
-   sample nebula lua code:
    [main](http://saneasylum.ath.cx:8080/cgi-bin/viewcvs.cgi/sas-nebula-contrib/onion/nebula/data/onion/onion.lua?rev=HEAD&content-type=text/vnd.viewcvs-markup)
    [class](http://saneasylum.ath.cx:8080/cgi-bin/viewcvs.cgi/sas-nebula-contrib/onion/nebula/data/onion/onion.class.lua?rev=HEAD&content-type=text/vnd.viewcvs-markup)

[]{#tools_libraries} tools / libraries
--------------------------------------

-   <http://lua-users.org/wiki/LuaAddonsArchive>
-   <http://tbayne.dyndns.org/Projects/lash.php> lua shell
-   gtk2: <http://www.starynkevitch.net/Basile/guisdoc.html> [Some
    comments on
    this[^?^](http://www.program-transformation.org/edit/Transform/GamedevGuisApproach?topicparent=Transform.LuaLanguage)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   wxWindows: <http://www.luascript.thersgb.net/index.htm>
-   corba/org: <http://www.tecgraf.puc-rio.br/luaorb/>
-   xml: <http://lua-users.org/wiki/LuaXml>
-   <http://www.unixreview.com/documents/s=2427/uni1021991894316/0205h.htm>
-   [SqLite[^?^](http://www.program-transformation.org/edit/Transform/SqLite?topicparent=Transform.LuaLanguage)]{.twikiNewLink
    style="background : #FFFFCE;"}: Lua:LuaSqlite
    -   is this old (lua4)?
        <http://domingo.dad-it.com/ws-lua-sqlite.whtm>

### []{#debuggers_ide_s} debuggers / ide\'s

-   <http://www.lcc.ufrn.br/~milano/ild/index.html>
-   <http://lua-users.org/wiki/SimpleDebugger>
-   <http://www.tecgraf.puc-rio.br/~scuri/luacmd/>
-   <http://www.gorlice.net.pl/~rybak/luaide/>
-   <http://zerbe.homeunix.net/edelua.htm> embeddable development
    environment
-   <http://www.tecgraf.puc-rio.br/~tomas/ldb/> lua debugger page
    -   <http://www.inf.puc-rio.br/~roberto/ldb.html> another lua
        debugger page?
    -   <http://www.inf.puc-rio.br/~roberto/ldb.tar.gz> debugger
    -   <http://www.inf.puc-rio.br/~roberto/ldbman.ps.gz> manual
-   <http://www.xtgsystems.com/linux/lua/titmouse.php>
-   <http://www.scintilla.org/> ( a free source code editing component
    for Win32 and GTK+\--not lua-specific )

\-- [WillNorris](../Main/WillNorris){.twikiLink} - 23 May 2003

[]{#Standard_libs} Standard libs
--------------------------------

-   <http://lua-users.org/wiki/StandardLibraries>

<!-- -->

-   <http://sashipa.ben.free.fr/dcplaya/Documentation/html/group__dcplaya__lua__basics__library.html>

[]{#Lua_XML_Parser} Lua [XML](XML){.twikiLink} Parser
-----------------------------------------------------

-   <http://lua-users.org/wiki/LuaXml>

[]{#Lua_tools} Lua tools
------------------------

-   <http://www.place.org/~nop/lua/>

[]{#wxLua} wxLua
----------------

-   wxLua is a binding of the wxWindows classes for the Lua programming
    language.
-   <http://www.luascript.thersgb.net/>

[]{#LuaOrb} [LuaOrb[^?^](http://www.program-transformation.org/edit/Transform/LuaOrb?topicparent=Transform.LuaLanguage)]{.twikiNewLink style="background : #FFFFCE;"}
---------------------------------------------------------------------------------------------------------------------------------------------------------------------

-   This site presents
    [LuaOrb[^?^](http://www.program-transformation.org/edit/Transform/LuaOrb?topicparent=Transform.LuaLanguage)]{.twikiNewLink
    style="background : #FFFFCE;"}, a binding between the interpreted
    language Lua and CORBA. As usual, this binding defines mappings
    between Lua and IDL

types. However, unlike other bindings,
[LuaOrb[^?^](http://www.program-transformation.org/edit/Transform/LuaOrb?topicparent=Transform.LuaLanguage)]{.twikiNewLink
style="background : #FFFFCE;"} relies on the reflexive facilities of
CORBA and the dynamic nature of Lua.

-   <http://www.tecgraf.puc-rio.br/luaorb/>

[]{#Random_Info} Random Info
----------------------------

-   <http://www.lua.org/versions.html>

<!-- -->

-   Currently, Lua has a strong presence whenever programmers need a
    light, efficient, and portable language. It is being used by some
    tens of thousands programmers around the world, both in research and
    in industrial projects. Lua has been successfully used in games
    (e.g. Grim Fandango, Escape from Monkey Island, MK2, Baldur\'s
    Gate), in robots (e.g. Crazy Ivan, that won the Danish
    [RoboCup[^?^](http://www.program-transformation.org/edit/Transform/RoboCup?topicparent=Transform.LuaLanguage)]{.twikiNewLink
    style="background : #FFFFCE;"} in 2000 and 2001), and several other
    applications (e.g. a hot-swappable Ethernet switch (CPC4400), a
    genetic sequence visualization system (GUPPY), \"The most Linux on
    one floppy disk\" (tomsrtbt)). An extended list of applications
    using Lua can be found at <http://www.lua.org/uses.html>

\--
[JohnHinton[^?^](http://www.program-transformation.org/edit/People/JohnHinton?topicparent=Transform.LuaLanguage)]{.twikiNewLink
style="background : #FFFFCE;"} - 27 Oct 2003

\-- [WillNorris](../Main/WillNorris){.twikiLink} - 11 Nov 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
