---
title: DdsBaseDate.ButtonID Property

Id: amfDdsBaseDateClassButtonIDProperty
TocParent: amfDdsBaseDateClassProperties
TocOrder: 50

keywords: ButtonID property
keywords: DdsBaseDate.ButtonID property
keywords: Web server controls [ASNA.Monarch], date field button id
keywords: how to, set date field control button id
keywords: how to, get date field control button id
keywords: display files, setting date field control button id
keywords: display files, getting date field control button id
keywords: web controls, setting date field control button id
keywords: web controls, getting date field control button id
keywords: field controls, date field, button id
keywords: button id

---

Gets the button identification comprised of the **ButtonSuffix** appended to the name of the control for a date control field.

#### Syntax
<pre class="syntax"> **BegProp ButtonID Access(*Public) Type(*String)
    BegGet;** </pre>

#### Property Values
String containing the button identification comprised of the suffix appended to the name of the control.

#### Remarks
Once a [ ButtonSuffix](amfDdsBaseDateClassButtonSuffixProperty.html) property value is entered, the **ButtonID** property will display the new values. For example, if the **ID** is **"DoneDate"** and the suffix property is set to **"_MyButton"** , the **ButtonID** property would be **"DoneDate_MyButton"** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBaseDate Class](amfDdsBaseDateClass.html) <br /> [ DdsBaseDate Class Members](amfDdsBaseDateClassMembers.html) <br /> [ Derived Classes](amfDdsBaseDateDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
