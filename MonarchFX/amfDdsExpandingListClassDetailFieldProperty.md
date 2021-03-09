---
title: DdsExpandingList.DetailField Property

Id: amfDdsExpandingListClassDetailFieldProperty
TocParent: amfDdsExpandingListClassProperties
TocOrder: 45

keywords: DetailField property
keywords: DdsExpandingList.DetailField property

---

Gets or sets an IFS field to draw the data for the Detail from.

#### Syntax
<pre class="prettyprint"> **BegProp DetailField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the IFS location of the IBM i CharField that the Detail data is drawn from. Requires [DdsExpandingList.DetailFieldLength](amfDdsExpandingListClassDetailFieldLengthProperty.html).

#### Remarks
This sets a CharField in an IBM i record to draw the data for the Detail from. It must be used with [DetailFieldLength](amfDdsExpandingListClassDetailFieldLengthProperty.html) in order to avoid throwing an error. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsExpandingList Description](amfUnderstandingLists.html)<br /> [ DdsExpandingList Class](amfDdsExpandingListClass.html) <br /> [ DdsExpandingList Class Members](amfDdsExpandingListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
