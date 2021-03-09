---
title: DdsRecord.CursorLocation Property

Id: amfDdsRecordClassCursorLocationProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 55

keywords: CursorField property
keywords: DdsRecord.CursorField property
keywords: how to, set field name of cursor location
keywords: how to, get field name of cursor location
keywords: cursor location
keywords: cursor, location
keywords: cursors, location
keywords: web controls, setting field name of cursor location
keywords: web controls, getting field name of cursor location
keywords: subfiles, setting field name of cursor location
keywords: subfiles, getting field name of cursor location
keywords: subfile controls, setting field name of cursor location
keywords: subfile controls, getting field name of cursor location
keywords: subfile records, setting field name of cursor location
keywords: subfile records, getting field name of cursor location
keywords: records, setting field name of cursor location
keywords: records, getting field name of cursor location
keywords: display files, field name of cursor location

---

Gets or sets the location of the cursor

#### Syntax
<pre class="prettyprint"> **BegProp CursorLocation="'field-name-1,field-name-2':conditional-value"** </pre>

#### Property Values
field-name-1 &#8211; String. Name of the field whose contents is the virtual row where the cursor should be positioned.

field-name-2 &#8211;String. Name of the field whose contents is the virtual column where the cursor should be positioned. 

cconditional value &#8211; [Indicator conditional value](amfConditionalValueClass.html).

#### Remarks
To set the **CursorLocation** property at design-time, click on the far right side of the property and enter the names of the fields that contain the virtual row and column where the cursor should be positioned.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
