---
title: DdsDataField.Usage Property

Id: amfDdsDataFieldClassUsageProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 110

keywords: CssClass property, _OutputOnly appended
keywords: CSS, _OutputOnly
keywords: _OutputOnly
keywords: cascading style sheets, _OutputOnly
keywords: Usage property
keywords: DdsDataField.Usage property
keywords: Web server controls [ASNA.Monarch], field usage
keywords: how to, set field control usage
keywords: how to, get field control usage
keywords: display files, setting field control usage
keywords: display files, getting field control usage
keywords: web controls, setting field control usage
keywords: web controls, getting field control usage
keywords: field controls, usage
keywords: FieldUsages enumeration, used by
keywords: enumerations [ASNA.Monarch.WebDspF], FieldUsages, used by

---

Gets gets sets a value that indicates how the field is used, output, input, both (input and output), or hidden.

#### Syntax
<pre class="prettyprint"> **BegProp Usage Access(*Public ) Type(ASNA.Monarch.WebDspF.FieldUsages)
   BegGet;  BegSet** </pre>

#### Property Values
[ ANSA.Monarch.WebDspF.FieldUsages](amfFieldUsagesEnumeration.html). One of the valid enumeration values indicating how the field is to be used.

#### Remarks
To set the **Usage** property, click on the right side of the property window and choose one of the values from the drop-down box: Hidden, OutputOnly, InputOnly, or Both. The default is **both** (input and output).

When this property is set to ** *OutputOnly* ** , Monarch Framework appends **"_OutputOnly"** to the control's CssClass property at runtime. For example, if the CssClass property at runtime is "DdsDecField", then at runtime the control's generated HTML class attribute would be **class="DdsDecField_OutputOnly"** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br />[ FieldUsages Enumeration](amfFieldUsagesEnumeration.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
