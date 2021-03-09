---
title: DdsTable.SelectedRowValue Property

Id: amfDdsTableClassSelectedRowValueProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: SelectedRowValue property
keywords: DdsTable.SelectedRowValue property
keywords: Web server controls [ASNA Monarch], setting DdsTable SelectedRowValue
keywords: how to, set DdsTable SelectedRowValue
keywords: how to, get DdsTable SelectedRowValue

---

Gets or sets a value that will be passed to the RPG program in the <code>SelectedField</code> to indicate that a specific row (as opposed to the column) is selected.

#### Syntax
<pre class="prettyprint"> **BegProp SelectedRowValue Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string which identifies the row selected.

#### Remarks
This property is used in conjunction with [SelectedField](amfDdsTableClassSelectedFieldProperty.html) and [SelectRowKey](amfDdsTableClassSelectRowKeyProperty.html) to fire an event (such as opening a new display file) when a row is selected.

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

