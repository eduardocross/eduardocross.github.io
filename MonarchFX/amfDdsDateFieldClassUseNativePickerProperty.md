---
title: DdsDateField.UseNativePicker Property

Id: amfDdsDateFieldClassUseNativePickerProperty
TocParent: amfDdsDateFieldClassProperties
TocOrder: 150

keywords: UseNativePicker property
keywords: DdsDateField.UseNativePicker property
keywords: Web server controls [ASNA.Monarch], date field Suppress Leading Zeroes
keywords: how to, set date field control Suppress Leading Zeroes
keywords: how to, get date field control Suppress Leading Zeroes
keywords: display files, setting date field control Suppress Leading Zeroes
keywords: display files, getting date field control Suppress Leading Zeroes
keywords: web controls, setting date field control Suppress Leading Zeroes
keywords: web controls, getting date field control Suppress Leading Zeroes
keywords: field controls, date fields, UseNativePicker

---

Sets whether to use the native date picker embedded into many modern browsers and devices. (Defaults to **True** ).

#### Syntax
<pre class="prettyprint"> **BegProp UseNativePicker Access(*Public) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean (defaults to **True** ). If **True** , the native date picker, as supplied on google Chrome or Apple's Safari, will be called when the user fills or modifies the Value.

#### Remarks
This property has no effect if the DdsDateField is viewed on a platform which does not support native date pickers, such as Internet Explorer. 

When set to <code>True</code> most browsers that support Native Pickers will ignore the [NoDateText](amfDdsBaseDateClassNoDateTextProperty.html) property.

To set this property at design time, click on the right side of the property window and select <code>True</code> or <code>False</code>. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDateField Class](amfDdsDateFieldClass.html) <br /> [ DdsDateField Class Members](amfDdsDateFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
<!-- last one -->

