---
title: DdsHostFile.TextFieldLength Property

Id: amfDdsHostFileClassTextFieldLengthProperty
TocParent: amfDdsHostFileClassPropertiesMain
TocOrder: 30

keywords: TextFieldLength property
keywords: DdsHostFile.TextFieldLength property

---

Gets or sets an integer value that defines the length of the CharField from which the data to be displayed in a [Host File control](amfDdsHostFileClass.html) is drawn.

#### Syntax
<pre class="prettyprint"> **BegProp TextFieldLength Access(*Public) Type(*int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the length (in characters) of the CharField from which the text for the control will be drawn. 

#### Remarks
This sets the length of the IFS CharField to draw the text for the Host File control from. Required by [TextField](amfDdsHostFileClassTextFieldProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsHostFile Description](amfUnderstandingHostFiles.html)<br /> [ DdsHostFile Class](amfDdsHostFileClass.html) <br /> [ DdsHostFile Class Members](amfDdsHostFileClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
