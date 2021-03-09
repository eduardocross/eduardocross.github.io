---
title: DdsUploader.DirectoryField Property

Id: amfDdsUploaderClassDirectoryFieldProperty
TocParent: amfDdsUploaderClassPropertiesMain

keywords: Directory property
keywords: DdsUploader.DirectoryField property

---

Defines the name of a record field used to report the file to be displayed in a [DdsUploader control](amfDdsUploaderClass.html).

#### Syntax
<pre class="prettyprint"> **BegProp DirectoryField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Defines the name of a record field used to report the file to be shown by the DdsUploader control. 

#### Remarks
This property is best used when the file to be used on the page may change periodically, but will always be in a consistent location, such as for newsletters, product documentation, or other items that are updated frequently. Requires the use of [DirectoryFieldLength](amdDdsUploaderClassDirectoryFieldProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsUploader Description](amfUnderstandingUploaderControls.html)<br /> [ DdsUploader Class](amfDdsUploaderClass.html) <br /> [ DdsUploader Class Members](amfDdsUploaderClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
