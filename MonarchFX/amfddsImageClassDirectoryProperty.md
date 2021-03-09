---
title: DdsImage.Directory Property

Id: amfDdsImageClassDirectoryProperty
TocParent: amfDdsImageClassPropertiesMain
TocOrder: 06

keywords: Directory property
keywords: DdsImage.Directory property

---

Gets or sets an absolute file path to the file to be presented by the Image Control.

#### Syntax
<pre class="prettyprint"> **BegProp Directory Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the filepath for the file to be presented in the Web Display by the Image Control.

#### Remarks
As this property sets up an absolute path, this property is best used when the file to be presented on the page is unlikely to change at any foreseeable point. Overridden by [DirectoryField](amfDdsImageClassDirectoryFieldProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsImage Description](amfUnderstandingImageControls.html)<br /> [ DdsImage Class](amfDdsImageClass.html) <br /> [ DdsImage Class Members](amfDdsImageClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
