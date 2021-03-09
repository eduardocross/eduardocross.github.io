---
title: DdsDecDateField.SuppressLeadingZeroes Property

Id: amfDdsDecDateFieldClassSuppressLeadingZeroesProperty
TocParent: amfDdsDecDateFieldClassProperties
TocOrder: 149

keywords: Value property
keywords: DdsDecDateField.Value property
keywords: Web server controls [ASNA.Monarch], date field value
keywords: how to, set date field control value
keywords: how to, get date field control value
keywords: display files, setting date field control value
keywords: display files, getting date field control value
keywords: web controls, setting date field control value
keywords: web controls, getting date field control value
keywords: field controls, date fields, value

---

Gets or sets whether leading zeroes in the date field value are shown or suppressed. (Defaults to **False** ).

#### Syntax
<pre class="prettyprint"> **BegProp SuppressLeadingZeroes Access(*Public) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean (defaults to **False** ) that determines whether to drop the leading zeroes in the mm.dd.yy value. If **True** , leading zeroes in the month and day categories are deleted, so the value 04.04.06 would be displayed as 4.4.06.

#### Remarks
While this property defaults to **False,** if the numeric field is identified as a date when importing Display Files and it has editCode = "Y", then this property is set to **True** . 

To set this property at design time, click on the right side of the property window and select True or False. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDecDateField Class](amfDdsDecDateFieldClass.html) <br /> [ DdsDecDateField Class Members](amfDdsDecDateFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
<!-- last one -->

