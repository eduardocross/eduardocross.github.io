---
title: IAdgTransaction.Rollback Method

Id: dcsIAdgTransactionClassRollbackMethod
TocParent: dcsIAdgTransactionMethods
TocOrder: 1

keywords: Rollback method
keywords: IAdgTransaction.Rollback method

keywords: database transactions, cancel database changes within current context
keywords: manual transactions, cancel database changes within current context
keywords: automatic transactions, cancel database changes within current context and begin new

---

Cancel changes to the database that have been performed within the current transaction context.
<pre>
        <span class="lang">[C#]</span>
 **Public virtual void Rollback();** 
      </pre>
      <pre>
        <span class="lang">[Visual Basic] </span>
 **Public NotOverridable Sub Rollback()** 
      </pre>
      <pre>
        <span class="lang">[Visual RPG]</span>
 **BegSub Rollback Access(*Public) Modifier(*NotOverridable)** 
      </pre>

Exceptions

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="30%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type</th>
            <th colspan="1" rowspan="1">
							Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException 
</td>
            <td colspan="1" rowspan="1">

See table below. 
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="20%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1" style="height: 23px">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1" style="height: 23px">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEccIORECERR
</td>
            <td colspan="1" rowspan="1">

Recoverable I/O error occurred in commit/rollback operation. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEccIORECERR
</td>
            <td colspan="1" rowspan="1">

Unrecoverable I/O error occurred in commit/rollback operation. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEUNKNOWN 
</td>
            <td colspan="1" rowspan="1">

An unknown error (unpublished by the data provider) occurred. 
</td>
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

**Rollback** is used to cancel any changes that have occurred, via [Connection](dcsIAdgTransactionClassConnectionProperty.html), within the current transaction. Database providers may implement other related platform-dependent side effects, such as repositioning file pointers and releasing record locks. Also, database providers may have restrictions on the number of times [ Commit](dcsIAdgTransactionClassCommitMethods.html) and/or **Rollback** may be invoked within a single transaction context. Please consult the database provider's documentation for details.

When invoked on the automatic transaction implementation of **IAdgTransaction** (see [AdgConnection.BeginAutoTransaction Method](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html)), **Rollback** also ends the current transaction context and automatically begins a new transaction context using the parameters of the preceding transaction. The new transaction is under the control of **IAdgTransaction** .
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
      [Commit Method](dcsIAdgTransactionClassCommitMethods.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [BeginAutoTransaction 
					Method](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

