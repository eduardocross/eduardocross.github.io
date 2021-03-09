---
title: DdsList.CategoryField Property

Id: amfDdsListClassCategoryFieldProperty
TocParent: amfDdsListClassProperties
TocOrder: 09

keywords: CategoryField property
keywords: DdsList.CategoryField property

---

Defines the name of a record field used to report the data for the Category.

#### Syntax
<pre class="prettyprint"> **BegProp CategoryField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of a record field used to record the category data. Requires [DdsList.CategoryFieldLength](amfDdsListClassCategoryFieldLengthProperty.html).

#### Remarks
This sets a CharField in a record to draw the data for the Category from. It must be used with [CategoryFieldLength](amfDdsListClassCategoryFieldLengthProperty.html) in order to avoid throwing an error. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
