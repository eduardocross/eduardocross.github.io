---
title: DdsImage.UploadedNameFieldLength Property

Id: amfDdsImageClassUploadedNameFieldLengthProperty
TocParent: amfDdsImageClassPropertiesMain
TocOrder: 46

keywords: UploadedNameFieldLength property
keywords: DdsImage.UploadedNameFieldLength property

---

Gets or sets the length of the CharField that holds the name of the file to be uploaded to the Image Control.

#### Syntax
<pre class="prettyprint"> **BegProp UploadedNameFieldLength Access(*Public) Type(*int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the length of the CharField that holds the name of the file to be uploaded to the Image Control.

#### Remarks
This sets the length of the CharField used by the [UploadedNameField](amfDdsImageClassUploadedNameFieldProperty.html). It must be used in conjuction with that property to avoid throwing an error.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsImage Description](amfUnderstandingImageControls.html)<br /> [ DdsImage Class](amfDdsImageClass.html) <br /> [ DdsImage Class Members](amfDdsImageClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
