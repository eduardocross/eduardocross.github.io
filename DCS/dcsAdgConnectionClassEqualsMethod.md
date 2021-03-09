---
title: AdgConnection.Equals Method

Id: dcsAdgConnectionClassEqualsMethod
TocParent: dcsAdgConnectionMethodsMain
TocOrder: 5

keywords: Equals method
keywords: AdgConnection.Equals method

keywords: comparing two AdgConnection objects
keywords: how to, compare two AdgConnection objects

---

#### Returns <span> **true** </span> if the [SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) properties of the objects being compared refer to the same object. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public override bool Equals(
   object obj
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Overrides Function Equals(_
 ByVal obj As Object
) As Boolean** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc Equals Type( *Boolean ) Access( *Public ) Modifier( *Overrides )** 
      </pre>

Parameters

<dl>
        <dt>obj
					</dt>
        <dd>The **AdgConnection**  object to compare with this instance.
					</dd>
</dl>

Exceptions

None.
Remarks

Returns<span> false</span> if <span> *obj* </span> refers to a null instance. Otherwise returns the value of the [ op_Equality](dcsAdgConnectionclassopEqualityMethod.html) method invoked on the <span> **SourceProfile** </span> of this <span> **AdgConnection** </span> object against the **SourceProfile** of the **AdgConnection** object being compared. 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgConnection Class Members](dcsAdgConnectionMembers.html)
      <br />
      [SourceProfile Property](dcsAdgConnectionClassSourceProfileProperty.html)
      <br />
      [op_Equality Method](dcsSourceProfileClassop_EqualityMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

