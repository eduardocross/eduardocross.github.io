---
title: DdsSubfile.VirtualRowsPerRecord Property

Id: amfDdsSubfileClassVirtualRowsPerRecord
TocParent: amfDdsSubfileClassPropertiesMain
TocOrder: 123

keywords: VirtualRowsPerRecord property
keywords: DdsSubfile.VirtualRowsPerRecord property
keywords: subfiles, vertical positioning
keywords: web controls, vertical subfile positioning
keywords: how to, postion subfiles
keywords: subfile records, setting vertical position
keywords: subfile vertical placement

---

Sets the vertical positions occupied by fields in a subfile record (as described by DDS).

#### Syntax
<pre class="prettyprint"> **BegProp VirtualRowsPerRecord Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. An integer value that sets the vertical positions occupied by fields in a subfile record (as described by the DDS.) 

#### Remarks
When not defined, this property is set to 1. During migration, values are computed from the subfile record fields found in the DDS.

To set this property at design-time, right click the **VirtualRowsPerRecord** property and enter a number value into the text box.

This property was added in Wings 5.2.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSubfile Class](amfDdsSubfileClass.html) <br /> [ DdsSubfile Class Members](amfDdsSubfileClassMembers.html) <br /> [ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
