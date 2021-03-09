---
title: DdsSubfile.VirtualWidth Property

Id: amfDdsSubfileClassVirtualWidthProperty
TocParent: amfDdsSubfileClassPropertiesMain
TocOrder: 122

keywords: VirtualWidth property
keywords: DdsSubfile.VirtualWidth property
keywords: subfiles, horizontal position
keywords: web controls, horizontal subfile placement
keywords: how to, set subfile's horizontal placement
keywords: subfile records, horizontal placement
keywords: subfile positioning

---

Sets the horizontal positions occupied by fields in a subfile record (as described by the DDS).

#### Syntax
<pre class="prettyprint"> **BegProp VirtualWidth Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. An integer value that sets the horizontal positions occupied by fields in a subfile record (as described by the DDS). 

#### Remarks
When not defined, this property is set to 0. During migration, values are computed from the subfile record fields found in the DDS.

To set this property at design-time, right click the **VirtualWidth** property and enter an integer value into the text box.

This property was added with Monarch and Wings 5.2.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSubfile Class](amfDdsSubfileClass.html) <br /> [ DdsSubfile Class Members](amfDdsSubfileClassMembers.html) <br /> [ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
