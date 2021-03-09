---
title: DdsPushButtonFieldChoice.VirtualRowCol Property

Id: amfDdsPushButtonFieldChoiceClassVirtualRowColProperty
TocParent: amfDdsPushButtonFieldChoiceClassPropertiesMain

keywords: VirtualRowCol property
keywords: DdsPushButtonFieldChoice.VirtualRowCol property
keywords: visibility, resetting hyperlink field
keywords: Hyperlink, display position
keywords: hyperlink fields, display position
keywords: hyperlink field display position
keywords: how to, set hyperlink display position
keywords: how to, get hyperlink display position
keywords: web controls, setting hyperlink display position
keywords: web controls, getting hyperlink display position
keywords: display files, setting hyperlink display position
keywords: display files, getting hyperlink display position

---

Gets or sets the row and column that this field is reported on in the Display file.

#### Syntax
<pre class="prettyprint"> **BegProp VirtualRowCol Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the row and column this field is reported on in the Display file; such as **7,27** .

#### Remarks
The row and column in the display file determines the order of HTML tags in the HTML document that is created.

To set this property at design-time, click on the right of the property and enter the row and column positions in the Display file.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsPushButtonFieldChoice Description](amfUnderstandingLinks.html)<br /> [DdsPushButtonFieldChoice Class](amfDdsPushButtonFieldChoiceClass.html) <br clear="none" /> [DdsPushButtonFieldChoice Class Members](amfDdsPushButtonFieldChoiceClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
