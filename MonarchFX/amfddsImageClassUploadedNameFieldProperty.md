---
title: DdsImage.UploadedNameField Property

Id: amfDdsImageClassUploadedNameFieldProperty
TocParent: amfDdsImageClassPropertiesMain
TocOrder: 45

keywords: UploadedNameField property
keywords: DdsImage.UploadedNameField property

---

Identifies the name of a record field used to define the [Name](amfDdsImageClassNameProperty.html) to be given to the uploaded image file.

#### Syntax
<pre class="prettyprint"> **BegProp UploadedNameField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the character field whose value will hold the [Name](amfDdsImageClassNameProperty.html) to be given to the file or files uploaded by the Image Control. 

#### Remarks
This property sets the name of a character field whose value at runtime will set the name of the file to be uploaded. The value of this field is set via the [Name property](amfDdsImageClassNameProperty.html).

Both this property and [UploadedNameFieldLength](amfDdsImageClassUploadedNameFieldLengthProperty.html) are required for the Image Control's upload function.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsImage Description](amfUnderstandingImageControls.html)<br /> [ DdsImage Class](amfDdsImageClass.html) <br /> [ DdsImage Class Members](amfDdsImageClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
