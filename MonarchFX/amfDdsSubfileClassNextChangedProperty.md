---
title: DdsSubfile.NextChanged Property

Id: amfDdsSubfileClassNextChangedProperty
TocParent: amfDdsSubfileClassPropertiesMain
TocOrder: 50

keywords: NextChanged property
keywords: DdsSubfile.NextChanged property
keywords: READC
keywords: SFLNXTCHG
keywords: subfiles, indicating record changed
keywords: subfiles, determining changed records
keywords: web controls, determining changed records
keywords: how to, indicate record has changed
keywords: how to, set record as changed
keywords: how to, determine if record as changed
keywords: subfile records, setting as changed
keywords: subfile records, checking if changed
keywords: subfile usage, checking record changed

---

Gets or sets a string containing *False or *True indicating if the record has changed and whether READC will read the record. (SFLNXTCHG)

#### Syntax
<pre class="prettyprint"> **BegProp NextChanged Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. ***False** sets the record as not changed and READC will not read this record; ***True** sets the record as changed guaranteeing that READC will read this record.

#### Remarks
To set this property at design-time, click on the right of the **NextChanged** property and enter * **False** or ***True** . The default is ***False** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSubfile Class](amfDdsSubfileClass.html) <br /> [ DdsSubfile Class Members](amfDdsSubfileClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
