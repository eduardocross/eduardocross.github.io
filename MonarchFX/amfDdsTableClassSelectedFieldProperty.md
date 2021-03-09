---
title: DdsTable.SelectedField Property

Id: amfDdsTableClassSelectedFieldProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: SelectedField property
keywords: DdsTable.SelectedField property
keywords: Web server controls [ASNA Monarch], setting DdsTable SelectedField
keywords: how to, set DdsTable SelectedField
keywords: how to, get DdsTable SelectedField

---

Gets or sets a string containing the Name of the field which will be set to 1 when the record is selected and 0 when not selected.

#### Syntax
<pre class="prettyprint"> **BegProp SelectedField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the Name of the field which will be set to 1 when the record is selected and 0 when not selected.

#### Remarks
This property is used in conjunction with [SelectRowKey](amfDdsTableClassSelectRowKeyProperty.html) to fire an event (such as opening a new display file) when a row is selected.

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

