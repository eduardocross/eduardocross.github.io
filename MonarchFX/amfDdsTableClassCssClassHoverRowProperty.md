---
title: DdsTable.CssClassHoverRow Property

Id: amfDdsTableClassCssClassHoverRowProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: CssClassHoverRow property
keywords: DdsTable.CssClassHoverRow property
keywords: Web server controls [ASNA Monarch], setting DdsTable Class Hover Row
keywords: how to, set DdsTable Class Hover Row
keywords: how to, get DdsTable Class Hover Row

---

Gets or sets a string containing the name of the CssClass to apply to the row currently being hovered over.

#### Syntax
<pre class="prettyprint"> **BegProp CssClassHoverRow Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the name of the CssClass to apply to the row that the mouse pointer is hovering over.

#### Remarks
The CssClass to apply to the row where the mouse pointer is curently hovering. Does not apply in touch formats, as there is no pointer. Defaults to HoverRow.

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

