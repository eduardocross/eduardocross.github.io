---
title: DdsList.ImageDirectoryField Property

Id: amfDdsListClassImageDirectoryFieldProperty
TocParent: amfDdsListClassProperties
TocOrder: 55

keywords: ImageDirectoryField property
keywords: DdsList.ImageDirectoryField property

---

Gets or sets an IFS field to draw the data for the Image Directory from.

#### Syntax
<pre class="prettyprint"> **BegProp ImageDirectoryField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the IFS location of the IBM i CharField that the Image Directory data is drawn from. Requires [DdsList.ImageDirectoryFieldLength](amfDdsListClassImageDirectoryFieldLengthProperty.html).

#### Remarks
This sets a CharField in an IBM i record to draw the data for the Image Directory from. It must be used with [ImageDirectoryFieldLength](amfDdsListClassImageDirectoryFieldLengthProperty.html) in order to avoid throwing an error. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
