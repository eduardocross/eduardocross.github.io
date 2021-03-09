---
title: DdsFile.CursorField Property

Id: amfDdsFileClassCursorFieldProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 70

keywords: CursorField property
keywords: DdsFile.CursorField property
keywords: how to, get field name of current cursor position
keywords: cursor position, field name
keywords: web controls, getting field name of current cursor position
keywords: display files, setting field name of current cursor position

---

Gets the name of the field within the record format at the current cursor position.

#### Syntax
<pre class="prettyprint"> **BegProp CursorField Access(*Public) Type(*String)
   BegGet;** </pre>

#### Property Value
String containing the field name at the current cursor position.

#### Remarks
Use the [ CursorRecord](amfDdsFileClassCursorRecordProperty.html) property to get the name of the record format for the field at the cursor's location, and use the [ CursorLocation](amfDdsFileClassCursorLocationProperty.html) property to determine the cursor's position within the current field.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ CursorLocation Property](amfDdsFileClassCursorLocationProperty.html) <br clear="none" /> [CursorRecord Property](amfDdsFileClassCursorRecordProperty.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
