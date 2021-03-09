---
title: DdsFile.CursorRecord Property

Id: amfDdsFileClassCursorRecordProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 90

keywords: CursorRecord property
keywords: DdsFile.CursorRecord property
keywords: how to, get current cursor position record format name
keywords: record formats, name at current cursor position
keywords: cursor position, record format name
keywords: web controls, getting current cursor position record format name
keywords: display files, getting current cursor position record format name

---

Gets the name of the record format for the field at the current cursor position.

#### Syntax
<pre class="prettyprint"> **BegProp CursorRecord Access(*Public) Type(*String)
   BegGet;** </pre>

#### Property Value
String containing the record format for the field at the current cursor position.

#### Remarks
Use the [ CursorField](amfDdsFileClassCursorFieldProperty.html) property to get the field name at the cursor's current position and use the [ CursorLocation](amfDdsFileClassCursorLocationProperty.html) property to determine the cursor's position within the current field.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ CursorLocation Property](amfDdsFileClassCursorLocationProperty.html) <br clear="none" /> [CursorField Property](amfDdsFileClassCursorFieldProperty.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
