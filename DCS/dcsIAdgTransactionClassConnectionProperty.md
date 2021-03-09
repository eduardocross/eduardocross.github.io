---
title: IAdgTransaction.Connection Property

Id: dcsIAdgTransactionClassConnectionProperty
TocParent: dcsIAdgTransactionProperties
TocOrder: 0

keywords: Connection property
keywords: IAdgTransaction.Connection property
keywords: database transactions, connection context
keywords: database connections, transaction context
keywords: transaction context of database transaction
keywords: transaction context, about database connection

---

The connection to the database representing the transaction context.
<pre>        <span class="lang">[C#]</span>
 **Public virtual AdgConnection Connection { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Overridable ReadOnly Property Connection<br />   As [AdgConnection](dcsAdgConnectionClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Connection Type(AdgConnection) Modifier(*Overridable)
   BegGet** 
      </pre>

Property Value

[AdgConnection](dcsAdgConnectionClass.html). The connection to the database associated with the transaction.
Remarks

The value of this property is a reference to the **AdgConnection** object whose [AdgConnection.BeginAutoTransaction](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) or [AdgConnection.BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html) method was used to create the **IAdgTransaction** .

The context of a database transaction is limited to this connection. The [ Commit](dcsIAdgTransactionClassCommitMethods.html) and [Rollback ](dcsIAdgTransactionClassRollbackMethod.html) methods effect only those database modifications performed by this connection, within the transaction's boundaries. 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See 
Also

<dl />
      [IAdgTransaction Class](dcsIAdgTransactionClass.html)
      <br />
      [IAdgTransaction Class Members](dcsIAdgTransactionMembers.html)
      <br />
      [Commit Method](dcsIAdgTransactionClassCommitMethods.html)
      <br />
      [Rollback Method](dcsIAdgTransactionClassRollbackMethod.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html)
      <br />
      [BeginAutoTransaction 
					Method](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

