---
title: DdsSubfileControl.VerticalScrollBar Property

Id: amfDdsSubfileControlClassVerticalScrollBar 
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 300

keywords: VerticalScrollBar property
keywords: DdsSubfileControl.VerticalScrollBar property
keywords: subfiles, boolean expression controlling vertical scrollbar
keywords: web controls, boolean expression controlling vertical scrollbar
keywords: how to, set boolean expression to control vertical scrollbar
keywords: how to, get boolean expression controlling vertical scrollbar
keywords: subfile records, boolean expression controlling vertical scrollbar
keywords: subfile usage, boolean expression controlling vertical scrollbar

---

Sets whether a vertical scrollbar is shown to the right of the subfile. 

#### Syntax
<pre class="prettyprint"> **BegProp VerticalScrollBar Access(*Public) Type(*Bool)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. If **True** the subfile shows a vertical scrollbar to the right. This increases the effective width of the subfile by 19 pixels. 

#### Remarks
This property defaults to **true** on migration.

To set this property at design-time, right click **VerticalScrollBar** property and enter the conditional indicators. <br />

This property was added with Monarch Framework 6.1<br />

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
