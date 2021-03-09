---
title: DdsButton.VirtualRowCol Property

Id: amfDdsButtonClassVirtualRowColProperty
TocParent: amfDdsButtonClassProperties
TocOrder: 90

keywords: VirtualRowCol property
keywords: DdsButton.VirtualRowCol property
keywords: Web server controls [ASNA.Monarch], dds button display position
keywords: how to, set dds button display position
keywords: how to, get dds button display position
keywords: display files, setting dds button display positiony
keywords: display files, getting dds button display position
keywords: web controls, setting dds button display position
keywords: web controls, getting dds button display position
keywords: dds button, display position
keywords: field controls, dds button, display position

---

Gets or sets the row and column that this field is reported on in the Display file.

#### Syntax
<pre class="syntax"> **BegProp VirtualRowCol Access(*Public) Type(*String)
   BegGet:  BegSet** </pre>

#### Property Values
String containing the row and column this field is reported on in the Display file, such as **7,27** .

#### Remarks
The row and column in the display file determines the order of HTML tags in the HTML document that is created.

To set this property at design-time, click on the right side of the property window and enter the row and column, comma separated.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsButton Description](amfUnderstandingButtons.html)<br /> [DdsButton Class](amfDdsButtonClass.html) <br /> [ DdsButton Class Members](amfDdsButtonClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
