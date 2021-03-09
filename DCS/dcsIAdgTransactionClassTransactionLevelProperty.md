---
title: IAdgTransaction.TransactionLevel Property

Id: dcsIAdgTransactionClassTransactionLevelProperty
TocParent: dcsIAdgTransactionProperties
TocOrder: 2

keywords: TransactionLevel property
keywords: IAdgTransaction.TransactionLevel property
keywords: enumerations [DCS 16.0 TransactionLevel, used by
keywords: TransactionLevel enumeration, used by

keywords: transactions, connection lock level returned
keywords: transaction connection lock level returned
keywords: database transactions, connection lock level returned

---

The locking level for the transaction.
<pre>        <span class="lang">[C#]</span>
 **public TransactionLevel TransactionLevel { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **public ReadOnly Function TransactionLevel As [ASNA.DataGate.Common.TransactionLevel](dcsTransactionLevelEnumeration.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp TransactionLevel Type(TransactionLevel) Access(*Public) Modifier(*NotOverridable)** 
      </pre>

Property Value

[ASNA.DataGate.Common.TransactionLevel](dcsTransactionLevelEnumeration.html). The **TransactionLevel** for the transaction.
Remarks

The value of this property is used by the database provider to prioritize the transaction. **TransactionLevel** is initialized by the overloads of [AdgConnection.BeginAutoTransaction](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) and [AdgConnection.BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html) that provide the *tl* parameter. Other versions of **BeginAutoTransaction** and **BeginTransaction** initialize the property to **TransactionLevel.Medium** .
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span>
See Also

<dl />
      [IAdgTransaction Class](dcsIAdgTransactionClass.html)
      <br />
      [IAdgTransaction Class Members](dcsIAdgTransactionMembers.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [TransactionLevel Enumeration](dcsTransactionLevelEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

