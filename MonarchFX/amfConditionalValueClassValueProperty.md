---
title: ConditionalValue.Value Property

Id: amfConditionalValueClassValueProperty
TocParent: amfConditionalValueClassProperties
TocOrder: 120

keywords: Value property
keywords: ConditionalValue.Value property
keywords: conditioning expressions, value portion
keywords: indicator expressions, value portion
keywords: how to, set value portion of conditional expression
keywords: how to, get value portion of conditional expression
keywords: how to, set value portion of indicator expression
keywords: how to, get value portion of indicator expression
keywords: web controls, value portion of conditional expression
keywords: display files, value portion of conditional expression
keywords: web controls, value portion of indicator expression
keywords: display files, value portion of indicator expression

---

Gets or sets the *value* portion of a conditional indicator expression.

#### Syntax
<pre class="syntax"> **BegProp Value Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the ***value*** portion of a conditional indicator expression.

#### Remarks
The composition of a conditional indicator expression is ** *value* : *condition* ** . An example using conditional indicators might be Red:03 &amp; !99, where the **Value** property is "Red".
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[ ConditionalValue Class](amfConditionalValueClass.html) <br /> [ ConditionalValue Class Members](amfConditionalValueClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
