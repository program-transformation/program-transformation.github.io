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
    Page](http://www.program-transformation.org/edit/Spoofax/ContinuousBuildingSpoofax?t=1536826250)
-   [Rename
    Page](http://www.program-transformation.org/rename/Spoofax/ContinuousBuildingSpoofax)
-   [Attach
    File](http://www.program-transformation.org/attach/Spoofax/ContinuousBuildingSpoofax)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Spoofax/ContinuousBuildingSpoofax?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Spoofax/ContinuousBuildingSpoofax?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Spoofax/ContinuousBuildingSpoofax?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Spoofax/ContinuousBuildingSpoofax?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Spoofax/ContinuousBuildingSpoofax?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Spoofax/ContinuousBuildingSpoofax)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Spoofax/ContinuousBuildingSpoofax?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Spoofax/ContinuousBuildingSpoofax?template=oopsmore&param1=1.2&param2=1.2)
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
Continuous Building Spoofax {#continuous-building-spoofax .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Spoofax
:::

[]{#Using_Maven_Tycho} Using Maven Tycho
----------------------------------------

Spoofax project can be built continuously using a combination of Maven,
Tycho and Ant. Using Maven should make it easy to run it in a continuous
build server like Hudson. We use the same techniques described here in
[our continuous builds](http://hydra.nixos.org/project/spoofax) on
[Hydra](http://nixos.org/hydra).

Make sure you have the following software installed:

-   [Maven 3.0](http://maven.apache.org/)
-   Ant
-   Eclipse with Spoofax installed

For this example we assume you have installed eclipse in **\$ECLIPSE**.

This description is based on the following [Nix](http://nixos.org)
expression we use in our continuous builds:

-   <https://svn.strategoxt.org/repos/StrategoXT/hydra/spoofax-fun.nix>
-   <https://svn.strategoxt.org/repos/StrategoXT/hydra/eclipse.nix>

### []{#Installing_Spoofax_from_command}[]{#Installing_Spoofax_from_command_} Installing Spoofax from command-line

You can install Eclipse and Spoofax like described
[here](Download){.twikiLink}. However, in a continuous build/integration
setting it is sometimes useful to be able to perform these actions from
the command-line. *Note that this script uses the Spoofax unstable
update site*.

    cd $ECLIPSE

    # remove vm args
    sed -i 's|-Xms[0-9]*m||' eclipse.ini
    sed -i 's|-Xss[0-9]*m||' eclipse.ini
    sed -i 's|-Xmx[0-9]*m||' eclipse.ini
    sed -i 's|-XX:MaxPermSize=[0-9]*m||' eclipse.ini
    sed -i '/^$/d' eclipse.ini
    perl -pi -e "s/^\r\n//" eclipse.ini

    # add own default vmwargs
    echo "-Xms256m" >> eclipse.ini
    echo "-Xss8m" >> eclipse.ini
    echo "-Xmx1024m" >> eclipse.ini
    echo "-XX:MaxPermSize=256m" >> eclipse.ini
    echo "-server" >> eclipse.ini

    # install spoofax
    ALL_SITES="http://spoofax.org/update/unstable"
    java -Xmx512m -jar plugins/org.eclipse.equinox.launcher_*.jar  \
         -application org.eclipse.equinox.p2.director \
         -metadataRepository $ALL_SITES \
         -artifactRepository $ALL_SITES \
         -installIU org.strategoxt.imp.feature.group \
         -data ../data \
         -consolelog

### []{#Setting_up_Maven} Setting up Maven

Create a directory with the editor plugin project, feature project and
update site project in it.

Then issue the following command (replace version and groupId with
something appropriate) to generate the maven pom.xml files:

    mvn org.sonatype.tycho:maven-tycho-plugin:generate-poms -Dversion=1.0-SNAPSHOT -DgroupId=mygroup -Dtycho.targetPlatform=$ECLIPSE

If you want to run tests, like JUnit tests, make sure you add org.junit4
to your plugin dependencies and MANIFEST.MF. If your tests reside in
your main plugin, you will need to edit the generated pom.xml file of
that plugin. Replace,

      <packaging>eclipse-plugin</packaging>

by,

      <packaging>eclipse-test-plugin</packaging>

If you have your tests in a seperate plugin which name ends with
*tests*, Tycho should recognize this and change the packaging element
for you.

### []{#Running_ant_builds} Running ant builds

Before running Maven you need to use build.main.xml of the Spoofax
project(s) to generate some code/files that spoofax normally generates
automatically from Eclipse (parsetables, java code from stratego, etc.)


    export LOCALCLASSPATH="utils/aster.jar:utils/make_permissive.jar:utils/sdf2imp.jar:utils/strategoxt.jar"
    export ANT_OPTS="-Xss8m -Xmx2048m"
    export PATH=$PATH:$ECLIPSE/plugins/org.strategoxt.imp.nativebundle_*/native/linux/

    for d in */build.main.xml ; do
      cd `dirname $d`
      mkdir -p utils 
      cp -Rv `find $ECLIPSE -name strategoxt.jar` utils/
      cp -Rv `find $ECLIPSE -name aster.jar` utils/
      cp -Rv `find $ECLIPSE -name sdf2imp.jar` utils/
      cp -Rv `find $ECLIPSE -name make_permissive.jar` utils/
      ant -f build.main.xml -Declipse.spoofaximp.jars=utils all
      cd ..
    done

### []{#Running_Maven_build} Running Maven build

When this is done, the project can be built using:

    mvn package -Dtycho.targetPlatform=$ECLIPSE -e

If this is done successfully, you should have an update site available
in your update site project directory.

If you would like to run the testsuites perform:

    mvn integration-test -Dtycho.targetPlatform=$ECLIPSE -e

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
