---
title: SourceProfile.op_Equality Method

Id: dcsSourceProfileClassop_EqualityMethod
TocParent: dcsSourceProfileMethodsMain
TocOrder: 4

keywords: how to, compare two SourceProfile instances for equality
keywords: op_Equality method
keywords: SourceProfile.op_Equality method

---

Compares two instances of <span>SourceProfile</span> for equality.
<pre class="prettyprint">
        <span>[Visual RPG]</span>
        <span>
SourceProfile.op_Equality</span>
        <span>(x, y)</span>
      </pre>
      <pre class="prettyprint">[Visual Basic]<span>
returnValue = SourceProfile.op_Equality</span>(x, y)</pre>

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

Return Value

<span>True</span> if <span>x</span> and <span>y</span> have the same invocation lists; otherwise false.
Exceptions

None.
Remarks

Returns<span> true</span> if the references being compared refer to the same object. Otherwise, returns the value of the [Equals](dcsSourceProfileClassEqualsMethod.html) method invoked on left, and passed right as a parameter. 
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html) <br />[SourceProfile Class Members](dcsSourceProfileMembers.html)<br />[ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

