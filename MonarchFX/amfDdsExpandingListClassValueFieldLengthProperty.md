---
title: DdsExpandingList.ValueFieldLength Property

Id: amfDdsExpandingListClassValueFieldLengthProperty
TocParent: amfDdsExpandingListClassProperties
TocOrder: 120

keywords: ValueFieldLength property
keywords: DdsExpandingList.ValueFieldLength property

---

Gets or sets the length (in characters) of the field the Value data will be drawn from.

#### Syntax
<pre class="prettyprint"> **BegProp ValueFieldLength Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the length of the Record field from which the data for the value will be drawn. Requires [ValueField](amfDdsExpandingListClassValueFieldProperty.html).

#### Remarks
Sets the length of the field the data for the value will be drawn from. Must be used with [ValueField](amfDdsExpandingListClassValueFieldProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsExpandingList Description](amfUnderstandingLists.html)<br /> [ DdsExpandingList Class](amfDdsExpandingListClass.html) <br /> [ DdsExpandingList Class Members](amfDdsExpandingListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
