---
title: DdsSubfileControl.ShowRecordField Property

Id: amfDdsSubfileControlClassShowRecordFieldProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 120

keywords: ShowRecordField property
keywords: DdsSubfileControl.ShowRecordField property
keywords: how to, set first record to display
keywords: how to, get first record to display
keywords: subfiles, setting first record to display
keywords: subfiles, getting first record to display
keywords: subfile records, setting first record to display
keywords: subfile records, getting first record to display
keywords: subfile controls, setting first record to display
keywords: subfile controls, getting first record to display
keywords: web controls, first record to display
keywords: SFLRCDNBR

---

Gets or sets the name of a hidden field containing the record number of the subfile record whose page is to be displayed. (SFLRCDNBR).

#### Syntax
<pre class="prettyprint"> **BegProp ShowRecordField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. The name of the hidden field containing the record number of the subfile record whose page is to be displayed.

#### Remarks
The hidden field must be of type decimal and contain a valid record number. The **ShowRecordField** property is used in conjunction with the [ ShowRecordAtTop](amfDdsSubfileControlClassShowRecordAtTopProperty.html) and [ ShowRecordWithCursor](amfDdsSubfileControlClassShowRecordWithCursorProperty.html) properties to support the SFLRCDNBR keywords CURSOR and *TOP.

When the **ShowRecordWithCursor** property is **true** , the cursor is placed in the record indicated by the **ShowRecordField** property. The cursor is positioned at the first input-capable field in the record. If there are no input-capable fields, the **ShowRecordField** property is ignored.

When the **ShowRecordAtTop** property is **true** (*TOP), the record, indicated by the **ShowRecordField** property, is displayed as the first record on the page.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ShowRecordAtTop Property](amfDdsSubfileControlClassShowRecordAtTopProperty.html) <br />[ ShowRecordWithCursor Property](amfDdsSubfileControlClassShowRecordWithCursorProperty.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
