---
title: DdsSubfileControl.ClickSetsCurrentRecord Property

Id: amfDdsSubfileControlClassClickSetsCurrentRecordProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 12

keywords: SubfileDrop property
keywords: DdsSubfileControl.SubfileDrop property
keywords: subfiles, conditional indicator expression controlling truncated display
keywords: web controls, conditional indicator expression controlling truncated display
keywords: how to, set conditional indicator expression to control truncated display
keywords: how to, get conditional indicator expression controlling truncated display
keywords: subfile records, conditional indicator expression controlling truncated display
keywords: subfile usage, conditional indicator expression controlling truncated display

---

Determines if the mouse click is handled to update the selection state. Note: If set to false and CueCurrentRecord is true, when changing rows using the keyboard TAB key, the "current record" CSS style will be applied.

#### Syntax
<pre class="prettyprint"> **BegProp ClickSetsCurrentRecord Access(*Public) Type(*Bool)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. If **true** a click event will select the current record, and the current record CSS style (.DdsSubfileCurrentRecord) will be applied to it. If **false** where CueCurrentRecord is **true** , the "current record" CSS style will be applied when changing rows using the TAB key, but not on a click.

#### Remarks
To set this property at design-time, right click the **ClickSetsCurrentRecord** property and select True or False from the dropdown box.

This property was added with Monarch Framework 6.1.<br />

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
