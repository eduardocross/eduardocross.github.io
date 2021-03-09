---
title: DdsImage.ViewType Property

Id: amfDdsImageClassViewTypeProperty
TocParent: amfDdsImageClassPropertiesMain
TocOrder: 80

keywords: ViewType property
keywords: DdsImage.ViewType property

---

Sets how the stored images will be displayed. Defaults to <code>DisplayAll</code>.

#### Syntax
<pre class="prettyprint"> **BegProp ViewStyle Access(*Public) Type(*Enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enum. Possible values include:

- **<code>DisplayAll</code>**  &#8212; Default.  Displays all images in a standard image gallery (best for PC browsers).
- <code>None</code> &#8212; No images will be displayed, although buttons allowing users to upload images will still be visible if Upload is enabled.
- <code>SwipeShow</code> &#8212; Images will be displayed in a mobile-phone-friendly swipe gallery.

#### Remarks
This property sets the presentation of the DdsImage control.

This property was added with version 8.0.
**Note &#8212;**  This property may not function properly on devices with Android versions Gingerbread or older.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsImage Description](amfUnderstandingImageControls.html)<br /> [ DdsImage Class](amfDdsImageClass.html) <br /> [ DdsImage Class Members](amfDdsImageClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
