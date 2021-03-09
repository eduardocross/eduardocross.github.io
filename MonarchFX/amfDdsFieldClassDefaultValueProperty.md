---
title: DdsField.DefaultValue Property

Id: amfDdsFieldClassDefaultValueProperty
TocParent: amfDdsFieldClassProperties
TocOrder: 40

keywords: DefaultValue property
keywords: DdsField.DefaultValue property
keywords: Web server controls [ASNA.Monarch], field default value
keywords: how to, set field control default value
keywords: display files, setting field control default value
keywords: web controls, setting field control default value
keywords: field controls, default value

---

Sets a default value to display in a Field with the [Usage](amfDdsDataFieldClassUsageProperty.html) property set to <code> **InputOnly** </code>.

#### Syntax
<pre class="syntax"> **BegProp DefaultValue Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. The default value to display in the fields marked <code>InputOnly</code>.

#### Remarks
To set this property at design time, click on the right side of the property window and enter the default value for the field.

The value specified in this property will be used as the value of the field if the Field's [Usage](amfDdsDataFieldClassUsageProperty.html) property is <code>InputOnly</code>. If the **Usage** value is <code>OutputOnly</code> or <code>Both</code>, the selected DefaultValue will be shown ONLY the first time the field is displayed while the associated program is running(any programmatically generated content will be ignored). If the field's value is updated while the program is running, the updated value will be shown instead.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Class Members](amfDdsCharFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ CheckedValue Property](amfDdsCharFieldClassCheckedValueProperty.html) <br /> [ UncheckedValue Property](amfDdsCharFieldClassUncheckedValueProperty.html) <br /> [ChangeInd Property](amfDdsDataFieldClassChangeIndProperty.html) <br />[ DdsCharField.InputStyle](amfDdsCharFieldClassInputStyleProperty.html)<br />[ DdsDataField.ChangeInd Property](amfDdsDataFieldClassChangeIndProperty.html)<br />[ DdsRecord.ChangeInd Property](amfDdsRecordClassChangeIndProperty.html)
