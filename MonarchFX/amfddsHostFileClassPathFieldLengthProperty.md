---
title: DdsHostFile.PathFieldLength Property

Id: amfDdsHostFileClassPathFieldLengthProperty
TocParent: amfDdsHostFileClassPropertiesMain
TocOrder: 15

keywords: PathFieldLength property
keywords: DdsHostFile.PathFieldLength property

---

Gets or sets an integer value that defines length of the PathField from which the data to be displayed in a [Host File Control](amfDdsHostFileClass.html) is drawn.

#### Syntax
<pre class="prettyprint"> **BegProp PathFieldLength Access(*Public) Type(*int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the length in characters of the Path Field from which the IFS location of the Host File will be drawn. 

#### Remarks
This sets the length of the path field, and is required by [PathField](amdDdsHostFileClassPathFieldProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsHostFile Description](amfUnderstandingHostFiles.html)<br /> [ DdsHostFile Class](amfDdsHostFileClass.html) <br /> [ DdsHostFile Class Members](amfDdsHostFileClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
