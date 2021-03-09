---
title: DdsList.Directory Property

Id: amfDdsListClassImageDirectoryProperty
TocParent: amfDdsListClassPropertiesMain
TocOrder: 06

keywords: ImageDirectory property
keywords: DdsList.ImageDirectory property

---

Gets or sets an absolute path to the image file to be presented by the List Control.

#### Syntax
<pre class="prettyprint"> **BegProp ImageDirectory Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the filepath for the file to be presented in the Web Display by the List control.

#### Remarks
As this property sets up an absolute path, it is best used when the file to be presented on the page is unlikely to change at any foreseeable point. Overridden by [DirectoryField](amfDdsListClassImageDirectoryFieldProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
