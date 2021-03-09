---
title: DdsUploader.NameField Property

Id: amfDdsUploaderClassNameFieldProperty
TocParent: amfDdsUploaderClassPropertiesMain

keywords: NameField property
keywords: DdsUploader.NameField property

---

Sets a field that controls or contains the name of uploaded files. 

#### Syntax
<pre class="prettyprint"> **BegProp NameField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the path to the CharField for the name assoiated with the Uploaded file.

#### Remarks
This property sets a field that either assigns names to uploaded files (on output), or stores the names of uploaded files (on input). It requires [NameFieldLength](amdDdsUploaderClassNameFieldLengthProperty.html).

- **Output:**  Defines the name to be used for uploaded file.  Accepts wildcard '?' symbol to create unique names, i.e. UPLOAD??).
			Also accepts <code>*ORIGIN</code>, which keeps the original names.
- **Input:**  Reports the uploaded file's actual file name.  If there is no uploaded file, then it is set to blanks.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsUploader Description](amfUnderstandingUploaderControls.html)<br /> [ DdsUploader Class](amfDdsUploaderClass.html) <br /> [ DdsUploader Class Members](amfDdsUploaderClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
