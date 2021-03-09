---
title: IAdgTransaction Interface

Id: dcsIAdgTransactionClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 10

keywords: classes [DCS 16.0 IAdgTransaction class
keywords: interfaces [DCS 16.0 IAdgTransaction class
keywords: IAdgTransaction class
keywords: IAdgTransaction class, about IAdgTransaction class
keywords: database transactions, modeling management objects
keywords: database transactions, about managing
keywords: manual transactions
keywords: manual transactions, about managing
keywords: automatic transactions
keywords: automatic transactions, about managing

---

**IAdgTransaction** models database transaction management objects for database providers that support transaction processing. Instances of **IAdgTransaction** are manufactured by the [AdgConnection.BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html) and [AdgConnection.BeginAutoTransaction](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) methods.

For a list of all members of this type, see [IAdgTransaction Members](dcsIAdgTransactionMembers.html).

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) <br /> **ASNA.DataGate.Client.<span>IAdgTransaction</span>** 
<pre class="prettyprint">&lt;Serializable&gt; **Public Class IAdgTransaction** </pre>

Thread Safety

Instance members of this type are not guaranteed to be thread safe.
Remarks

**IAdgTransaction** provides properties and methods for managing database transaction processing. An instance of **IAdgTransaction** is associated with a single database connection (as referenced by the [ Connection](dcsIAdgTransactionClassConnectionProperty.html) property), which defines the operational context of a transaction. A [TransactionLevel](dcsIAdgTransactionClassTransactionLevelProperty.html) is assigned that the database provider may use to prioritize a transaction. The transaction is given an application-specific identifier ([Name](dcsIAdgTransactionClassNameProperty.html) ) that the database provider may use to identify transaction resources. 

Methods are provided to accept and cancel database modifications occuring within the boundaries of the transaction ([Commit](dcsIAdgTransactionClassCommitMethods.html) and [Rollback](dcsIAdgTransactionClassRollbackMethod.html) respectively). 

DCS provides two types of transaction objects - automatic and manual transactions, both of which implement **IAdgTransaction** . 

Manual transactions objects are constructed by the **AdgConnection.BeginTransaction** method. The database provider begins a transaction context upon successful construction of the manual transaction object. The behavior of the manual transaction with regard to the **Commit** and **Rollback** methods is database provider platform-dependent. Some providers may end the transaction context after a call to **Commit** or **Rollback** , while others may continue the transaction context after these method calls.

Automatic transactions are constructed by the **AdgConnection.BeginAutoTransaction** method. A transaction context is begun by the database provider upon successful construction of the automatic transaction object. The **Commit** and **Rollback** methods of an automatic transaction object perform the same functions as those of a manual transaction object. However, after successfully accepting or cancelling database modifications, both methods of an automatic transaction end the current transaction context and begin a new transaction using the parameters of the preceding transaction. The **IAdgTransaction** instance assumes control of the new transaction context. An automatic transaction is intended to emulate the behavior of IBM i database transactions for all database platforms.

With some database providers, calling the **Dispose** method to end the transaction context is critical to proper transaction processing. With both types of transaction objects, it is recommended that applications explicitly call **Dispose** to end the current transaction context rather than relying on the behavior of a specific database provider in ending the transaction.

Nested database transaction are allowed with transaction processing but this requires you to control the transaction flow from object to object while maintaining the security, recovery, concurrency, and integrity within the transaction boundary. DCS does not restrict nested transactions but the database provider may have mechanisms that prevent or limit such usage. Please consult the database provider's documentation for details.

At the time of this writing, only the IBM i database provider supports transaction processing.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgTransaction Members](dcsIAdgTransactionMembers.html)
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

