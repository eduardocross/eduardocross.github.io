---
title: DdsSubfileControl.ShowRecordWithCursor Property

Id: amfDdsSubfileControlClassShowRecordWithCursorProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 130

keywords: ShowRecordWithCursor property
keywords: DdsSubfileControl.ShowRecordWithCursor property
keywords: how to, set first record cursor display position
keywords: how to, get first record cursor display position
keywords: subfiles, setting first record display position
keywords: subfiles, getting first record display position
keywords: subfile records, setting first record display position
keywords: subfile records, getting first record display position
keywords: subfile controls, setting first record display position
keywords: subfile controls, getting first record display position
keywords: web controls, first record display position
keywords: SFLRCDNBR CURSOR
keywords: CURSOR, SFLRCDNBR

---

Gets or sets a boolean value to indicate if the cursor is to be positioned in the record number, contained in the hidden field in the [ShowRecordField](amfDdsSubfileControlClassShowRecordFieldProperty.html) property. This is equivalent to the SFLRCDNBR keyword CURSOR.

#### Syntax
<pre class="prettyprint">
 **BegProp ShowRecordWithCursor Access(*Public) Type()
   BegGet;  BegSet** 
            </pre>

#### Property Values
Boolean. **True** , indicates the cursor is to be positioned in the record; otherwise, **False** .

#### Remarks
When this property is set **True** , the cursor is positioned at the first input-capable field in the record. If there is no input-capable field, this property is ignored.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ShowRecordField Property](amfDdsSubfileControlClassShowRecordFieldProperty.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
