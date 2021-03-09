---
title: IAdgTransaction.Name Property

Id: dcsIAdgTransactionClassNameProperty
TocParent: dcsIAdgTransactionProperties
TocOrder: 1

keywords: Name property
keywords: IAdgTransaction.Name property
keywords: database transactions, name of
keywords: name of database transaction
keywords: how to, get name of database transaction

---

The name of the transaction.
<pre>        <span class="lang">[C#]</span>
 **Public virtual new string Name { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public NotOverridable ReadOnly Property Name As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Name Access(*Public) Type(*String) Modifier(*NotOverridable)** 
      </pre>

Returns

**String** . The name of the transaction as specified when the transaction was initiated.
Remarks

The name of the transaction is an arbitrary string which the database provider may use to identify transaction resources (e.g., the "TEXT" parameter of the iSeries "STRCMTCTL" command) 

The value of this property is initialized by the overloads of [ AdgConnection.BeginAutoTransaction](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) and [ AdgConnection.BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html) that provide the *Name* parameter. Other versions of **BeginAutoTransaction** and **BeginTransaction** set the value of **Name** to an empty string.

The value of **Name** is constant during the lifetime of **IAdgTransaction** with the following exception. If **IAdgTransaction** represents an automatic transaction, and the [ Commit](dcsIAdgTransactionClassCommitMethod2.html) method overload which defines the *TransactionName* parameter is invoked, the value of **Name** is set to the value of *TransactionName* upon the successful completion of **Commit** . 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgTransaction Class](dcsIAdgTransactionClass.html)
      <br />
      [IAdgTransaction Class Members](dcsIAdgTransactionMembers.html)
      <br />
      [Commit(String) Method](dcsIAdgTransactionClassCommitMethod2.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [BeginTransaction 
					Method](dcsAdgConnectionClassBeginTransactionMethodMain.html)
      <br />
      [BeginAutoTransaction 
					Method](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

