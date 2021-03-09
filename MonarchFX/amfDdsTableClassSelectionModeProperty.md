---
title: DdsTable.SelectionMode Property

Id: amfDdsTableClassSelectionModeProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: SelectionMode property
keywords: DdsTable.SelectedField property
keywords: Web server controls [ASNA Monarch], setting DdsTable SelectionMode
keywords: how to, set DdsTable SelectionMode
keywords: how to, get DdsTable SelectionMode

---

Gets or sets whether users can select multiple cells, or only one cell at a time.

#### Syntax
<pre class="prettyprint"> **BegProp SelectionMode Access(*Public) Type(*Enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enum. This determines whether single or multiple cells can be selected by the user.

#### Remarks
This property determines whether users can select multiple cells or only single cells.

**Caution** &#8211; this property does not interact with the <code>Usage</code> property of the individual cells so editing may be enabled for multiple cells simultaneously. Implementation of simultaneous editing scenarios is the responsibility of the developer. 

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

