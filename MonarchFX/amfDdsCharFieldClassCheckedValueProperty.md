---
title: DdsCharField.CheckedValue Property

Id: amfDdsCharFieldClassCheckedValueProperty
TocParent: amfDdsCharFieldClassPropertiesMain
TocOrder: 30

keywords: CheckedValue property
keywords: DdsCharField.CheckedValue property
keywords: Web server controls [ASNA.Monarch], checkbox checked value
keywords: how to, set field control checkbox checked value
keywords: how to, get field control checkbox checked value
keywords: display files, setting field control checkbox checked value
keywords: display files, getting field control checkbox checked value
keywords: web controls, setting field control checkbox checked value
keywords: web controls, getting field control checkbox checked value
keywords: field controls, checkbox checked value
keywords: checkboxes, checked value

---

When the [ InputStyle](amfDdsCharFieldClassInputStyleProperty.html) is set to display as a **CheckBox** , the **CheckedValue** property gets or sets the value to identify the CheckBox as being "checked".

#### Syntax
<pre class="syntax"> **BegProp CheckedValue Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String value to identify the CheckBox as being checked.

#### Remarks
Use the **CheckedValue** property to set the value(s) that specify the CheckBox as being 'checked'. You can also use the [ UncheckedValue](amfDdsCharFieldClassUncheckedValueProperty.html) property to specify the value(s) that determine the CheckBox as being 'unchecked'.

See [ DefaultValue](amfDdsCharFieldClassDefaultValueProperty.html) for details on fields containing values different of both **CheckedValue** and **UncheckedValue** 

To set this property at design time, click on the right side of the property window and enter the value to identify the box as being checked.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Members](amfDdsCharFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ DefaultValue Property](amfDdsCharFieldClassDefaultValueProperty.html) <br /> [ UncheckedValue Property](amfDdsCharFieldClassUncheckedValueProperty.html) <br /> [ InputStyles Property](amfDdsCharFieldClassInputStyleProperty.html) 
