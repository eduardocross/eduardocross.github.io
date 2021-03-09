---
title: ConditionalValue.Condition Property

Id: amfConditionalValueClassConditionProperty
TocParent: amfConditionalValueClassProperties
TocOrder: 10

keywords: Condition property
keywords: ConditionalValue.Condition property
keywords: conditioning expressions, condition portion
keywords: indicator expressions, condition portion
keywords: how to, set condition portion of conditional expression
keywords: how to, get condition portion of conditional expression
keywords: how to, set condition portion of indicator expression
keywords: how to, get condition portion of indicator expression
keywords: web controls, condition portion of conditional expression
keywords: display files, condition portion of conditional expression
keywords: web controls, condition portion of indicator expression
keywords: display files, condition portion of indicator expression

---

Gets or sets the *condition* portion of a conditional indicator expression.

#### Syntax
<pre class="syntax"> **BegProp Condition Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the ***condition*** of a conditional indicator expression as two operands. The first for when ***value*** evaluates true, the second when ***value*** evaluates false. Either can be *NONE

#### Remarks
The composition of a conditional indicator expression is ** *value* : *condition* ** . An example using conditional indicators might be Red:03 &amp; !99, where the **Condition** property is "03 &amp; !99".
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[ ConditionalValue Class](amfConditionalValueClass.html) <br /> [ ConditionalValue Class Members](amfConditionalValueClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
