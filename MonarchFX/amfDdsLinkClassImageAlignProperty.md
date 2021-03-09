---
title: DdsLink.ImageAlign Property

Id: amfDdsLinkClassImageAlignProperty
TocParent: amfDdsLinkClassPropertiesMain
TocOrder: 43

keywords: ImageAlign property
keywords: DdsLink.ImageAlign property

---

Gets or sets the alignment of the [Image](amfDdsLinkClassImageProperty.html) that represents the link if [LinkStyle](amfDdsLinkClassLinkStyleProperty.html) is set to Image. Otherwise, ignored.

#### Syntax
<pre class="prettyprint"> **BegProp Image Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Options include Left, Right, and Center.

#### Remarks
This property sets the alignment of the image used to represent the DdsLink on the screen. Only used if [LinkStyle](amfDdsLinkClassLinkStyleProperty.html) is set to Image.

This property was added to support Wings 6.1 and Mobile RPG 6.1.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsLink Description](amfUnderstandingLinks.html)<br /> [ DdsLink Class](amfDdsLinkClass.html) <br /> [ DdsLink Class Members](amfDdsLinkClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
