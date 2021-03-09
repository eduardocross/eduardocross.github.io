---
title: SourceProfile.Clone Method

Id: dcsSourceProfileClassCloneMethod
TocParent: dcsSourceProfileMethodsMain
TocOrder: 0

keywords: SourceProfile.Clone method
keywords: Clone method
keywords: database connections, create new source profile copy
keywords: connections, database source profile copied
keywords: how to, copy database source profile

---

Returns a copy of the <span> **SourceProfile** </span> object.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public virtual new object Clone();**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Overridable NotOverridable Clone() As Object**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc Clone Type(*Object) Access(*Public) Modifier(*NotOverridable)** 
      </pre>

Returns

An instance of [SourceProfile Property](dcsSourceProfileClass.html).
Exceptions

None.
Remarks

This method returns a copy of the **SourceProfile** object. If successful, the copy’s [SourceProfile ](dcsAdgConnectionClassSourceProfileProperty.html)property will reference the same **SourceProfile** object contained in the **SourceProfile** property of the copied object.

If the copied object is in the open [ State](dcsAdgConnectionClassStateProperty.html), the [AdgConnection.Open](dcsAdgConnectionClassOpenMethod.html) method is invoked on the copy thus providing a new database connection.

Note: A database connection cannot be shared between two instances of **SourceProfile** .
Requirements

**Namespace:** [ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

<span><strong style="FONT-WEIGHT: bold">Assembly:</strong> ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro </span> 
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [SourceProfile Property](dcsAdgConnectionClassSourceProfileProperty.html)
      <br />
      [State Property](dcsAdgConnectionClassStateProperty.html)
      <br />
      [Open Method](dcsAdgConnectionClassOpenMethod.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

