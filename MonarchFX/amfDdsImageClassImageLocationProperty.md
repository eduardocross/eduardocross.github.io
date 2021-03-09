---
title: DdsImage.ImageLocation Property

Id: amfDdsImageClassImageLocationProperty
TocParent: amfDdsImageClassPropertiesMain
TocOrder: 14

keywords: ImageLocation property
keywords: DdsImage.ImageLocation property

---

Gets or sets the location of the Image file to be displayed.

#### Syntax
<pre class="prettyprint"> **BegProp ImageLocation Access(*Public) Type(*Enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Possible values include:

- **HostIFS**  (Default) &#8212;
	   		The image file is located in the IFS.
- **ThisWebSite**  &#8212; The image file is located on the Windows Server 
			file system of the IIS server for the Website.
- **ExternalSource**  &#8212; 
			The image file is located at a different URL.

#### Remarks
This property sets the general location that the Image file will be drawn from. The default, HostIFS, is used when the image is in the IFS. ThisWebsite allows the control to present an image or images located on the Windows Server. Lastly, ExternalSource presents an image from a specific URL. In this case the [Name](amfDdsImageClassNameProperty.html) property cannot have wildcards, and upload functionality is unavailable. 

Note &#8211; Monarch apps may not use the HostIFS value.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsImage Description](amfUnderstandingImageControls.html)<br /> [ DdsImage Class](amfDdsImageClass.html) <br /> [ DdsImage Class Members](amfDdsImageClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
