---
title: DdsHostFile.Path Property

Id: amfDdsHostFileClassPathProperty
TocParent: amfDdsHostFileClassPropertiesMain
TocOrder: 05

keywords: Path property
keywords: DdsHostFile.Path property

---

Gets or sets an absolute IFS path to the file to be presented by the HostFile Control.

#### Syntax
<pre class="prettyprint"> **BegProp Path Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the filepath for the file to be presented in the Web Display by the HostFile Control.

#### Remarks
As this product sets up an absolute path, this control is best used when the file to be presented on the page is unlikely to change at any forseeable point.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsHostFile Description](amfUnderstandingHostFiles.html)<br /> [ DdsHostFile Class](amfDdsHostFileClass.html) <br /> [ DdsHostFile Class Members](amfDdsHostFileClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
