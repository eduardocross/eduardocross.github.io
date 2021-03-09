---
title: DdsBaseDate.DateValueID Property

Id: amfDdsBaseDateClassDateValueIDProperty
TocParent: amfDdsBaseDateClassProperties
TocOrder: 110

keywords: DateValueID property
keywords: DdsBaseDate.DateValueID property
keywords: Web server controls [ASNA.Monarch], date field value id
keywords: how to, set date field control value id
keywords: display files, setting date field control value id
keywords: web controls, setting date field control value id
keywords: field controls, date field
keywords: date field, value id

---

Gets the date identification comprised of the **DateValueSuffix** appended to the name of the control for a date control field.

#### Syntax
<pre class="syntax"> **BegProp DateValidID Access(*Public) Type(*String)
    BegGet;** </pre>

#### Property Values
String containing the date identification comprised of the date value suffix appended to the name of the control.

#### Remarks
Once a [ DateValueSuffix](amfDdsBaseDateClassDateValueSuffixProperty.html) property value is entered, the **DateValueID** property will display a new value. For example, if the **ID** is **"DoneDate"** and the suffix property is set to **"_MyDateValue"** , the **DateValueID** property would be **"DoneDate_MyDateValue"** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBaseDate Class](amfDdsBaseDateClass.html) <br /> [ DdsBaseDate Class Members](amfDdsBaseDateClassMembers.html) <br /> [ Derived Classes](amfDdsBaseDateDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
