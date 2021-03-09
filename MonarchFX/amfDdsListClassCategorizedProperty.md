---
title: DdsList.Categorized Property

Id: amfDdsListClassCategorizedProperty
TocParent: amfDdsListClassProperties
TocOrder: 05

keywords: Categorized property
keywords: DdsList.Categorized property

---

Gets or sets whether or not the list is divided into Categories.

#### Syntax
<pre class="prettyprint"> **BegProp Categorized Access(*Public) Type(*boolean)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. If True the List will be divided into categories determined by the [CategoryField](amfDdsListClassCategoryFieldProperty.html) and [CategoryFieldLength](amfDdsListClassCategoryFieldLengthProperty.html) properties. If False those properties are ignored.

#### Remarks
This determines whether the list is divided into categories. Useful for all supported list types.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
