---
title: DdsList.ListType Property

Id: amfDdsListClassListTypeProperty
TocParent: amfDdsListClassProperties
TocOrder: 78

keywords: ListType property
keywords: DdsList.ListType property

---

Gets or sets the type of list items to display.

#### Syntax
<pre class="prettyprint"> **BegProp ListType Access(*Public) Type(*Enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Options include:

- Checkbox  &#8211; 
	   	Presents a list featuring check boxes
- Dropdown  &#8211;
	   	Presents a dropdown list (ignores Image, Chevron, and detail)
- Listbox  &#8211;
	   	Presents a simple Listbox
- Radio  &#8211;
	   	Presents a list with each item including a radio button option.
- Navigation  &#8211;
	   	Presents a navigation list, featuring Chevrons

#### Remarks
Sets the overall appearance and contents of the list.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
