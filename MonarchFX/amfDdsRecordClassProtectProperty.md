---
title: DdsRecord.Protect Property

Id: amfDdsRecordClassProtectProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 87

keywords: Protect property
keywords: DdsRecord.Protect property
keywords: how to, return same input data
keywords: web controls, returning same input data
keywords: subfiles, returning same input data
keywords: subfile controls, returning same input data
keywords: subfile records, returning same input data
keywords: records, returning same input data
keywords: display files, returning same input data
keywords: RTNDATA

---

Gets or sets an indicator expression (or *True) which determines whether the fields in this record are protected.

#### Syntax
<pre class="prettyprint"> **BegProp Protect Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Accepts either an indicator expression or special value (*True).

#### Remarks
When this property is set ***True** , all input-capable fields in the record will become read-only (protected). New fields that are added may not be protected unless this property is reinvoked.

To set this property at design-time, click on the right of the **Protect** property and choose an option from the drop-down box.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
