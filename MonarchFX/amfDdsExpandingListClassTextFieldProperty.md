---
title: DdsExpandingList.TextField Property

Id: amfDdsExpandingListClassTextFieldProperty
TocParent: amfDdsExpandingListClassProperties
TocOrder: 115

keywords: TextField property
keywords: DdsExpandingList.TextField property

---

Gets or sets an IFS field to draw the data for the Text attribute from.

#### Syntax
<pre class="prettyprint"> **BegProp TextField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the IFS location of the IBM i CharField that the Text data is drawn from. Requires [DdsExpandingList.TextFieldLength](amfDdsExpandingListClassTextFieldLengthProperty.html).

#### Remarks
This sets a CharField in an IBM i record to draw the data for the Text attribute from. It must be used with [TextFieldLength](amfDdsExpandingListClassTextFieldLengthProperty.html) in order to avoid throwing an error. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsExpandingList Description](amfUnderstandingLists.html)<br /> [ DdsExpandingList Class](amfDdsExpandingListClass.html) <br /> [ DdsExpandingList Class Members](amfDdsExpandingListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
