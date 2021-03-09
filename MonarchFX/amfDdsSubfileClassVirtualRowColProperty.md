---
title: DdsSubfile.VirtualRowCol Property

Id: amfDdsSubfileClassVirtualRowColProperty
TocParent: amfDdsSubfileClassPropertiesMain
TocOrder: 121

keywords: VirtualRowCol property
keywords: DdsSubfile.VirtualRowCol property
keywords: subfiles, placement
keywords: web controls, using subfile positioning
keywords: how to, use subfile placement
keywords: subfile records, positioning
keywords: subfile placement

---

Gets or sets the upper-left corner of the Subfile screen area, as defined by DDS. 

#### Syntax
<pre class="prettyprint"> **BegProp VirtualRowCol Access(*Public) Type(*Col,Row)
   BegGet;  BegSet** </pre>

#### Property Values
Row, Column. This property sets the precise location of the upper-left hand corner of the Subfile screen area. 

#### Remarks
By default, this property takes it's value from the DDS during migration. If not defined in the DDS, it remains empty.

To set this property at design-time, right click the **VirtualRowCol** property and enter a row number and column number in the text box.

This property was added with Wings 5.2.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSubfile Class](amfDdsSubfileClass.html) <br /> [ DdsSubfile Class Members](amfDdsSubfileClassMembers.html) <br /> [ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
