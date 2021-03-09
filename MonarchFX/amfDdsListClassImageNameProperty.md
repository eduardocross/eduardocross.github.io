---
title: DdsList.ImageNameField Property

Id: amfDdsListClassImageNameFieldProperty
TocParent: amfDdsListClassProperties
TocOrder: 70

keywords: ImageNameField property
keywords: DdsList.ImageNameField property

---

Contains the name of the Image to display.

#### Syntax
<pre class="prettyprint"> **BegProp ImageName Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Contains the name of the Image to display.

#### Remarks
This a hardcoded name for an image to be displayed. Since it establishes a fixed name and filepath, this property should only be employed when its value is unlikely to be changed. Overriden by [ImageNameField](amfddslistClassImageNameFieldProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
