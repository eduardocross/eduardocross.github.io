---
title: DdsBaseDate.NoDateText Property

Id: amfDdsBaseDateClassNoDateTextProperty
TocParent: amfDdsBaseDateClassProperties
TocOrder: 170

keywords: NoDateText property
keywords: DdsBaseDate.NoDateText property
keywords: Web server controls [ASNA.Monarch], indicate text value for no date
keywords: how to, set text value for no date
keywords: how to, get text value for no date
keywords: display files, setting text value for no date
keywords: display files, getting text value for no date
keywords: web controls, setting text value for no date
keywords: web controls, getting text value for no date
keywords: field controls, date field, text value for no date

---

Sets the text to be displayed as a 'no date' value.

#### Syntax
<pre class="syntax"> **BegProp NoDateText Access(*Public) Type(*String)
    BegGet;   BegSet** </pre>

#### Property Values
String. The text value to display when no date is selected.

#### Remarks
This property sets a text value to be displayed when no date value has been entered. This is may be useful when a required date has not yet been selected.

This property applies **only** when RPG sets a date to <code>*LoVal</code> before writing the record format to the Workstation file.

If a value of <code>*Empty</code> is used, the text will still be displayed as empty, or blank. Any other entered text will be displayed on screen in the field.

To set **NoDateText** at design time, click to the right of the property and enter the text value for no date.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBaseDate Class](amfDdsBaseDateClass.html) <br /> [ DdsBaseDate Class Members](amfDdsBaseDateClassMembers.html) <br /> [ Derived Classes](amfDdsBaseDateDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
