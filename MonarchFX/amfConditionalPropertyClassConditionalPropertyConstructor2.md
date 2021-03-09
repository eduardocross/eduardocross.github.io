---
title: ConditionalProperty Constructor (string)

Id: amfConditionalPropertyClassConditionalPropertyConstructor2
TocParent: amfConditionalPropertyClassConditionalPropertyConstructors
TocOrder: 20

---

This method constructs a new instance of a **ConditionalProperty** object assigning an initial value to the [ PropString](amfConditionalPropertyClassPropStringProperty.html) property.

#### Syntax
<pre class="syntax"> **BegConstructor ConditionalProperty Access(*Public)
  DclSrParm *propString*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *propString* 
        </dt>
        <dd>

String containing the initial value for the **PropString** property. This is a list of comma separated conditional values. For example, "07 **:** 03 &amp; !99 **,** 03 **:** 06 **,** 99 **:** 05 ! 03"
</dd></dl>

#### Remarks
The composition of a conditional value expression is ** *value* : *condition* ** . For example (Red **:** 03 &amp; !99), where ***value*** is "Red", and the ***condition*** is "03 &amp; !99".
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[ ConditionalProperty Class](amfConditionalPropertyClass.html) <br /> [ ConditionalProperty Class Members](amfConditionalPropertyClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
