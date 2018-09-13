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
    Page](http://www.program-transformation.org/edit/Spoofax/ExampleIni?t=1536826261)
-   [Rename
    Page](http://www.program-transformation.org/rename/Spoofax/ExampleIni)
-   [Attach
    File](http://www.program-transformation.org/attach/Spoofax/ExampleIni)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Spoofax/ExampleIni?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Spoofax/ExampleIni?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Spoofax/ExampleIni?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Spoofax/ExampleIni)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Spoofax/ExampleIni?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Spoofax/ExampleIni?template=oopsmore&param1=1.1&param2=1.1)
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
Example Ini {#example-ini .twikiTopicTitle}
===========

::: {.twikiWebTitle}
Spoofax
:::

Example `eclipse.ini` file, taken from an OS X system:

    -startup
    ../../../plugins/org.eclipse.equinox.launcher_1.1.0.v20100507.jar
    --launcher.library
    ../../../plugins/org.eclipse.equinox.launcher.cocoa.macosx.x86_64_1.1.0.v20100503
    -showsplash
    org.eclipse.platform
    --launcher.XXMaxPermSize
    256m
    --launcher.defaultAction
    openFile
    -vmargs
    -Xss8m
    -Xms256m
    -Xmx1024m
    -XX:MaxPermSize=256m
    -server
    -Xdock:icon=../Resources/Eclipse.icns
    -XstartOnFirstThread
    -Dorg.eclipse.swt.internal.carbon.smallFonts
    -Djava.net.preferIPv4Stack=true

Note that every option appears on a separate line, with no following
spaces, and that the memory options appear *after* the `-vmargs` option.
The `-Xmx` and `-Xms` options replace corresponding options that may
have been in the existing file. Setting these options ensures that
Eclipse has sufficient memory to dynamically load editors and is
prepared for a full meta-programming environment.

[(back to download page)](Download){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
