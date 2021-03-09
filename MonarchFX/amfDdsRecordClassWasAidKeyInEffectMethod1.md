---
title: DdsRecord.WasAidKeyInEffect(ConditionalValue, integer)

Id: amfDdsRecordClassWasAidKeyInEffectMethod1
TocParent: amfDdsRecordClassWasAidKeyInEffectMethods
TocOrder: 10

---

This overloaded method returns a boolean value indicating if the indicator expression was in effect for the keys specified. If in effect, the resulting indicator is also returned.

#### Syntax
<pre class="prettyprint"> **BegFunc WasAidKeyInEffect Access(*Public) Type(*Boolean)
   DclSrParm *indExpression*  Type(ASNA.Monarch.WebDspF.ConditionalValue) Rank(1)
   DclSrParm *resultingIndicator*  Type(*Integer)** </pre>

#### Parameters
<dl>
        <dt>
 *indExpression* 
        </dt>
        <dd>An array of 
        [
        ASNA.Monarch.WebDspF.ConditionalValue](amfConditionalValueClass.html) objects that
        represents the indicator expression.</dd>
        <dt>
 *resultingIndicator* 
        </dt>
        <dd>Integer. The indicator set as a result of the
        evaluation of the indicator expression.</dd>
</dl>

#### Return Value
**True** if the method determines the indicator expression was present in the conditional values and also returns the *resultingIndicator* set; otherwise **False** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ConditionalValue Class](amfConditionalValueClass.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) 
