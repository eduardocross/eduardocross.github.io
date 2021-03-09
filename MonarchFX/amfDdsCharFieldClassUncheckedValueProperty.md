---
title: DdsCharField.UncheckedValue Property

Id: amfDdsCharFieldClassUncheckedValueProperty
TocParent: amfDdsCharFieldClassPropertiesMain
TocOrder: 90

keywords: UncheckedValue property
keywords: DdsCharField.UncheckedValue property
keywords: Web server controls [ASNA.Monarch], checkbox unchecked value
keywords: how to, set field control checkbox unchecked value
keywords: how to, get field control checkbox unchecked value
keywords: display files, setting field control checkbox unchecked value
keywords: display files, getting field control checkbox unchecked value
keywords: web controls, setting field control checkbox unchecked value
keywords: web controls, getting field control checkbox unchecked value
keywords: field controls, checkbox unchecked value
keywords: checkboxes, unchecked value

---

When the [ InputStyle](amfDdsCharFieldClassInputStyleProperty.html) is set to display as a **CheckBox** , the **UncheckedValue** property gets or sets the value to identify the CheckBox as being "unchecked".

#### Syntax
<pre class="syntax"> **BegProp UncheckedValue Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. The value to identify the box as being unchecked.

#### Remarks
Use the **UncheckedValue** property to set the value(s) that specify the CheckBox as being 'unchecked'. You can also use the [ CheckedValue](amfDdsCharFieldClassCheckedValueProperty.html) property to specify the value(s) that determine the CheckBox as being 'checked'.

See [ DefaultValue](amfDdsCharFieldClassDefaultValueProperty.html) for details on fields containing values different of both **CheckedValue** and **UncheckedValue** .

To set this property at design time, click on the right side of the property window and enter the value to identify the box as being unchecked.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Members](amfDdsCharFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ DefaultValue Property](amfDdsCharFieldClassDefaultValueProperty.html) <br /> [ CheckedValue Property](amfDdsCharFieldClassCheckedValueProperty.html) <br /> [ InputStyles Property](amfDdsCharFieldClassInputStyleProperty.html) 
