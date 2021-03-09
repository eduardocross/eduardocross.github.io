---
title: AdgConnection.BeginAutoTransaction(String, String)

Id: dcsAdgConnectionClassBeginAutoTransactionMethod3
TocParent: dcsAdgConnectionClassBeginAutoTransactionMethodMain
TocOrder: 0

---

Begins an automatic database transaction creating an instance of an [IAdgTransaction](dcsIAdgTransactionClass.html) object with the name and options specified.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public IAdgTransaction BeginAutoTransaction(
   string Name,
   string Options
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function BeginAutoTransaction( _
   ByVal Name As String _
   ByVal Options As String _
) As [IAdgTransaction](dcsIAdgTransactionClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc BeginAutoTransaction Access(*Public) Type(IAdgTransaction)
   DclSrParm Name Type(*String)
   DclSrParm Options Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *Name* 
        </dt>
        <dd>An arbitrary string naming the transaction. </dd>
        <dt>
 *Options* 
        </dt>
        <dd>A string containing database provider platform-dependent command options for 
								initiating the transaction. Otherwise, the empty string or a null reference.
							</dd>
</dl>

Return Value

**IAdgTransaction** . An automatic transaction object associated with the database connection.
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

This method begins an *automatic transaction* for those database providers that support transaction processing. The returned **IAdgTransaction** object representing the transaction is associated with the database connection of [AdgConnection](dcsAdgConnectionClass.html). This version of **BeginAutoTransaction** produces a transaction where the [ TransactionLevel](dcsIAdgTransactionClassTransactionLevelProperty.html) property of the returned **IAdgTransaction** object has the value [TransactionLevel.Medium](dcsTransactionLevelEnumeration.html).

An automatic transaction (as initiated by **BeginAutoTransaction** ) is distinguished from a manual transaction (as initiated by the [ BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html) methods) by the behaviors of the [ IAdgTransaction.Commit](dcsIAdgTransactionClassCommitMethods.html) method and [ IAdgTransaction.Rollback](dcsIAdgTransactionClassRollbackMethod.html) methods. **Commit** and **Rollback** result in the acceptance and cancellation, respectively, of accumulated database modifications within the current transaction's boundaries. In an automatic transaction, these methods also result in the end of the current transaction followed by the immediate creation of a new transaction under the control of **IAdgTransaction** . Thus, the behavior of an automatic transaction is similar to the behavior of an IBM i database transaction for all database provider platforms. 

Automatic transactions can be used when an application expects the behavior of **IAdgTransaction** to be uniform regardless of the transaction-enabled database provider in use. However, note that at the time of this writing, only the IBM i database provider is transaction-enabled. For future multi-platform compatibility, use of automatic transactions is recommended. For the finest level of control over each transaction, use of manual transactions is recommended (see **BeginTransaction** ).

*Name* may be used by the database provider to identify transaction resources. *Name* initializes the [ Name](dcsIAdgTransactionClassNameProperty.html) property of the **IAdgTransaction** object returned. Specifying the empty string or a null reference for *Name* results in an anonymous transaction.

*Options* specifies command options for initiating the new **IAdgTransaction** object specific to the database provider. For example, transactions on IBM i database providers are initiated via the "STRCMTCTL" CL command, with the "LCKLVL", "TEXT", and "CMTSCOPE(*JOB)" parameters. Other parameters not specified by DCS, such as "NFYOBJ" and "DFTJRN", may be specified via *Options* (e.g. "NFYOBJ(MYLIB/MYOBJ *MSGQ) DFTJRN(MYLIB/MYJRN)" ). If other command options are not required, specify the empty string or null reference for *Options* . Note that non-empty string values for *Options* may defeat the multi-platform compatibility provided by automatic transactions. In an automatic transaction, the value of *Options* is used for each new transaction created by **Commit** and **Rollback** .
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
      [BeginTransaction 
					Method](dcsAdgConnectionClassBeginTransactionMethodMain.html)
      <br />
      [IAdgTransaction Class](dcsIAdgTransactionClass.html)
      <br />
      [Commit Method](dcsIAdgTransactionClassCommitMethods.html)
      <br />
      [Name Property](dcsIAdgTransactionClassNameProperty.html)
      <br />
      [Rollback Method](dcsIAdgTransactionClassRollbackMethod.html)
      <br />
      [TransactionLevel 
					Property](dcsIAdgTransactionClassTransactionLevelProperty.html)
      <br />
      [ASNA.DataGate.Common.TransactionLevel 
					Enumeration](dcsTransactionLevelEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

