---
title: DdsBaseDate.ButtonSuffix Property

Id: amfDdsBaseDateClassButtonSuffixProperty
TocParent: amfDdsBaseDateClassProperties
TocOrder: 60

keywords: ButtonSuffix property
keywords: DdsBaseDate.ButtonSuffix property
keywords: Web server controls [ASNA.Monarch], date field button suffix
keywords: how to, set date field control button suffix
keywords: how to, get date field control button suffix
keywords: display files, setting date field control button suffix
keywords: display files, getting date field control button suffix
keywords: web controls, setting date field control button suffix
keywords: web controls, getting date field control button suffix
keywords: field controls, date field, button suffix
keywords: button suffix

---

Gets or sets the value of a suffix to be appended to the name of the control creating the [ ButtonID](amfDdsBaseDateClassButtonIDProperty.html) for a date control field.

#### Syntax
<pre class="syntax"> **BegProp ButtonSuffix Access(*Public) Type(*String)
     BegGet;   BegSet** </pre>

#### Property Values
String containing the suffix to be appended to the name of the control creating the **ButtonID** . The default is **_Button** .

#### Remarks
To set the **ButtonSuffix** at design time, click to the right of the property and enter a suffix value. Once a value is entered, the **ButtonID** property is updated to show its new values. For example, if the **ID** is **"** **DoneDate"** and the suffix property is set to **"** **_MyButton"** , the **ButtonID** would be **"DoneDate_MyButton"** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBaseDate Class](amfDdsBaseDateClass.html) <br /> [ DdsBaseDate Class Members](amfDdsBaseDateClassMembers.html) <br /> [ Derived Classes](amfDdsBaseDateDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
