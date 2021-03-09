---
title: AdgConnection.BeginTransaction Methods

Id: dcsAdgConnectionClassBeginTransactionMethodMain
TocParent: dcsAdgConnectionMethodsMain
TocOrder: 1

keywords: BeginTransaction methods
keywords: AdgConnection.BeginTransaction methods
keywords: database transactions, begin manual
keywords: database transactions, lock level set for manual
keywords: database transactions, name set for manual
keywords: database transactions, options set for manual
keywords: manual transactions, beginning
keywords: manual transactions, lock level set
keywords: manual transactions, name set
keywords: manual transactions, options set
keywords: how to, begin manual database transactions
keywords: how to, set manual database transaction lock level
keywords: how to, set manual database transaction name
keywords: how to, set manual database transaction options

---

Overloaded method that begins a manual database transaction creating an instance of an [IAdgTransaction](dcsIAdgTransactionClass.html) object with combinations of transaction locking level, name, and command options parameters specified.
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 50%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Overload List
						</th>
            <th colspan="1" rowspan="1">
							Description
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[BeginTransaction(TransactionLevel)](dcsAdgConnectionClassBeginTransactionMethod1.html) 
</td>
            <td colspan="1" rowspan="1">

Begins a manual database transaction creating an instance of an **IAdgTransaction** object with lock level specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[BeginTransaction(TransactionLevel, string)](dcsAdgConnectionClassBeginTransactionMethod2.html) 
</td>
            <td colspan="1" rowspan="1">

Begins a manual database transaction creating an instance of an **IAdgTransaction** object with the name and lock level specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[BeginTransaction(TransactionLevel, string, string)](dcsAdgConnectionClassBeginTransactionMethod4.html) 
</td>
            <td colspan="1" rowspan="1">

Begins a manual database transaction creating an instance of an **IAdgTransaction** object with the name, lock level, and options specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[BeginTransaction(string)](dcsAdgConnectionClassBeginTransactionMethod3.html) 
</td>
            <td colspan="1" rowspan="1">

Begins a manual database transaction creating an instance of an **IAdgTransaction** object with the name specified.
</td>
          </tr>
</table>

See Also

[AdgConnection Class](dcsAdgConnectionClass.html) <br /> [AdgConnection Class Members](dcsAdgConnectionMembers.html) <br /> [IAdgTransaction Class](dcsIAdgTransactionClass.html) <br /> [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html) 
