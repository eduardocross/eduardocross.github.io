---
title: DdsList.NavigableField Property

Id: amfDdsListClassNavigableFieldProperty
TocParent: amfDdsListClassProperties
TocOrder: 80

keywords: NavigableField property
keywords: DdsList.NavigableField property

---

Gets or sets a field name or indicator number that determines whether a field or set of fields is navigable.

#### Syntax
<pre class="prettyprint"> **BegProp NavigableField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the field name or indicator that controls whether the item is navigable at all. The special value ***TRUE** is used to indicate that all items should be navigable.

#### Remarks
Defines a field, and sets it to a value. 

For example 'DRILL' indicates the request to define a field called 'DRILL'. The program or developer can then set the value of the field 'DRILL' to '1' before adding a record to the subfile, indicating that the user will be able to tap on that record. Setting 'DRILL' to '0' before adding the subfile record would prevent the user from tapping on it. 

Any items don't match the value or have the indicator will appear "grayed out" and won't be selectable.

If all the list items are going to be navigable, do not specify this property at all, or set it to the special value '*TRUE'.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
