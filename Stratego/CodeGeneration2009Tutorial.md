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
    Page](http://www.program-transformation.org/edit/Stratego/CodeGeneration2009Tutorial?t=1536825569)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/CodeGeneration2009Tutorial)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/CodeGeneration2009Tutorial)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/CodeGeneration2009Tutorial?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/CodeGeneration2009Tutorial?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Stratego/CodeGeneration2009Tutorial?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/CodeGeneration2009Tutorial?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Stratego/CodeGeneration2009Tutorial?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/CodeGeneration2009Tutorial?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/CodeGeneration2009Tutorial?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/CodeGeneration2009Tutorial?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/CodeGeneration2009Tutorial)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/CodeGeneration2009Tutorial?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Stratego/CodeGeneration2009Tutorial?template=oopsmore&param1=1.9&param2=1.9)
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
Code Generation 2009 Tutorial {#code-generation-2009-tutorial .twikiTopicTitle}
=============================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The software for the Code Generation 2009 Tutorial is available through
a virtual machine. To run this virtual machine you need a recent version
of [VirtualBox](http://www.virtualbox.org/wiki/Downloads) (version 2.2
or higher).

The virtual machine contains an Ubuntu 9.04 install, including the
necessary [StrategoXT](StrategoXT){.twikiLink} components:

-   [StrategoXT](StrategoXT){.twikiLink}, including the manual
-   [JavaFront](JavaFront){.twikiLink}
-   [WebDSL](WebDSL){.twikiLink}
-   [WebDSL](WebDSL){.twikiLink} source code
-   Tomcat

If you have any questions, please feel free to send an email to

-   [Rob Vermaas](mailto:rob.vermaas@gmail.com)
    (<rob.vermaas@gmail.com>)
-   [Eelco Visser](mailto:visser@acm.org) (<visser@acm.org>)

or go to the \#stratego IRC channel on irc.freenode.net.

[]{#Installation} Installation
------------------------------

The virtual machine image can be downloaded:

-   <ftp://ftp.strategoxt.org/pub/stratego/vm/CodeGen.zip>

The zip file is approximately 1.5GB compressed, and you need about 4GB
of space for the uncompressed image.

After downloading

-   unzip the downloaded file
-   start Virtual Box
-   Press *New* button, which starts a wizard, press next
-   Enter a name for the virtual machine, and fill in:
    -   Operating system: Linux
    -   Version: Ubuntu
-   Press Next
-   Enter the amount of memory available in the virtual machine, we
    recommend at least 512MB
-   Press Next
-   Select *use existing harddisk*, and press on the button next to the
    dropdown box to go to the Virtual Media Manager
    -   Press *Add* button
    -   Choose the downloaded and extracted disk image (CodeGen.vdi) and
        select *Open*
    -   Then press *Select* button, which closes the Virtual Media
        Manager
-   Press *Next*, which will show a summary of what you have just done
-   Press *Finish* to add the machine to your VirtualBox

Now, the virtual machine is available in Virtualbox, and it is possible
to start the machine. Username and password for the default login is
**guest**.

The sample application for the tutorial is available in
*/home/guest/src/tutorial*.

[]{#Testing_image} Testing image
--------------------------------

To check if the image is correctly installed,

-   open terminal (menu Applications/Accessoires/Terminal)
-   *cd src*
-   *./build-webdsl-svn*
-   *cd tutorial*
-   *webdsl build deploy*, to deploy the sample application
-   start Tomcat using the desktop item
-   start firefox and point browser to <http://localhost:8080/tasks/>

[]{#Shared_folders} Shared folders
----------------------------------

To mount a shared folder (from VirtualBox)

-   In VirtualBox, go to menu *Devices*, then *Shared Folders*
-   Choose *Add* and fill in \* Folder Path: / (to share the root
    filesystem of the host) \* Folder Name: share
-   Press OK
-   open terminal (menu Applications/Accessoires/Terminal)
-   Execute: *mount-shared share /home/guest/Desktop/share* to mount the
    shared folder with name \'share\' to a folder on your desktop.

[]{#Issues} Issues
------------------

-   in some cases networking does not work immediately. Open a terminal
    (e.g. alt-f2, then type gnome-terminal or menu
    *Applications/Accessoires/Terminal*) and execute: **sudo
    /etc/init.d/networking restart**. (Password *guest*.)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
