---
title: DdsTable.Columns Property

Id: amfDdsTableClassColumnsProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: Columns property
keywords: DdsTable.Columns property
keywords: Web server controls [ASNA Monarch], ddsTable Columns
keywords: how to, set DdsTable Columns
keywords: how to, get DdsTable Columns
keywords: DdsTable Columns

---

Gets or sets the type for a collection of columns. Possible types include: BinaryColumn, CharColumn, PackedColumn, ZonedColumn and IconColumn.

#### Syntax
<pre class="prettyprint"> **BegProp Columns Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the type for a collection of columns. Acceptable values are: BinaryColumn, CharColumn, PackedColumn, ZonedColumn and IconColumn.

#### Remarks
To set this property at design time, click on the right side of
    the property window and enter a valid column type. Alternatively, use the [Column collection editor](amfUnderColumnList.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsTable Class](amfDdsTableClass.html)</dd>
        <dd>[DdsTable Class Members](amfDdsTableClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
       <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
</dl>

