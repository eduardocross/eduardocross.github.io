---
title: DdsTimeField.TimeSeparator Property

Id: amfDdsTimeFieldClassTimeSeparatorProperty
TocParent: amfDdsTimeFieldClassProperties
TocOrder: 220

keywords: TimeSeparator property
keywords: DdsTimeField.TimeSeparator property
keywords: Web server controls [ASNA Monarch], time field separator
keywords: how to, set time field control field separator
keywords: how to, get time field control field separator
keywords: display files, setting time field control field separator
keywords: display files, getting time field control field separator
keywords: web controls, setting time field control field separator
keywords: web controls, getting time field control field separator
keywords: field controls, time field, subfield separator

---

Gets or sets a value identifying the character to be used to separate the components of the time field for format **HMS** only. 

#### Syntax
<pre class="prettyprint"> **BegProp TimeSeparator Access(*Public) Type(*String)
     BegGet;  BegSet** </pre>

#### Property Values
A string value to use as the time field separator.

#### Remarks
The date separator is only valid for format **HMS** .

To set the **TimeSeparator** at design time, click to the right of the property and select a value from the drop-down list. Values are colon (:), comma (,), period (.), and null ().

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsTimeField Class](amfDdsTimeFieldClass.html) <br /> [ DdsTimeField Class Members](amfDdsTimeFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
