---
title: DdsFile.CursorLocation Property

Id: amfDdsFileClassCursorLocationProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 80

keywords: CursorLocation property
keywords: DdsFile.CursorLocation property
keywords: how to, get cursor position in field
keywords: cursor position, in field
keywords: web controls, getting cursor position in field
keywords: display files, getting cursor position in field

---

Gets the position of the cursor within the current field.

#### Syntax
<pre class="prettyprint"> **BegProp CursorLocation Access(*Public) Type(*Integer)
   BegGet;** </pre>

#### Property Value
Integer containing the current cursor position within the field.

#### Remarks
Use the [ CursorRecord](amfDdsFileClassCursorRecordProperty.html) property to get the name of the record format for the field at the cursor's location, and use the [ CursorField](amfDdsFileClassCursorFieldProperty.html) property to return the field name at the cursor's current position.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [CursorField Property](amfDdsFileClassCursorFieldProperty.html) <br clear="none" /> [CursorRecord Property](amfDdsFileClassCursorRecordProperty.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
