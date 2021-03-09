---
title: DdsImage.UploadMaxWidth Property

Id: amfDdsImageClassUploadMaxWidthProperty
TocParent: amfDdsImageClassPropertiesMain
TocOrder: 65

keywords: UploadMaxWidth property
keywords: DdsImage.UploadMaxWidth property

---

Sets the maxium width (in pixels) that an uploaded image can take up.

#### Syntax
<pre class="prettyprint"> **BegProp UploadMaxWidth Access(*Public) Type(*int)
   BegGet;  BegSet** </pre>

#### Property Values
Int. Sets the maximum width (in pixels) for all uploaded images. If left blank the image's original width will be preserved.

#### Remarks
This property works as a pair with [UploadMaxHeight](amfddsChartClassUploadMaxHeightProperty.html), when one of them is left blank, the other will be computed to preserve the original image's aspect ratio.
**Note &#8212;**  This property may not function properly on devices with Android versions Gingerbread or older.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsImage Description](amfUnderstandingImageControls.html)<br /> [ DdsImage Class](amfDdsImageClass.html) <br /> [ DdsImage Class Members](amfDdsImageClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
