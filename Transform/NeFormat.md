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
    Page](http://www.program-transformation.org/edit/Transform/NeFormat?t=1536826520)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/NeFormat)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/NeFormat)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/NeFormat?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/NeFormat?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/NeFormat?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/NeFormat?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/NeFormat?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/NeFormat)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/NeFormat?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/NeFormat?template=oopsmore&param1=1.2&param2=1.2)
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
Ne Format {#ne-format .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#New_style_EXE_Format} New-style EXE Format
----------------------------------------------

An executable (.EXE) file for the Windows operating system contains a
combination of code and data or a combination of code, data, and
resources. The executable file also contains two headers: an MS-DOS
header and a Windows header. The next two sections describe these
headers; the third section describes the code and data contained in a
Windows executable file.

::: {.twikiToc}
-   [New-style EXE Format](NeFormat#New_style_EXE_Format)
-   [MS-DOS Header](NeFormat#MS_DOS_Header)
-   [Windows Header](NeFormat#Windows_Header)
-   [Information Block](NeFormat#Information_Block)
-   [Segment Table](NeFormat#Segment_Table)
-   [Resource Table](NeFormat#Resource_Table)
    -   [Type Information](NeFormat#Type_Information)
    -   [Name Information](NeFormat#Name_Information)
-   [Resident-Name Table](NeFormat#Resident_Name_Table)
-   [Module-Reference Table](NeFormat#Module_Reference_Table)
-   [Imported-Name Table](NeFormat#Imported_Name_Table)
-   [Entry Table](NeFormat#Entry_Table)
-   [Nonresident-Name Table](NeFormat#Nonresident_Name_Table)
-   [Code Segments and Relocation
    Data](NeFormat#Code_Segments_and_Relocation_Dat)
:::

[]{#MS_DOS_Header} MS-DOS Header
--------------------------------

The MS-DOS (old-style) executable-file header contains four distinct
parts: a collection of header information (such as the signature word,
the file size, and so on), a reserved section, a pointer to a Windows
header (if one exists), and a stub program. The following illustration
shows the MS-DOS executable-file header: If the word value at offset 18h
is 40h or greater, the word value at 3Ch is typically an offset to a
Windows header. Applications must verify this for each executable-file
header being tested, because a few applications have a different header
style. MS-DOS uses the stub program to display a message if Windows has
not been loaded when the user attempts to run a program.

[]{#Windows_Header} Windows Header
----------------------------------

The Windows (new-style) executable-file header contains information that
the loader requires for segmented executable files. This information
includes the linker version number, data specified by the linker, data
specified by the resource compiler, tables of segment data, tables of
resource data, and so on. The following illustration shows the Windows
executable-file header: The following sections describe the entries in
the Windows executable-file header.

[]{#Information_Block} Information Block
----------------------------------------

The information block in the Windows header contains the linker version
number, the lengths of various tables that further describe the
executable file, the offsets from the beginning of the header to the
beginning of these tables, the heap and stack sizes, and so on. The
following list summarizes the contents of the header information block
(the locations are relative to the beginning of the block):

Location: Description

-   00h: The signature word. The low byte contains \"N\" (4Eh) and the
    high byte contains \"E\" (45h).
-   02h: The linker version number.
-   03h: The linker revision number.
-   04h: The offset to the entry table (relative to the beginning of the
    header).
-   06h: The length of the entry table, in bytes.
-   08h: Reserved.
-   0Ch: Flags that describe the contents of the executable file. This
    value can be one or more of the following bits:
    -   0: The linker sets this bit if the executable-file format is
        SINGLEDATA. An executable file with this format contains one
        data segment. This bit is set if the file is a dynamic-link
        library (DLL).
    -   1: The linker sets this bit if the executable-file format is
        MULTIPLEDATA. An executable file with this format contains
        multiple data segments. This bit is set if the file is a Windows
        application. If neither bit 0 nor bit 1 is set, the
        executable-file format is NOAUTODATA. An executable file with
        this format does not contain an automatic data segment.
    -   2: Reserved.
    -   3: Reserved.
    -   8: Reserved.
    -   9: Reserved.
    -   11: If this bit is set, the first segment in the executable file
        contains code that loads the application.
    -   13: If this bit is set, the linker detects errors at link time
        but still creates an executable file.
    -   14: Reserved.
    -   15: If this bit is set, the executable file is a library module.
        If bit 15 is set, the CS:IP registers point to an initialization
        procedure called with the value in the AX register equal to the
        module handle. The initialization procedure must execute a far
        return to the caller. If the procedure is successful, the value
        in AX is nonzero. Otherwise, the value in AX is zero.\
        The value in the DS register is set to the library\'s data
        segment if SINGLEDATA is set. Otherwise, DS is set to the data
        segment of the application that loads the library.

<!-- -->

-   0Eh: The automatic data segment number. (0Eh is zero if the
    SINGLEDATA and MULTIPLEDATA bits are cleared.)
-   10h: The initial size, in bytes, of the local heap. This value is
    zero if there is no local allocation.
-   12h: The initial size, in bytes, of the stack. This value is zero if
    the SS register value does not equal the DS register value.
-   14h: The segment:offset value of CS:IP.
-   18h: The segment:offset value of SS:SP. The value specified in SS is
    an index to the module\'s segment table. The first entry in the
    segment table corresponds to segment number 1. If SS addresses the
    automatic data segment and SP is zero, SP is set to the address
    obtained by adding the size of the automatic data segment to the
    size of the stack.

<!-- -->

-   1Ch: The number of entries in the segment table.
-   1Eh: The number of entries in the module-reference table.
-   20h: The number of bytes in the nonresident-name table.
-   22h: A relative offset from the beginning of the Windows header to
    the beginning of the segment table.
-   24h: A relative offset from the beginning of the Windows header to
    the beginning of the resource table.
-   26h: A relative offset from the beginning of the Windows header to
    the beginning of the resident-name table.
-   28h: A relative offset from the beginning of the Windows header to
    the beginning of the module-reference table.
-   2Ah: A relative offset from the beginning of the Windows header to
    the beginning of the imported-name table.
-   2Ch: A relative offset from the beginning of the file to the
    beginning of the nonresident-name table.
-   30h: The number of movable entry points.
-   32h: A shift count that is used to align the logical sector. This
    count is log2 of the segment sector size. It is typically 4,
    although the default count is 9. (This value corresponds to the
    /alignment \[/a\] linker switch. When the linker command line
    contains /a:16, the shift count is 4. When the linker command line
    contains /a:512, the shift count is 9.)
-   34h: The number of resource segments.
-   36h: The target operating system, depending on which bits are set:
    -   0: Operating system format is unknown.
    -   1: Reserved.
    -   2: Operating system is Microsoft Windows.
    -   3: Reserved.
    -   4: Reserved.

<!-- -->

-   37h: Additional information about the executable file. It can be one
    or more of the following values: \* 1: If this bit is set, the
    executable file contains a Windows 2.x application that runs in
    version 3.x protected mode.
    -   2: If this bit is set, the executable file contains a Windows
        2.x application that supports proportional fonts.
    -   3: If this bit is set, the executable file contains a fast-load
        area.

<!-- -->

-   38h: The offset, in sectors, to the beginning of the fast-load area.
    (Only Windows uses this value.)
-   3Ah: The length, in sectors, of the fast-load area. (Only Windows
    uses this value.)
-   3Ch: Reserved.
-   3Eh: The expected version number for Windows. (Only Windows uses
    this value.)

[]{#Segment_Table} Segment Table
--------------------------------

The segment table contains information that describes each segment in an
executable file. This information includes the segment length, segment
type, and segment-relocation data. The following list summarizes the
values found in the segment table (the locations are relative to the
beginning of each entry):

-   00h: The offset, in sectors, to the segment data (relative to the
    beginning of the file). A value of zero means no data exists.
-   02h: The length, in bytes, of the segment, in the file. A value of
    zero indicates that the segment length is 64K, unless the selector
    offset is also zero.
-   04h: Flags that describe the contents of the executable file. This
    value can be one or more of the following:
    -   0: If this bit is set, the segment is a data segment. Otherwise,
        the segment is a code segment.
    -   1: If this bit is set, the loader has allocated memory for the
        segment.
    -   2: If this bit is set, the segment is loaded.
    -   3: Reserved.
    -   4: If this bit is set, the segment type is MOVABLE. Otherwise,
        the segment type is FIXED.
    -   5: If this bit is set, the segment type is PURE or SHAREABLE.
        Otherwise, the segment type is IMPURE or NONSHAREABLE.
    -   6: If this bit is set, the segment type is PRELOAD. Otherwise,
        the segment type is LOADONCALL.
    -   7: If this bit is set and the segment is a code segment, the
        segment type is EXECUTEONLY. If this bit is set and the segment
        is a data segment, the segment type is READONLY.
    -   8: If this bit is set, the segment contains relocation data.
    -   9: Reserved.
    -   10: Reserved.
    -   11: Reserved.
    -   12: If this bit is set, the segment is discardable.
    -   13: Reserved.
    -   14: Reserved.
    -   15: Reserved.
-   06h: The minimum allocation size of the segment, in bytes. A value
    of zero indicates that the minimum allocation size is 64K.

[]{#Resource_Table} Resource Table
----------------------------------

The resource table describes and identifies the location of each
resource in the executable file.

Following are the members in the resource table:

-   rscAlignShift: The alignment shift count for resource data. When the
    shift count is used as an exponent of 2, the resulting value
    specifies the factor, in bytes, for computing the location of a
    resource in the executable file.
-   rscTypes: An array of TTYPEINFO structures containing information
    about resource types. There must be one TTYPEINFO structure for each
    type of resource in the executable file.
-   rscEndTypes: The end of the resource type definitions. This member
    must be zero.
-   rscResourceNames: The names (if any) associated with the resources
    in this table. Each name is stored as consecutive bytes; the first
    byte specifies the number of characters in the name.
-   rscEndNames: The end of the resource names and the end of the
    resource table. This member must be zero.

### []{#Type_Information} Type Information

Following are the members in the TTYPEINFO structure:

-   rtTypeID: The type identifier of the resource. This integer value is
    either a resource-type value or an offset to a resource-type name.
    If the high bit in this member is set (0x8000), the value is one of
    the following resource-type values:
    -   RT\_ACCELERATOR: Accelerator table
    -   RT\_BITMAP: Bitmap
    -   RT\_CURSOR: Cursor
    -   RT\_DIALOG: Dialog box
    -   RT\_FONT: Font component
    -   RT\_FONTDIR: Font directory
    -   RT\_GROUP\_CURSOR: Cursor directory
    -   RT\_GROUP\_ICON: Icon directory
    -   RT\_ICON: Icon
    -   RT\_MENU: Menu
    -   RT\_RCDATA: Resource data
    -   RT\_STRING: String table\
        If the high bit of the value in this member is not set, the
        value represents an offset, in bytes relative to the beginning
        of the resource table, to a name in the rscResourceNames member.
-   rtResourceCount: The number of resources of this type in the
    executable file.
-   rtReserved: Reserved.
-   rtNameInfo: An array of TNAMEINFO structures containing information
    about individual resources. The
-   rtResourceCount member specifies the number of structures in the
    array.

### []{#Name_Information} Name Information

Following are the members in the TNAMEINFO structure:

-   rnOffset: An offset to the contents of the resource data (relative
    to the beginning of the file). The offset is in terms of alignment
    units specified by the rscAlignShift member at the beginning of the
    resource table.
-   rnLength: The resource length, in bytes.
-   rnFlags: Whether the resource is fixed, preloaded, or shareable.
    This member can be one or more of the following values:
    -   0x0010: Resource is movable (MOVEABLE). Otherwise, it is fixed.
    -   0x0020: Resource can be shared (PURE).
    -   0x0040: Resource is preloaded (PRELOAD). Otherwise, it is loaded
        on demand.
-   rnID: Specifies or points to the resource identifier. If the
    identifier is an integer, the high bit is set (8000h). Otherwise, it
    is an offset to a resource string, relative to the beginning of the
    resource table.
-   rnHandle: Reserved.
-   rnUsage: Reserved.

[]{#Resident_Name_Table} Resident-Name Table
--------------------------------------------

The resident-name table contains strings that identify exported
functions in the executable file. As the name implies, these strings are
resident in system memory and are never discarded. The resident-name
strings are case-sensitive and are not null-terminated. The following
list summarizes the values found in the resident-name table (the
locations are relative to the beginning of each entry):

-   00h: The length of a string. If there are no more strings in the
    table, this value is zero.
-   01h - xxh: The resident-name text. This string is case-sensitive and
    is not null-terminated.
-   xxh + 01h: An ordinal number that identifies the string. This number
    is an index into the entry table.

The first string in the resident-name table is the module name.

[]{#Module_Reference_Table} Module-Reference Table
--------------------------------------------------

The module-reference table contains offsets for module names stored in
the imported-name table. Each entry in this table is 2 bytes long.

[]{#Imported_Name_Table} Imported-Name Table
--------------------------------------------

The imported-name table contains the names of modules that the
executable file imports. Each entry contains two parts: a single byte
that specifies the length of the string and the string itself. The
strings in this table are not null-terminated.

[]{#Entry_Table} Entry Table
----------------------------

The entry table contains bundles of entry points from the executable
file (the linker generates each bundle). The numbering system for these
ordinal values is 1-based\--that is, the ordinal value corresponding to
the first entry point is 1.

The linker generates the densest possible bundles under the restriction
that it cannot reorder the entry points. This restriction is necessary
because other executable files may refer to entry points within a given
bundle by their ordinal values.

The entry-table data is organized by bundle, each of which begins with a
2-byte header. The first byte of the header specifies the number of
entries in the bundle (a value of 00h designates the end of the table).
The second byte specifies whether the corresponding segment is movable
or fixed. If the value in this byte is 0FFh, the segment is movable. If
the value in this byte is 0FEh, the entry does not refer to a segment
but refers, instead, to a constant defined within the module. If the
value in this byte is neither 0FFh nor 0FEh, it is a segment index.

For movable segments, each entry consists of 6 bytes and has the
following form:

-   00h: Specifies a byte value. This value can be a combination of the
    following bits:
    -   0: If this bit is set, the entry is exported.
    -   1: If this bit is set, the segment uses a global (shared) data
        segment.
    -   3-7: If the executable file contains code that performs ring
        transitions, these bits specify the number of words that compose
        the stack. At the time of the ring transition, these words must
        be copied from one ring to the other.
-   01h: An int 3fh instruction.
-   03h: The segment number.
-   04h: The segment offset.

For fixed segments, each entry consists of 3 bytes and has the following
form:

-   00h: Specifies a byte value. This value can be a combination of the
    following bits:
    -   0: If this bit is set, the entry is exported.
    -   1: If this bit is set, the entry uses a global (shared) data
        segment. (This may be set only for SINGLEDATA library modules.)
    -   3-7: If the executable file contains code that performs ring
        transitions, these bits specify the number of words that compose
        the stack. At the time of the ring transition, these words must
        be copied from one ring to the other.
-   01h: Specifies an offset.

[]{#Nonresident_Name_Table} Nonresident-Name Table
--------------------------------------------------

The nonresident-name table contains strings that identify exported
functions in the executable file. As the name implies, these strings are
not always resident in system memory and are discardable. The
nonresident-name strings are case-sensitive; they are not
null-terminated. The following list summarizes the values found in the
nonresident-name table (the specified locations are relative to the
beginning of each entry):

-   00h: The length, in bytes, of a string. If this byte is 00h, there
    are no more strings in the table.
-   01h - xxh: The nonresident-name text. This string is case-sensitive
    and is not null-terminated.
-   xx + 01h: An ordinal number that is an index to the entry table.

The first name that appears in the nonresident-name table is the module
description string (which was specified in the module-definition file).

[]{#Code_Segments_and_Relocation_Dat} Code Segments and Relocation Data
-----------------------------------------------------------------------

Code and data segments follow the Windows header. Some of the code
segments may contain calls to functions in other segments and may,
therefore, require relocation data to resolve those references. This
relocation data is stored in a relocation table that appears immediately
after the code or data in the segment. The first 2 bytes in this table
specify the number of relocation items the table contains. A relocation
item is a collection of bytes specifying the following information:

-   Address type (segment only, offset only, segment and offset)
-   Relocation type (internal reference, imported ordinal, imported
    name)
-   Segment number or ordinal identifier (for internal references)
-   Reference-table index or function ordinal number (for imported
    ordinals)
-   Reference-table index or name-table offset (for imported names)

Each relocation item contains 8 bytes of data, the first byte of which
specifies one of the following relocation-address types:

-   0: Low byte at the specified offset
-   2: 16-bit selector
-   3: 32-bit pointer
-   5: 16-bit offset
-   11: 48-bit pointer
-   13: 32-bit offset

The second byte specifies one of the following relocation types:

-   0: Internal reference
-   1: Imported ordinal
-   2: Imported name
-   3: OSFIXUP

The third and fourth bytes specify the offset of the relocation item
within the segment.

If the relocation type is imported ordinal, the fifth and sixth bytes
specify an index to a module\'s reference table and the seventh and
eighth bytes specify a function ordinal value.

If the relocation type is imported name, the fifth and sixth bytes
specify an index to a module\'s reference table and the seventh and
eighth bytes specify an offset to an imported-name table.

If the relocation type is internal reference and the segment is fixed,
the fifth byte specifies the segment number, the sixth byte is zero, and
the seventh and eighth bytes specify an offset to the segment. If the
relocation type is internal reference and the segment is movable, the
fifth byte specifies 0FFh, the sixth byte is zero; and the seventh and
eighth bytes specify an ordinal value found in the segment\'s entry
table.

------------------------------------------------------------------------

Copyright © 1998 [Cristina Cifuentes](CristinaCifuentes){.twikiLink},
All Rights Reserved.\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
