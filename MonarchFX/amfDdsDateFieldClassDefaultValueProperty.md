---
title: DdsDateField.DefaultValue Property

Id: amfDdsDateFieldClassDefaultValueProperty
TocParent: amfDdsDateFieldClassProperties
TocOrder: 10

keywords: DefaultValue property
keywords: DdsDateField.DefaultValue property
keywords: Web server controls [ASNA.Monarch], date field default value
keywords: how to, set datefield control default value
keywords: display files, setting date field control default value
keywords: web controls, setting date field control default value
keywords: field controls, date fields, default value

---

Sets a default value to display in a DateField.

#### Syntax
<pre class="prettyprint"> **BegProp DefaultValue Access(*Public) Type(System.DateTime)
   BegGet;  BegSet** </pre>

#### Property Values
System.DateTime.

#### Remarks
To set this property at design time, click on the right side of the property window and select the date from the calendar.

The value specified in this property will be used as the value of the field if the Field's [Usage](amfDdsDataFieldClassUsageProperty.html) property is <code>InputOnly</code>. If the **Usage** value is <code>OutputOnly</code> or <code>Both</code>, the selected DefaultValue will be shown ONLY the first time the field is displayed while the associated program is running(any programmatically generated content will be ignored). If the field's value is updated while the program is running, the updated value will be shown instead.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDateField Class](amfDdsDateFieldClass.html) <br /> [ DdsDateField Class Members](amfDdsDateFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
<!-- last one -->

