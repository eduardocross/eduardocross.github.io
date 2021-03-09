---
title: DdsDateField.Value Property

Id: amfDdsDateFieldClassValueProperty
TocParent: amfDdsDateFieldClassProperties
TocOrder: 120

keywords: Value property
keywords: DdsDateField.Value property
keywords: Web server controls [ASNA.Monarch], date field value
keywords: how to, set date field control value
keywords: how to, get date field control value
keywords: display files, setting date field control value
keywords: display files, getting date field control value
keywords: web controls, setting date field control value
keywords: web controls, getting date field control value
keywords: field controls, date fields, value
keywords: date fields, value

---

Gets or sets the System.DateTime for this field.

#### Syntax
<pre class="prettyprint"> **BegProp Value Access(*Public) Type(System.DateTime)
   BegGet;  BegSet** </pre>

#### Property Values
System.DateTime.

#### Remarks
To set this property at design time, click on the right side of the property window and select the date from the calendar.

This property is used exclusively for fields with Usage=InputOnly. For any other Usage (i.e. OutputOnly or Both), the value of the control will be the value defined by the field in the RPG (or AVR) code. It is recommended that the date field in the RPG (or AVR) code be initialized to a valid date (such as today's date), otherwise a *Blank value is not guaranteed to be parsed as a valid date by the Browser (i.e. when the property [UseNativePicker](amfDdsDateFieldClassUseNativePickerProperty.html) is set to "true", and the Browser supports date HTML5 input - like Chrome and Safari). The way Invalid dates are displayed may vary, for example, if DateFormat is "USA", the invalid date may show as 01/01/1901 in Chrome).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDateField Class](amfDdsDateFieldClass.html) <br /> [ DdsDateField Class Members](amfDdsDateFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
<!-- last one -->

