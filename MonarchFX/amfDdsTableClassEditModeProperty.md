---
title: DdsTable.EditMode Property

Id: amfDdsTableClassEditModeProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: EditMode property
keywords: DdsTable.EditMode property
keywords: Web server controls [ASNA Monarch], setting DdsTable Edit Mode
keywords: how to, set DdsTable Edit Mode
keywords: how to, get DdsTable Edit Mode
keywords: MSGCON, file name

---

Sets whether to use inline editing or the cell-editing window for this DdsTable.

#### Syntax
<pre class="prettyprint"> **BegProp EditMode Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enum. A two option enumeration that determines how users interact with editable columns.

- **Modal&#8211;**  Utilizes the modal dialog editing capabilities.
- **Inline&#8211;**  Removes the modal dialog and allows the user to update data 
			within the selected cell.

#### Remarks
This property sets whether to use the (potentially more mobile-friendly) modal dialoge or (more green screen-familiar) inline editing.

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

