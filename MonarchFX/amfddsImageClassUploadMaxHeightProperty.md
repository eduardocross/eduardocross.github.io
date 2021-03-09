---
title: DdsImage.UploadMaxHeight Property

Id: amfDdsImageClassUploadMaxHeightProperty
TocParent: amfDdsImageClassPropertiesMain
TocOrder: 60

keywords: UploadMaxHeight property
keywords: DdsImage.UploadMaxHeight property

---

Sets the maximum height (in pixels) that an uploaded image can take up.

#### Syntax
<pre class="prettyprint"> **BegProp UploadMaxHeight Access(*Public) Type(*int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the maximum height (in pixels) for all uploaded images. If left blank the image's original height will be preserved.

#### Remarks
This property works as a pair with [UploadMaxWidth](amfddsChartClassUploadMaxWidthProperty.html), when one of them is left blank, the other will be computed to preserve the original image's aspect ratio.
**Note &#8211;**  This property may not function properly on devices with Android versions Gingerbread or older.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsImage Description](amfUnderstandingImageControls.html)<br /> [ DdsImage Class](amfDdsImageClass.html) <br /> [ DdsImage Class Members](amfDdsImageClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
