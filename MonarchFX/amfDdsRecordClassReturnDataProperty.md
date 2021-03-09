---
title: DdsRecord.ReturnData Property

Id: amfDdsRecordClassReturnDataProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 90

keywords: ReturnData property
keywords: DdsRecord.ReturnData property
keywords: how to, return same input data
keywords: web controls, returning same input data
keywords: subfiles, returning same input data
keywords: subfile controls, returning same input data
keywords: subfile records, returning same input data
keywords: records, returning same input data
keywords: display files, returning same input data
keywords: RTNDATA

---

Gets or sets the boolean value specifying whether to return the same data that was returned on the previous input operation sent to this record format (RTNDATA). The default is **False** .

#### Syntax
<pre class="prettyprint"> **BegProp ReturnData Access(*Public) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. **True** to return the same data that was returned on the previous input operation sent to this record format; otherwise **False** .

#### Remarks
When this property is set **True** , if the record is read twice without an intervening write, the second read gets the same data without the user being prompted.

To set this property at design-time, click on the right of the **ReturnData** property and choose an option from the drop-down box. The default is **False** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
