---
title: DdsBaseDate.DateSeparator Property

Id: amfDdsBaseDateClassDateSeparatorProperty
TocParent: amfDdsBaseDateClassProperties
TocOrder: 100

keywords: DateSeparator property
keywords: DdsBaseDate.DateSeparator property
keywords: enumerations [ASNA.Monarch.WebDspF], DdsBaseDate.DdsDateSeparator, used by
keywords: DdsBaseDate.DdsDateSeparator enumeration, used by
keywords: Web server controls [ASNA.Monarch], date field separator
keywords: how to, set date field control field separator
keywords: how to, get date field control field separator
keywords: display files, setting date field control field separator
keywords: display files, getting date field control field separator
keywords: web controls, setting date field control field separator
keywords: web controls, getting date field control field separator
keywords: field controls, date field, field separator

---

Gets or sets a value identifying the character to be used to separate the components of the date field for formats **DMY** , **MDY** , or **YMD** only.

#### Syntax
<pre class="syntax"> **BegProp DateSeparator Access(*Public) Type(DdsBaseDate.DdsDateSeparator)
     BegGet;  BegSet** </pre>

#### Property Values
[ DdsBaseDate.DdsDateSeparator](amfDdsDateSeparatorEnumeration.html). One of the valid enumeration values identifying the date field separator.

#### Remarks
The date separator is only valid for formats **DMY** , **MDY** , or **YMD** .

To set the **DateSeparator** at design time, click to the right of the property and select a value from the drop-down list. The default is **DEFAULT** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBaseDate Class](amfDdsBaseDateClass.html) <br /> [ DdsBaseDate Class Members](amfDdsBaseDateClassMembers.html) <br /> [ Derived Classes](amfDdsBaseDateDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
