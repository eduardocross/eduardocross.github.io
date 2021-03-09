---
title: DdsCharField.InputStyle Property

Id: amfDdsCharFieldClassInputStyleProperty
TocParent: amfDdsCharFieldClassPropertiesMain
TocOrder: 50

keywords: InputStyle property
keywords: DdsCharField.InputStyle property
keywords: InputStyles enumeration, used by
keywords: enumerations [ASNA.Monarch.WebDspF], InputStyles, used by
keywords: Web server controls [ASNA.Monarch], field input style
keywords: how to, set field control input style
keywords: how to, get field control input style
keywords: display files, setting field control input style
keywords: display files, getting field control input style
keywords: web controls, setting field control input style
keywords: web controls, getting field control input style
keywords: field controls, input style

---

Gets or sets the control style used to specify the field as a TextBox, Multi-line Textbox, Password, or a Checkbox.

#### Syntax
<pre class="syntax"> **BegProp InputStyle Access(*Public) Type([InputStyles](amfInputStylesEnumeration.html))
   BegGet;  BegSet** </pre>

#### Property Values
**InputStyles** references the style control for the field.

#### Remarks
The default is **Textbox** , which accepts any values from the user. However, use the [ Values](amfDdsDataFieldClassValuesProperty.html) property to enter the valid values that the application can accept from the user. If the user may not know what the values mean, also use the [ ValuesText](amfDdsDataFieldClassValuesTextProperty.html) property to indicate text for each of the entries in the **Values** property. However, for the entries in **Values** and/or the **ValuesText** to display for the user, use the [ ValuesStyle](amfDdsDataFieldClassValuesStyleProperty.html) property to specify whether just the **Values** or the **ValuesText** displays, or whether you want **both** of them to display in a drop-down box. ** *Please note that this also applies to a Multi-line textbox.* ** 

When the field is set to display as a **Checkbox** , you will need to know what the valid values for the field are, and determine if you will specify the accepted values when the Checkbox is checked or unchecked. To do this, specify entries in either the [ CheckedValue](amfDdsCharFieldClassCheckedValueProperty.html) or [ UnCheckedValue](amfDdsCharFieldClassUncheckedValueProperty.html) properties.

When set to **Multiline** the browser will render the contents using multiple lines (HTML &lt;textarea&gt;), otherwise it will show it as a long single-line field (HTML &lt;input&gt;). If a field is using multiple-lines the browser always wraps the content on a blank, in that sense, the **WRDWRAP** keyword is always enabled; there is no way to have the contents wrap in the middle of a word (like in 5250).

The Wings import feature sets the DdsCharField **InputStyle** property to **Multiline** only when the **CNTFLD** keyword is present in DDS. The **WRDWRAP** will be ignored always (because it is implied).

To set this property at design time, click on the arrow on the right side of the property window and choose one of the options shown in the drop-down box.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Class Members](amfDdsCharFieldClassMembers.html) <br /> [ InputStyles Enumeration](amfInputStylesEnumeration.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ CheckedValue Property](amfDdsCharFieldClassCheckedValueProperty.html) <br /> [ UnCheckedValue Property](amfDdsCharFieldClassUncheckedValueProperty.html) <br /> [ ValuesText Property](amfDdsDataFieldClassValuesTextProperty.html) <br /> [Values Property](amfDdsDataFieldClassValuesProperty.html) <br /> [ ValuesStyle Property](amfDdsDataFieldClassValuesTextProperty.html) 
