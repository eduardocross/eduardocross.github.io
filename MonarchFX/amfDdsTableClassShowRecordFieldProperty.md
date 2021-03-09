---
title: DdsTable.ShowRecordField Property

Id: amfDdsTableClassShowRecordFieldProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: ShowRecordField property
keywords: DdsTable.ShowRecordField property
keywords: Web server controls [ASNA Monarch], DdsTable ShowRecordField
keywords: how to, set DdsTable ShowRecordField
keywords: how to, get DdsTable ShowRecordField
keywords:  DdsTable ShowRecordField

---

Defines a decimal field which tracks the RRN of the selected record.

#### Syntax
<pre class="prettyprint"> **BegProp ShowRecordField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Defines a decimal (4, 0) field which will track the RRN of the record selected for navigation purposes. 

#### Remarks
This field can be updated to identify which row to scroll to when navigating back to a table. This property only applies if a height is set for the table (via the height or [VerticalMargin](amfDdsTableClassVerticalMarginProperty.html) properties).

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

