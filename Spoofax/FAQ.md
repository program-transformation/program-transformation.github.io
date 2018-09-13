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
    Page](http://www.program-transformation.org/edit/Spoofax/FAQ?t=1536826250)
-   [Rename
    Page](http://www.program-transformation.org/rename/Spoofax/FAQ)
-   [Attach
    File](http://www.program-transformation.org/attach/Spoofax/FAQ)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Spoofax/FAQ?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Spoofax/FAQ?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    41](http://www.program-transformation.org/view/Spoofax/FAQ?rev=1.41)
    [(diff 40)](http://www.program-transformation.org/rdiff/Spoofax/FAQ?rev1=1.41&rev2=1.40)
-   [Rev
    40](http://www.program-transformation.org/view/Spoofax/FAQ?rev=1.40)
    [(diff 39)](http://www.program-transformation.org/rdiff/Spoofax/FAQ?rev1=1.40&rev2=1.39)
-   [Rev
    39](http://www.program-transformation.org/view/Spoofax/FAQ?rev=1.39)
    [(diff 38)](http://www.program-transformation.org/rdiff/Spoofax/FAQ?rev1=1.39&rev2=1.38)
-   [Total
    History](http://www.program-transformation.org/rdiff/Spoofax/FAQ)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Spoofax/FAQ?template=oopsmore&param1=1.41&param2=1.41)
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
    \...](http://www.program-transformation.org/oops/Spoofax/FAQ?template=oopsmore&param1=1.41&param2=1.41)
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
FAQ {#faq .twikiTopicTitle}
===

::: {.twikiWebTitle}
Questions about all things Spoofax
:::

#### []{#Updates_of_Spoofax_cause_Eclipse} Updates of Spoofax cause Eclipse to time out; why?

Due to a known problem with the combination of Eclipse 3.7, Java 1.7,
and Windows, the update manager can be very slow or time out when
downloading plugins. As a workaround, you can add the option
`-Djava.net.preferIPv4Stack=true` to your `eclipse.ini` file, as
described on the [Download](Download){.twikiLink} page.

#### []{#Sometimes_Spoofax_says_see_error} Sometimes Spoofax says \"see error log.\" Where can I find it?

Go to *Window \> Show view \> Error log*.

[]{#vcs}

#### []{#Which_files_of_a_language_projec} Which files of a language project should I check into my SVN/CVS/GIT/etc. version management system?

You should check in all files, except for the `bin` and `include`
distribution directories. Some Spoofax projects also have a `utils`
directory that does not have to be checked in. Be sure to check in the
hidden files/directories that Eclipse maintains (`.project`,
`.classpath`, and `.externalToolBuilders`). If you use an Eclipse plugin
such as [Subclipse](http://subclipse.tigris.org), it\'ll check these
files in automatically. If you want, you can skip some of the
`.generated` files, but at this point the `build.generated.xml` and
`lib/editor-common.generated.str` files are required to build the
project.

[]{#jar}

#### []{#How_can_I_compile_my_Stratego_sp} How can I compile my Stratego specification to a JAR file instead of an interpreted ctree?

In your `build.main.xml` file, change this line:

    <target name="all" depends="spoofaximp.default.ctree"/>

into

    <target name="all" depends="spoofaximp.default.jar"/>

Then in your `editor/YourLanguage-Builders.esv`, change the `provider`
from `provider: include/yourlang.ctree` to
`provider: include/yourlang.jar`. (There may already be a
`provider: include/yourlang-java.jar` entry there.) When you distribute
your plugin, be sure you set the \"unpack\" option to \"true\" for your
plugin.

#### []{#How_do_I_deploy_my_language_plug} How do I deploy my language plugin to other users?

Either distribute it in source form to other Spoofax users, or follow
the steps of our [Tour](Tour#Plugin_deployment){.twikiAnchorLink} to
distribute it as an Eclipse plugin that does not require an existing
installation of Spoofax.

#### []{#How_can_I_use_Spoofax_with_C_bas} How can I use Spoofax with C-based Stratego projects?

Stratego projects written with the C version of Stratego typically have
a very different project structure from the one employed by Spoofax
projects. To migrate these projects to Spoofax, we advise users to
create a new Spoofax project with a wizard and adapt the existing
project to this structure. The \`build.main.xml\` file can be used to
set any Stratego options and file locations for use with the Ant build
system. Also see the next question.

#### []{#How_can_I_suppress_errors_in_the} How can I suppress errors in the Stratego editor in legacy Stratego projects?

Add a file called \`.disable-global-analysis\` to disable all non-local
errors. Any local errors such as missing local variables will still be
reported, but non-local errors such as missing strategies or
constructors will then be ignored. Use \`.warn-global-analysis\` to
print warnings instead for non-local errors.

#### []{#If_I_have_two_versions_of_the_sa} If I have two versions of the same language in my workspace, which one will be used?

If you have two versions of a language (e.g., one version installed as a
plugin and another loaded from source), the last version that you loaded
\"wins.\" Any Java components loaded using the default Eclipse plugin
system can only be loaded from installed.

#### []{#How_can_I_call_Java_methods_from} How can I call Java methods from my editor?

See [The Tour: Adding Java
components](http://strategoxt.org/Spoofax/Tour#Adding_Java_components).

#### []{#When_does_Eclipse_show_the_Spoof} When does Eclipse show the Spoofax console?

The Spoofax console can be used to print debugging messages. It is only
shown for editors that have been dynamically loaded from source; not for
editors that are deployed to end users.

#### []{#How_do_I_debug_my_Stratego_code}[]{#How_do_I_debug_my_Stratego_code_} How do I debug my Stratego code?

Stratego does not have a stepping debugger at this point. Instead, you
can try `<debug(!"some message)> x` to print a message in the console
with the value of term `x`, or just `debug(!"some message")` to print
the message and the current term. You can also use the `with` keyword in
rewrite rules as follows:

    rewrite: x -> x'
    with
      x' := <s> ....

which ensures that a stack trace is printed when the body of the `with`
fails (e.g., because `s` cannot be applied).

#### []{#How_can_I_output_multiple_files}[]{#How_can_I_output_multiple_files_} How can I output multiple files from a Stratego rule?

You can write directly to a file as follows:

    handle := <fopen> ("somefilename.ext", "w");
    <fputs> ("file contents string", handle);
    fclose

If you use this API from a `builder` or `on save` rule, you can change
it to the following form to ensure it only writes files statements like
the above:

    generate-java:
      (selected, position, ast, path, project-path) -> None()

#### []{#How_can_I_use_concrete_syntax_wi} How can I use concrete syntax with Spoofax?

See YellowGrass [issue 55](http://yellowgrass.org/issue/Spoofax/55).

#### []{#When_I_hit_build_project_nothing} When I hit \"build project\" nothing seems to happen? What\'s wrong?

Eclipse must have decided that you already ran the Ant file that
controls the build. Just edit and save one of the files in the project
and try again.

#### []{#Eclipse_gets_very_slow_after_usi} Eclipse gets very slow after using it for some time or when opening many editors

The most common cause of this is a lack of heap memory. The default
Eclipse setting of 256M (or 512M for 64-bit systems) is very small, even
for casual Eclipse users. Please [configure](Download){.twikiLink} your
Eclipse installation to use more memory.

#### []{#How_can_I_refresh_a_file_when_Ec} How can I refresh a file when Eclipse won\'t respond to F5?

This seems to be a common issue in Eclipse. Instead of pressing F5,
right-click on the file in the package explorer and select \"Refresh\".

#### []{#When_implementing_content_propos} When implementing content proposals, what to do when I get a NOCONTEXT term?

The `NOCONTEXT` term indicates that the parser is unable to construct a
valid abstract syntax tree that corresponds to the grammar, for the part
of the tree where content completion is triggered. You can add
additional rules to the grammar to help it make a (partial) tree for
these cases, as documented [on the mailing
list](https://mailman.st.ewi.tudelft.nl/pipermail/users/2010-December/000311.html).
This is an area for future improvement. Don\'t hesitate to ask further
questions about this topic!

[]{#nightly}

#### []{#Where_can_I_find_the_latest_blee} Where can I find the latest bleeding edge versions of Spoofax?

The very latest builds of Spoofax can be downloaded by configuring
Eclipse to use the `http://download.spoofax.org/update/nightly` update
site. These versions are frequently updated, haven\'t undergone
extensive testing, and may break existing features. If you run into any
problems with the nightly releases, make sure you run the latest version
and report the bug with the version number used in the [issue
tracker](http://yellowgrass.org/project/Spoofax). Current resolved and
unresolved issues for the nightly builds are listed in the
[roadmap](http://yellowgrass.org/roadmap/Spoofax).

#### []{#Artifact_not_found_during_instal}[]{#_Artifact_not_found_during_insta} \"Artifact not found\" during installation?

Eclipse can report this error when it tries to download an older version
of Spoofax that is no longer available. (This can especially occur with
the nightly builds.) Restarting Eclipse or going to the \"available
update sites\" dialog and refreshing or deleting and re-adding the
update site should solve this problem.

#### []{#How_do_I_report_a_deadlock}[]{#How_do_I_report_a_deadlock_} How do I report a deadlock?

See [how to report a
deadlock](http://wiki.eclipse.org/How_to_report_a_deadlock) in the
Eclipse wiki.

#### []{#How_do_I_call_Java_functions_fro} How do I call Java functions from Stratego?

You have to wrap them as Stratego strategies. If you generate a new
project, the
`editor/java/YOURLANGUAGE/strategies/java_strategy_0_0.java` class gives
an example. If you want to add strategies to an existing Spoofax
project, you can add further strategy classes to the same directory:

-   Create a new class that extends \`Strategy\`, following the template
    of \`java\_strategy\_0\_0.java\`
-   Add a reference to that class in `InteropRegisterer.java`

#### []{#Where_can_I_find_answers_to_some} Where can I find answers to some of my other questions?

Maybe our [documentation](Documentation){.twikiLink} can answer your
question. Otherwise, the
[YellowGrass](http://yellowgrass.org/project/Spoofax) issue tracker
lists issue reports and questions from other users. You can add your own
question there, or [contact](Support){.twikiLink} us directly.

\
\
\
\
\
\
\
\
\

\
\
\
\
\

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
