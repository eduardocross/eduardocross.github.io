---
title: AdgConnection.op_Equality Method

Id: dcsAdgConnectionclassopEqualityMethod
TocParent: dcsAdgConnectionMethodsMain
TocOrder: 7

keywords: op_Equality method
keywords: AdgConnection.op_Equality method

keywords: comparing two AdgConnection objects
keywords: how to, compare two AdgConnection objects

---

Compares two instances of <span> **AdgConnection** </span> for equality.
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **AdgConnection.op_Equality(x, y)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic]</span>
 **returnValue = AdgConnection.op_Equality(x, y)** 
      </pre>

Parameters

<dl>
        <dt>
 *x* 
        </dt>
        <dd>An **AdgConnection**  object to compare. </dd>
        <dt>
 *y* 
        </dt>
        <dd>An **AdgConnection**  object to compare.</dd>
</dl>

Return Value

**True** if <span> *x* </span> and <span> *y* </span> have the same invocation lists; otherwise **false** .
Exceptions

None.
Remarks

Returns **true** if the references being compared refer to the same object. Otherwise, returns the value of the [Equals ](dcsAdgConnectionClassEqualsMethod.html) method invoked on left, and passed right as a parameter. 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgConnection Class Members](dcsAdgConnectionMembers.html)
      <br />
      [Equals Method](dcsAdgConnectionClassEqualsMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

