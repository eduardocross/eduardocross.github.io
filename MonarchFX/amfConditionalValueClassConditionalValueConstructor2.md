---
title: ConditionalValue Constructor(string, string)

Id: amfConditionalValueClassConditionalValueConstructor2
TocParent: amfConditionalValueClassConditionalValueConstructors
TocOrder: 20

---

This method constructs a new instance of a **ConditionalValue** object with the conditional indicator expression established.

#### Syntax
<pre class="syntax"> **BegConstructor ConditionalValue Access(*Public)
  DclSrParm *condition*  Type(*String)
  DclSrParm *val*  Type (*String)** </pre>

#### Parameters
<dl>
        <dt>
 *condition* 
        </dt>
        <dd>

String containing the ***condition*** of the indicator expression that when evaluated to true, cause the value to be selected.
</dd>
        <dt>
 *val* 
        </dt>
        <dd>

String containing the ***value*** for the condition expression.
</dd>
</dl>

#### Remarks
The composition of a conditional indicator expression is ** *value* : *condition* ** . An example using conditional indicators might be "Red:03 &amp; !99", where ***value*** is "Red" and the ***condition*** is "03 &amp; !99". When this expression is evaluated, the value "Red" is selected if *IN03 is *ON and *IN99 is *OFF.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ConditionalValue Class](amfConditionalValueClass.html) <br /> [ ConditionalValue Class Members](amfConditionalValueClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
