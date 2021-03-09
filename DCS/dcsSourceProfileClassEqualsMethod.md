---
title: SourceProfile.Equals Method

Id: dcsSourceProfileClassEqualsMethod
TocParent: dcsSourceProfileMethodsMain
TocOrder: 1

keywords: Equals method
keywords: SourceProfile.Equals method

---

Returns <span> **true** </span> if the [SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) objects being compared refer to the same object. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public override bool Equals(<br />   object obj<br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Overrides Function Equals( _<br />   ByVal obj As Object _<br />) As Boolean** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc Equals Type(*Boolean) Access(*Public) Modifier(*Overrides)<br />   DclSrParm obj Type(*Object)** 
      </pre>

Parameters

<dl>
        <dt>
 *obj* 
        </dt>
        <dd>The	<span>[SourceProfile](dcsSourceProfileClass.html)</span>
						object to compare with this instance.
					</dd>
</dl>

Returns

Boolean. **True** if the [SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) objects being compared refer to the same object; otherwise **False** .
Exceptions

None.
Remarks

Returns **false** if *obj* refers to a null instance. Otherwise returns the value of the [ op_Equality](dcsSourceProfileClassop_EqualityMethod.html) method invoked on the **SourceProfile** of this object against the **SourceProfile** of the object being compared.
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See Also

<dl />
      <span>
        [SourceProfile Class](dcsSourceProfileClass.html)
        <br />
        [SourceProfile Class Members](dcsSourceProfileMembers.html) <br />[
						op_Equality Method](dcsSourceProfileClassop_EqualityMethod.html)<br />[ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)</span>

