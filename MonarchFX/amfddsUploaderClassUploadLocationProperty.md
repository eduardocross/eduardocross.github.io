---
title: DdsImage.UploadLocation Property

Id: amfDdsImageClassUploadLocationProperty
TocParent: amfDdsImageClassPropertiesMain

keywords: CssClassUploadLocation property
keywords: DdsUploader.UploadLocation property

---

Sets whether the upload will be from the website or the IFS.

#### Syntax
<pre class="prettyprint"> **BegProp UploadLocation Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Valus include: 

- ThisWebSite
- HostIFS (Default)

#### Remarks
This property sets whether ths file to be uploaded is in the HostIFS (default), or the Website.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsUploader Description](amfUnderstandingUploaderControls.html)<br /> [ DdsUploader Class](amfDdsUploaderClass.html) <br /> [ DdsUploader Class Members](amfDdsUploaderClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
