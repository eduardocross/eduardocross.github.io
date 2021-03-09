---
title: DdsExpandingList.EndOfListText Property

Id: amfDdsExpandingListClassEndOfListTextProperty
TocParent: amfDdsExpandingListClassProperties
TocOrder: 47

keywords: EndOfListText property
keywords: DdsExpandingList.EndOfListText property

---

Sets the text to display on the "Get more records" button when all records have been added to the list. Defaults to <code>NO MORE RECORDS</code>.

#### Syntax
<pre class="prettyprint"><code class="language-avr"> **BegProp EndOfListText Access(*Public) Type(*String)
   BegGet;  BegSet** </code></pre>

#### Property Values
String. A string that defines the text which will be displayed on the button users press to add more records from the subfile to the list once all records have already been added.

#### Remarks
Only used once all records have been added and the button is grayed out.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10 Pro

#### See Also
[DdsExpandingList Description](amfUnderstandingLists.html)<br /> [ DdsExpandingList Class](amfDdsExpandingListClass.html) <br /> [ DdsExpandingList Class Members](amfDdsExpandingListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
