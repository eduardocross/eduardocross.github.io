---
title: DdsExpandingList.MoreItemsText Property

Id: amfDdsExpandingListClassMoreItemsTextProperty
TocParent: amfDdsExpandingListClassProperties
TocOrder: 79

keywords: MoreItemsText property
keywords: DdsExpandingList.MoreItemsText property

---

Sets the text to display on the "Get more records" button. Defaults to <code>GET MORE RECORDS</code>.

#### Syntax
<pre class="prettyprint"><code class="language-avr"> **BegProp MoreItemsText Access(*Public) Type(*String)
   BegGet;  BegSet** </code></pre>

#### Property Values
String. A string that defines the text which will be displayed on the button users press to add more records from the subfile to the list.

#### Remarks
Used as long as there are still records in the subfile that haven't been added to the list. Once the final record is added, the value for [EndOfListText](amfDdsExpandingListClassEndOfListTextProperty.html) will be displayed instead.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10 Pro

#### See Also
[DdsExpandingList Description](amfUnderstandingLists.html)<br /> [ DdsExpandingList Class](amfDdsExpandingListClass.html) <br /> [ DdsExpandingList Class Members](amfDdsExpandingListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
