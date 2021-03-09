---
title: DdsTable.FieldLength Property

Id: amfDdsTableClassFieldLengthProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: FieldLength property
keywords: DdsTable.FieldLength property
keywords: Web server controls [ASNA Monarch], setting DdsTable FieldLength
keywords: how to, set DdsTable FieldLength
keywords: how to, get DdsTable FieldLength
keywords: DdsTable Field Length

---

Gets or sets an integer containing the length (in characters) of a data field used by the DdsTable.

#### Syntax
<pre class="prettyprint"> **BegProp FieldLength Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Int. An integer containing the length of a field the DdsTable draws data from, often set automatically based on the [Subfile Name](amfDdsTableClassSubfileNameProperty.html).

#### Remarks
Works in concert with [FieldName](amfDdsTableClassFieldNameProperty.html) to define an RPG field.

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

