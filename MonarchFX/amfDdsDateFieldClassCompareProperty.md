---
title: DdsDateField.Compare Property

Id: amfDdsDateFieldClassCompareProperty
TocParent: amfDdsDateFieldClassProperties
TocOrder: 6

keywords: Compare property
keywords: DdsDateField.Compare property
keywords: web controls, setting field control validation operator and value
keywords: how to, set field control validation operator and value
keywords: display files, setting field control validation operator and value
keywords: Web server controls [ASNA.Monarch], field control validation operator and value
keywords: field controls, validation operator and value

---

Gets or sets the relational operator and value used to validate user data input for the field. 

#### Syntax
<pre class="prettyprint"> **BegProp Compare Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the relational operator and value used to validate user data input.

#### Remarks
Relational operators are:

- &lt; for less than.
- &lt;= for less than or equal to.
- &gt; for greater than.
- &gt;= for greater than or equal to.
- = for equal.
- &lt;&gt; for unequal.
- <code>RANGE</code> to validate that the value falls between a preset minimum and maximum value (inclusive).

The format for the property for all operators other than <code>RANGE</code> is: <br /> <code>Operator *value* </code>

When using <code>RANGE</code> the format is:<br /> <code>RANGE *from-value to-value* </code>

The special value <code>*TODAY</code> can be used to represent the current date according to the system server, for the purposes of the comparison.

To set this property at design-time, click to the right of the property and enter the relational operator and value to use in the comparison operation. For example, to ensure the user enters a customer number of greater than or equal to 1000, enter &gt;= 1000 as shown in the example below.

![](Images/zzDdsDateFieldCompare.jpg) 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDateField Class](amfDdsDateFieldClass.html) <br /> [ DdsDateField Class Members](amfDdsDateFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDateFieldDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
