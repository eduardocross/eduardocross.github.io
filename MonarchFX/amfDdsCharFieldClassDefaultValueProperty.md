---
title: DdsCharField.DefaultValue Property

Id: amfDdsCharFieldClassDefaultValueProperty
TocParent: amfDdsCharFieldClassPropertiesMain
TocOrder: 40

keywords: DefaultValue property
keywords: DdsCharField.DefaultValue property
keywords: Web server controls [ASNA.Monarch], field default value
keywords: how to, set field control default value
keywords: display files, setting field control default value
keywords: web controls, setting field control default value
keywords: field controls, default value

---

Sets a default value to display in a CharField with the [Usage](amfDdsDataFieldClassUsageProperty.html) property set to <code> **InputOnly** </code>.

#### Syntax
<pre class="syntax"> **BegProp DefaultValue Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. The default value to display in the fields marked <code>InputOnly</code>.

#### Remarks
To set this property at design time, click on the right side of the property window and enter the default value for the field.

The value specified in this property will be used as the value of the field if the Field's [Usage](amfDdsDataFieldClassUsageProperty.html) property is <code>InputOnly</code>. If the **Usage** value is <code>OutputOnly</code> or <code>Both</code>, the selected DefaultValue will be shown ONLY the first time the field is displayed while the associated program is running(any programmatically generated content will be ignored). If the field's value is updated while the program is running, the updated value will be shown instead.

The following variation applies when the [ DdsCharField.InputStyle](amfDdsCharFieldClassInputStyleProperty.html) property is <code> **Checkbox** </code>. 

This <code> **DefaultValue** </code> property is used on character fields that are displayed as **Checkboxes** to determine if the checkbox should be marked as checked or not. On output operations, the value of the field determines the state of the checkbox as follows: 

- If the field value is equal to 
            [
            CheckedValue](amfDdsCharFieldClassCheckedValueProperty.html) the box is checked; if the field
            value is equal to the 
            [
            UncheckedValue](amfDdsCharFieldClassUncheckedValueProperty.html) then the box is unchecked.
- However if the field
          value is neither equal to 
          <code> **CheckedValue** </code> or 
          <code> **UncheckedValue** </code>, then the box will be checked if the 
          <code> **CheckedValue** </code> is equal to the 
          <code> **DefaultValue** </code>;
          basically, 
          <code> **DefaultValue** </code> determines the default checkbox
          state for those fields with values outside of their
          domain.
- In any event, when the
          Checkbox is displayed as checked, the value of 
          <code> **CheckedValue** </code> will be returned to the
          program, and when the Checkbox is NOT checked, the value
          of 
          <code> **UnCheckedValue** </code> will be returned to the
          program. In the process of returning the 
          <code> **UnCheckedValue** </code>, if this value differs
          from the value output from the program, then
          the 
          <code> **ChangeInd** </code> indicator will be set to TRUE for the field and for
          the Record (
          [
          DdsDataField.ChangeInd](amfDdsDataFieldClassChangeIndProperty.html) and 
          [
          DdsRecord.ChangeInd](amfDdsRecordClassChangeIndProperty.html) respectively).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Class Members](amfDdsCharFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ CheckedValue Property](amfDdsCharFieldClassCheckedValueProperty.html) <br /> [ UncheckedValue Property](amfDdsCharFieldClassUncheckedValueProperty.html) <br /> [ChangeInd Property](amfDdsDataFieldClassChangeIndProperty.html) <br />[ DdsCharField.InputStyle](amfDdsCharFieldClassInputStyleProperty.html)<br />[ DdsDataField.ChangeInd Property](amfDdsDataFieldClassChangeIndProperty.html)<br />[ DdsRecord.ChangeInd Property](amfDdsRecordClassChangeIndProperty.html)
