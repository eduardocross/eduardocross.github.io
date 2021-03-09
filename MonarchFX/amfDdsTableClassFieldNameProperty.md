---
title: DdsTable.FieldName Property

Id: amfDdsTableClassFieldNameProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: FieldName property
keywords: DdsTable.FieldName property
keywords: Web server controls [ASNA Monarch], setting DdsTable FieldName
keywords: how to, set DdsTableFieldName
keywords: how to, get DdsTableFieldName+

---

Gets or sets a string containing the name of a data field used by the DdsTable

#### Syntax
<pre class="prettyprint"> **BegProp FieldName Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the Name of a field the DdsTable draws data from, often set automatically based on the [Subfile Name](amfDdsTableClassSubfileNameProperty.html).

#### Remarks
Works in concert with [FieldLength](amfDdsTableClassFieldLengthProperty.html) to define an RPG field.

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

