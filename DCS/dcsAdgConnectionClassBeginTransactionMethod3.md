---
title: AdgConnection.BeginTransaction(String)

Id: dcsAdgConnectionClassBeginTransactionMethod3
TocParent: dcsAdgConnectionClassBeginTransactionMethodMain
TocOrder: 0

---

Begins a manual database transaction creating an instance of an [ IAdgTransaction](dcsIAdgTransactionClass.html) object with the name specified. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public IAdgTransaction BeginTransaction(
   string Name
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function BeginAutoTransaction( _
   ByVal Name As String
) As [IAdgTransaction](dcsIAdgTransactionClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc BeginAutoTransaction Access(*Public) Type(IAdgTransaction)
   DclSrParm Name Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *Name* 
        </dt>
        <dd>A string naming the transaction.
					</dd>
</dl>

Return Value

**IAdgTransaction** . A manual transaction object associated with the database connection.
Exceptions

**ASNA.DataGate.Common.dgException** is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of
							<br />
							dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR
</td>
            <td colspan="1" rowspan="1">

The database server encountered a system error. Details are available via the SystemError and Text fields of [dgException](dcsdgExceptionClass.html). For IBM i database providers, further details are available in the job log corresponding to the database connection.
</td>
          </tr>
</table>

Remarks

This method begins a *manual transaction* for those database providers that support transaction processing. The returned **IAdgTransaction** object representing the transaction is associated with the database connection of [AdgConnection](dcsAdgConnectionClass.html).

A manual transaction (as initiated by **BeginTransaction** ) is distinguished from an automatic transaction (as initiated by the [ BeginAutoTransaction](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) methods) by the behaviors of the [ IAdgTransaction.Commit](dcsIAdgTransactionClassCommitMethods.html) and [ IAdgTransaction.Rollback](dcsIAdgTransactionClassRollbackMethod.html) methods. **Commit** and **Rollback** result in the acceptance and cancellation, respectively, of accumulated database modifications within the current transaction's boundaries. In an automatic transaction, these methods also result in the end of the current transaction followed by the immediate creation of a new transaction under the control of **IAdgTransaction** . Thus, the behavior of an automatic transaction is similar to the behavior of an IBM i database transaction for all database provider platforms.

Manual transactions should be used when an application requires a high degree of control over the transaction. Manual transactions can only be initiated with the **BeginTransaction** method. Further, manual transactions are not automatically renewed by DCS in the **Commit** and **Rollback** methods, as automatic transactions are. When multi-platform compatibility is of greater concern, use of automatic transactions is recommended (see **BeginAutoTransaction** ). For the finest level of control over each transaction, use of manual transactions is recommended.

*Name* may be used by the database provider to identify transaction resources. *Name* initializes the [ Name](dcsIAdgTransactionClassNameProperty.html) property of the **IAdgTransaction** object returned. Specifying the empty string or a null reference for *Name* results in an anonymous transaction.

The value of the [ TransactionLevel](dcsIAdgTransactionClassTransactionLevelProperty.html) property of the **IAdgTransaction** object returned is [TransactionLevel.Medium](dcsTransactionLevelEnumeration.html).
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

[AdgConnection Class](dcsAdgConnectionClass.html) <br /> [AdgConnection Class Members](dcsAdgConnectionMembers.html) <br /> [BeginAutoTransaction Method](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) <br /> [IAdgTransaction Class](dcsIAdgTransactionClass.html) <br /> [IAdgTransaction Class Commit Method](dcsIAdgTransactionClassCommitMethods.html) <br /> [IAdgTransaction Class Name Property](dcsIAdgTransactionClassNameProperty.html) <br /> [IAdgTransaction Class Rollback Method](dcsIAdgTransactionClassRollbackMethod.html) <br /> [IAdgTransaction Class TransactionLevel Property](dcsIAdgTransactionClassTransactionLevelProperty.html) <br /> [ASNA.DataGate.Common.TransactionLevel Enumeration](dcsTransactionLevelEnumeration.html) <br /> [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html) 
