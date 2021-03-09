---
title: DdsGmap.SelectedField Property

Id: amfDdsGMapClassSelectedFieldProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: SelectedField property
keywords: DdsGmap.SelectedField property

---

Sets whether a record or field is currently selected, allowing users to select multiple pins.

#### Syntax
<pre class="prettyprint"> **BegProp SelectedField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. This sets the name of the selected field within the DdsGMap. It can be set to establish an initial default.

#### Remarks
To set this property at design-time, click on the right hand side of the property window and enter the desired field name.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
