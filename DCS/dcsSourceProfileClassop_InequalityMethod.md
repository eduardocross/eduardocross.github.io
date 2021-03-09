---
title: SourceProfile.op_InEquality Method

Id: dcsSourceProfileClassop_InequalityMethod
TocParent: dcsSourceProfileMethodsMain
TocOrder: 5

keywords: op_InEquality method
keywords: SourceProfile.op_InEquality method
keywords: how to, compare two SourceProfile instances for inequality

---

Returns the opposite value returned by op_Equality.
<pre class="prettyprint">
        <span>[Visual RPG]</span>
        <span>
SourceProfile.op_Inequality</span>
        <span>(x, y)</span>
        <span>  </span>
      </pre>
      <pre class="prettyprint">
        <span>[Visual Basic]
returnValue = SourceProfile.op_Inequality</span>
        <span>(x, y)</span>
      </pre>

Parameters

<dl>
        <dt>
 *x* 
        </dt>
        <dd>A SourceProfile object to compare. </dd>
        <dt>
 *y* 
        </dt>
        <dd>A SourceProfile object to compare.
							</dd>
</dl>

Exceptions

None.
Remarks

Returns false if the references being compared refer to the same object. Otherwise, returns the negated value of the [Equals](dcsSourceProfileClassEqualsMethod.html) method invoked on left, and passed right as a parameter. 
Requirements

<strong style="FONT-WEIGHT: bold">Namespace:</strong> [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      <span>
        [SourceProfile Class](dcsSourceProfileClass.html) <br />[
						SourceProfile Members](dcsSourceProfileMembers.html)<br />[ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)</span>

