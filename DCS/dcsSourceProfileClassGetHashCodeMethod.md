---
title: SourceProfile.GetHashCode Method

Id: dcsSourceProfileClassGetHashCodeMethod
TocParent: dcsSourceProfileMethodsMain
TocOrder: 2

keywords: GetHashCode method
keywords: SourceProfile.GetHashCode method

---

Invokes the <span>GetHashCode</span> method of the <span>SourceProfile</span> property.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public override int GetHashCode();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Overrides Function GetHashCode() As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc GetHashCode Type(*Integer) Len(4) Access(*Public) Modifier(*Overrides)** 
      </pre>

Return Value

A 32-bit signed integer value, obtained from a hash algorithm using the values of the public properties of the SourceProfile object as input. Such a value can be used as a unique identifier for the set of entities described by a SourceProfile object. 
Exceptions

**NullReferenceException** . The value of the <span>SourceProfile</span> property is null. 
Remarks

This method returns a value identifying the contents of the object contained by the current SourceProfile. The value is not guaranteed to be unique to the SourceProfile instance. The value does not identify the current connection or the SourceProfile instance itself.

The DataGate client assembly uses this method internally for connection pooling and other functionality.
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)
      <br />
      [SourceProfile Class Constructors](dcsSourceProfileConstructorsMain.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

