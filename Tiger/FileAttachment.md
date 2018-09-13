::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![Stratego
logo](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)

------------------------------------------------------------------------

***Tiger in Stratego***

------------------------------------------------------------------------

**[WebHome](WebHome){.twikiLink}**\
[Tiger Compiler](TigerCompiler){.twikiLink}\
[Architecture](CompilerArchitecture){.twikiLink}\
[Packages](CompilerPackages){.twikiLink}\
[Components](CompilerComponent){.twikiLink}\
[Glossary](WebGlossary){.twikiLink}

[Download](DownloadAndInstallation){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tiger/FileAttachment?t=1536826696)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/FileAttachment)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/FileAttachment)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/FileAttachment?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/FileAttachment?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/FileAttachment?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/FileAttachment)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/FileAttachment?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/FileAttachment?template=oopsmore&param1=1.1&param2=1.1)
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
File Attachment {#file-attachment .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

[]{#File_Attachments} File Attachments
======================================

*Each topic can have one or more files of any type attached to it by
using the Attach screen to upload (or download) files from your local
PC. Attachments are stored under revision control: uploads are
automatically backed up; all previous versions of a modified file can be
retrieved.*

[]{#What_Are_Attachments_Good_For}[]{#What_Are_Attachments_Good_For_} What Are Attachments Good For?
----------------------------------------------------------------------------------------------------

File Attachments can be used to create powerful customized groupware
solutions, like file sharing and document management systems, and quick
Web page authoring.

### []{#Document_Management_System} Document Management System

-   You can use Attachments to store and retrieve documents (in any
    format, with associated graphics, and other media files); attach
    documents to specific TWiki topics; collaborate on documents with
    full revision control; distribute documents on a [need-to-know
    basis](../TWiki/FileAttachment#AttachmentAccess){.twikiAnchorLink}
    using web and topic-level access control; create a central reference
    library that\'s easy to share with an user group spread around the
    world.

### []{#File_Sharing} File Sharing

-   For file sharing,
    [FileAttachments](../TWiki/FileAttachment){.twikiLink} on a series
    of topics can be used to quickly create a well-documented,
    categorized digital download center for all types of files:
    documents; graphics and other media; drivers and patches;
    applications; anything you can safely upload!

### []{#Web_Authoring} Web Authoring

-   Through your Web browser, you can easily upload graphics (or sound
    files, or anything else you want to link to on a page) and place
    them on a single page, or use them across a web, or site-wide.
    -   ***NOTE:*** You can also add graphics - any files - directly,
        typically by FTP upload. This requires FTP access, and may be
        more convenient if you have a large number of files to load.
        FTP-ed files can\'t be managed using browser-based Attachment
        controls. You can use your browser to create
        [TWikiVariables](../TWiki/TWikiVariables){.twikiLink} shortcuts,
        like this %H% =
        ![HELP](../pub/TWiki/TWikiDocGraphics/help.gif){width="16"
        height="16"}.

[]{#Uploading_Files} Uploading Files
------------------------------------

-   Click on the `Attach` link at the bottom of the page. The `Attach`
    screen lets you browse for a file, add a comment, and upload it. The
    uploaded file will show up in the [File Attachment
    table](../TWiki/FileAttachment#FileAttachmentTable){.twikiAnchorLink}.
    -   ***NOTE:*** The topic must already exist. It is a two step
        process if you want to attach a file to a non-existing topic;
        first create the topic, then add the file attachment.
    -   Any type of file can be uploaded. Some files that might pose a
        security risk are renamed, ex: `*.php` files are renamed to
        `*.php.txt` so that no one can place code that would be read in
        a .php file.
    -   The previous upload path is retained for convenience. In case
        you make some changes to the local file and want to upload it,
        again you can copy the previous upload path into the Local file
        field.
    -   TWiki can limit the file size. This is defined by the
        `%ATTACHFILESIZELIMIT%` variable of the
        [TWikiPreferences](../TWiki/TWikiPreferences){.twikiLink},
        currently set at 100000 KB.
        -   ![ALERT!](../pub/TWiki/TWikiDocGraphics/warning.gif){width="16"
            height="16"} It\'s not recommended to upload files greater
            than a few hundred K through a browser. Large files can be
            extremely slow-loading, and often time out. Use an FTP site
            for large file uploads.

[]{#Downloading_Files} Downloading Files
----------------------------------------

-   Click on the file in the [File Attachment
    table](../TWiki/FileAttachment#FileAttachmentTable){.twikiAnchorLink}.

[]{#AttachmentAccess}

-   ![ALERT!](../pub/TWiki/TWikiDocGraphics/warning.gif){width="16"
    height="16"} *NOTE:* There is no access control on individual
    attachments. If you need control over single files, create a
    separate topic per file and set topic-level [access
    restrictions](../TWiki/TWikiDocumentation#TWikiAccessControl){.twikiAnchorLink}
    for each.

[]{#Moving_Attachment_Files} Moving Attachment Files
----------------------------------------------------

An attachment can be moved between topics.

-   Click `Manage` on the Attachment to be moved.
-   On the control screen, select the new web and/or topic.
-   Click `Move`. The attachment and its version history are moved. The
    original location is stored as [topic Meta
    Data](../TWiki/TWikiDocumentation#Meta_Data_Definition){.twikiAnchorLink}.

[]{#Deleting_Attachments} Deleting Attachments
----------------------------------------------

Move unwanted Attachments to web `Trash`, topic `TrashAttachment`.

[]{#Linking_to_Attached_Files} Linking to Attached Files
--------------------------------------------------------

-   Once a file is attached it can be referenced in the topic. Example:
    1.  `Attach` file: `Sample.txt`
    2.  `Edit` topic and enter: `%ATTACHURL%/Sample.txt`
    3.  `Preview`: `%ATTACHURL%/Sample.txt` text appears as:
        /pub/TWiki/FileAttachment/Sample.txt, a link to the text file.

<!-- -->

-   To reference an attachment located in another topic, enter:
    -   `%PUBURL%/%WEB%/OtherTopic/Sample.txt` (if it\'s within the same
        web)
    -   `%PUBURL%/Otherweb/OtherTopic/Sample.txt` (if it\'s in a
        different web)

<!-- -->

-   Attached HTML files and text files can be inlined in a topic.
    Example:
    1.  `Attach` file: `Sample.txt`
    2.  `Edit` topic and write text:
        `%INCLUDE{"%ATTACHURL%/Sample.txt"}%`
        -   Content of attached file is shown inlined.
        -   Read more in
            [IncludeTopicsAndWebPages](http://www.program-transformation.org/TWiki/IncludeTopicsAndWebPages){.twikiLink}.

<!-- -->

-   GIF, JPG and PNG images can be attached and shown embedded in a
    topic. Example:
    1.  `Attach` file: `Smile.gif`
    2.  `Edit` topic and write text: `%ATTACHURL%/Smile.gif`
    3.  `Preview`: text appears as /pub/TWiki/FileAttachment/Smile.gif,
        an image.

[]{#FileAttachmentTable}

[]{#File_Attachment_Contents_Table} File Attachment Contents Table
------------------------------------------------------------------

Files attached to a topic are displayed in a directory table, displayed
at the bottom of the page, or optionally, hidden and accessed when you
click **Attach**.

> +-----------------------------------------------------------------------+
> |   **[Attachment](FileAttachment)**                                    |
> |                                                        **Action**     |
> |                                                                       |
> |                            **Size** **Date**              **Who**     |
> |                   **Comment**                                         |
> |   ------------------------------------------------------------------- |
> | ------------------------------------------------------ -------------- |
> | --------------------------------------------------------------------- |
> | ------------------------ ---------- --------------------- ----------- |
> | ----------------- ---------------                                     |
> |   ![](../pub/icn/txt.gif){width="16" height="16"} [Sample.txt](../vie |
> | wfile/TWiki/FileAttachment@rev=&filename=Sample.txt)   [manage](http: |
> | //www.program-transformation.org/attach/TWiki/FileAttachment?filename |
> | =Sample.txt&revInfo=1)        0.1 K 22 Jul 2000 - 19:37   [PeterThoen |
> | y](PeterThoeny)   Just a sample                                       |
> |   ![](../pub/icn/bmp.gif){width="16"} [Smile.gif](../viewfile/TWiki/F |
> | ileAttachment@rev=&filename=Smile.gif)                 [manage](http: |
> | //www.program-transformation.org/attach/TWiki/FileAttachment?filename |
> | =Smile.gif&revInfo=1)         0.1 K 22 Jul 2000 - 19:38   [PeterThoen |
> | y](PeterThoeny)   Smiley face                                         |
> +-----------------------------------------------------------------------+
>
[]{#File_Attachment_Controls} File Attachment Controls
------------------------------------------------------

Clicking on a `Manage` link takes you to a new page that looks like
this:

> +-----------------------------------------------------------------------+
> |   **[Attachment](FileAttachment)**                                    |
> |                                                              **Action |
> | **                                                                    |
> |                                  **Size** **Date**              **Who |
> | **                      **Comment**      **[Attribute](FileAttribute) |
> | **                                                                    |
> |   ------------------------------------------------------------------- |
> | ------------------------------------------------------------ -------- |
> | --------------------------------------------------------------------- |
> | ------------------------------ ---------- --------------------- ----- |
> | ----------------------- --------------- ----------------------------- |
> | ---                                                                   |
> |   ![](../pub/icn/txt.gif){width="16" height="16"} [Sample.txt](../vie |
> | wfile/TWiki/TWiki/FileAttachment@rev=&filename=Sample.txt)   [manage] |
> | (http://www.program-transformation.org/attach/TWiki/FileAttachment?fi |
> | lename=Sample.txt&revInfo=1)        0.1 K 22 Jul 2000 - 19:37   [Pete |
> | rThoeny](PeterThoeny)   Just a sample                                 |
> |   ![](../pub/icn/bmp.gif){width="16" height="16"} [Smile.gif](../view |
> | file/TWiki/FileAttachment@rev=&filename=Smile.gif)           [manage] |
> | (http://www.program-transformation.org/attach/TWiki/FileAttachment?fi |
> | lename=Smile.gif&revInfo=1)         0.1 K 22 Jul 2000 - 19:38   [Pete |
> | rThoeny](PeterThoeny)   Smiley face                                   |
> |                                                                       |
> | Update attachment `Sample.txt`                                        |
> | ------------------------------                                        |
> |                                                                       |
> |   **Version**   **Action**                                            |
> |                   **Date**              **Who**                       |
> | **Comment**                                                           |
> |   ------------- ----------------------------------------------------- |
> | ----------------- --------------------- ----------------------------  |
> | -------------                                                         |
> |   1.1           [view](../viewfile/TWiki/FileAttachment@rev=1.1&filen |
> | ame=Sample.txt)   2001.08.30.09.28.56   [PeterThoeny](PeterThoeny)    |
> |                                                                       |
> |                                                                       |
> |   ------------- ----------------------------------------------------- |
> | --------                                                              |
> |       Previous\ `C:\DATA\Sample.txt` ([PeterThoeny](PeterThoeny))     |
> |         upload:                                                       |
> |                                                                       |
> |     Local file:                                                       |
> |                                                                       |
> |        Comment:                                                       |
> |                                                                       |
> |           Link: Create a link to the attached file at the end of the  |
> | topic.                                                                |
> |                                                                       |
> |      Hide file: Hide attachment in normal topic view.                 |
> |   ------------- ----------------------------------------------------- |
> | --------                                                              |
> |                                                                       |
> | *Help text \...*                                                      |
> |                                                                       |
> | Topic **FileAttachment** . { \| \| [Move                              |
> | attachment](http://www.program-transformation.org/rename/TWiki/FileAt |
> | tachment?attachment=Sample.txt)                                       |
> | \| [Cancel](FileAttachment) }                                         |
> +-----------------------------------------------------------------------+
>
-   The first table is a list of all attachments, including their
    attributes. An `h` means the attachment is hidden, it isn\'t listed
    when viewing a topic.

<!-- -->

-   The second table is all the versions of the attachment. Click on
    **View** to see that version. If it\'s the most recent version,
    you\'ll be taken to an URL that always displays the latest version,
    which is usually what you want.
    -   **To change the comment** on an attachment, enter a new comment
        and then click **Change properties**. Note that the comment
        listed against the specific version will not change, however the
        comment displayed when viewing the topic does change.
    -   **To hide/unhide** an attachment, enable the `Hide file`
        checkbox, then click `Change properties`.

[]{#Known_Issues} Known Issues
------------------------------

-   Unlike topics, attachments are not locked during editing. As a
    workaround, you can change the comment to indicate an attachment
    file is being worked on - the comment on the specific version isn\'t
    lost, it\'s there when you list all versions of the attachment.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
