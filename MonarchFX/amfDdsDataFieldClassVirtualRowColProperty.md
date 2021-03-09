---
title: DdsDataField.VirtualRowCol Property

Id: amfDdsDataFieldClassVirtualRowColProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 150

keywords: VirtualRowCol property
keywords: DdsDataField.VirtualRowCol property
keywords: Web server controls [ASNA.Monarch], field display position
keywords: how to, set field control display position
keywords: how to, get field control display position
keywords: display files, setting field control display position
keywords: display files, getting field control display position
keywords: web controls, setting field control display position
keywords: web controls, getting field control display position
keywords: field controls, display position

---

Gets or sets the row and column that this field is reported on in the Display file.

#### Syntax
<pre class="prettyprint"> **BegProp VirtualRowCol Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

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
[ DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
