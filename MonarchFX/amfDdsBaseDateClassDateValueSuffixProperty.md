---
title: DdsBaseDate.DateValueSuffix Property

Id: amfDdsBaseDateClassDateValueSuffixProperty
TocParent: amfDdsBaseDateClassProperties
TocOrder: 120

keywords: DateValueSuffix property
keywords: DdsBaseDate.DateValueSuffix property
keywords: Web server controls [ASNA.Monarch], date field value suffix
keywords: how to, set date field control value suffix
keywords: how to, get date field control value suffix
keywords: display files, setting date field control value suffix
keywords: display files, getting date field control value suffix
keywords: web controls, setting date field control field separator
keywords: web controls, getting date field control value suffix
keywords: field controls, date field
keywords: date field, value suffix

---

Gets or sets a string value containing a value to be appended to the name of the control creating the [ DateValueID](amfDdsBaseDateClassDateValueIDProperty.html) for a date control field.

#### Syntax
<pre class="syntax"> **BegProp DateValueSuffix Access(*Public) Type(*String)
   BegGet;   BegSet** </pre>

#### Property Values
String containing the value to be appended to the name of the control creating the **DateValueID** . The default is **_DateValue** .

#### Remarks
To set the **DateValueSuffix** at design time, click to the right of the property and enter a suffix value. Once a value is entered, the **ButtonID** property is updated to show the new values. For example, if the **ID** is **"DoneDate"** and the suffix property is set to **"_MyDateValue"** , the **ButtonID** would be **"DoneDate_MyDateValue"** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBaseDate Class](amfDdsBaseDateClass.html) <br /> [ DdsBaseDate Class Members](amfDdsBaseDateClassMembers.html) <br /> [ Derived Classes](amfDdsBaseDateDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
