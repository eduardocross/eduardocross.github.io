---
title: DdsHostFile.PathField Property

Id: amfDdsHostFileClassPathFieldProperty
TocParent: amfDdsHostFileClassPropertiesMain
TocOrder: 10

keywords: Path property
keywords: DdsHostFile.PathField property

---

Defines the name of a record field used to report the path to files for a [HostFile control](amfDdsHostFileClass.html) to use.

#### Syntax
<pre class="prettyprint"> **BegProp PathField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of the record Field used to report the path to files for the Host File control. 

#### Remarks
This property is best used when the file to be used on the page may change periodically, but will always be in a consistent location, such as for newsletters, product documentation, or other items that are updated frequently. Requires [PathFieldLength](amfDdsHostFileClassPathFieldLengthProperty.html), and overrides [Path.](amfDdsHostFileClassPathProperty.html)

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsHostFile Description](amfUnderstandingHostFiles.html)<br /> [ DdsHostFile Class](amfDdsHostFileClass.html) <br /> [ DdsHostFile Class Members](amfDdsHostFileClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
