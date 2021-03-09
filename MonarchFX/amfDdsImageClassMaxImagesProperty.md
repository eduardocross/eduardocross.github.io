---
title: DdsImage.MaxImages Property

Id: amfDdsImageClassMaxImagesProperty
TocParent: amfDdsImageClassPropertiesMain
TocOrder: 18

keywords: MaxImages property
keywords: DdsImage.MaxImages property

---

Gets or sets the maximum number of image files to send to the browser.

#### Syntax
<pre class="prettyprint"> **BegProp MaxImages Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. "0" is treated as a special value, indicating that all images that match the criteria set in [Name](amfDdsImageClassNameProperty.html) or [NameField](amfDdsImageClassNameFieldProperty.html) should be displayed.

#### Remarks
This property sets the maximum number of image files to send to the browser. This can be extremely useful for controlling the load times on pages by limiting the volume of (potentially very large) image files being sent over the connection.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsImage Description](amfUnderstandingImageControls.html)<br /> [ DdsImage Class](amfDdsImageClass.html) <br /> [ DdsImage Class Members](amfDdsImageClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
