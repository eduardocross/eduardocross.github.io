---
title: DdsHostFile.TextField Property

Id: amfDdsHostFileClassTextFieldProperty
TocParent: amfDdsHostFileClassPropertiesMain
TocOrder: 25

keywords: TextField property
keywords: DdsHostFile.TextField property

---

Defines the name of a record field used to report the text to be associated with a [Host File control](amfDdsHostFileClass.html).

#### Syntax
<pre class="prettyprint"> **BegProp TextField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of the record field that holds the text to be associated with a hosted file. Often used for captions or descriptions.

#### Remarks
This property is often best used when the text will appear on multiple web pages and/or is likely to be changed or updated frequently. By targeting a known field, it's possible to eliminate the need for a lot of upkeep. Requires [TextFieldLength](amfDdsHostFileClassTextFieldLengthProperty.html), and overrides [Text.](amfDdsHostFileClassTextProperty.html)

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsHostFile Description](amfUnderstandingHostFiles.html)<br /> [ DdsHostFile Class](amfDdsHostFileClass.html) <br /> [ DdsHostFile Class Members](amfDdsHostFileClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
