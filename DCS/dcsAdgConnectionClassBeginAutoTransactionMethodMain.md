---
title: AdgConnection.BeginAutoTransaction Methods

Id: dcsAdgConnectionClassBeginAutoTransactionMethodMain
TocParent: dcsAdgConnectionMethodsMain
TocOrder: 0

keywords: BeginAutoTransaction methods
keywords: AdgConnection.BeginAutoTransaction methods
keywords: database transactions, begin automatic
keywords: database transactions, lock level set for automatic
keywords: database transactions, name set for automatic
keywords: database transactions, options set for automatic
keywords: automatic transactions, beginning
keywords: automatic transactions, lock level set
keywords: automatic transactions, name set
keywords: automatic transactions, options set
keywords: how to, begin automatic database transactions
keywords: how to, set automatic database transaction lock level
keywords: how to, set automatic database transaction name
keywords: how to, set automatic database transaction options

---

Overloaded method that begins an automatic database transaction creating an instance of an [IAdgTransaction](dcsIAdgTransactionClass.html) with combinations of transaction locking level, name, and command options parameters specified.
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 40%" />
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

[BeginAutoTransaction(TransactionLevel, string)](dcsAdgConnectionClassBeginAutoTransactionMethod1.html) 
</td>
            <td colspan="1" rowspan="1">

Begins an automatic database transaction creating an instance of an **IAdgTransaction** object with the options and lock levels specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[BeginAutoTransaction(TransactionLevel, string, string)](dcsAdgConnectionClassBeginAutoTransactionMethod2.html) 
</td>
            <td colspan="1" rowspan="1">

Begins an automatic database transaction creating an instance of an **IAdgTransaction** object with the name, options, and lock level specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[BeginAutoTransaction(string, string)](dcsAdgConnectionClassBeginAutoTransactionMethod3.html) 
</td>
            <td colspan="1" rowspan="1">

Begins an automatic database transaction creating an instance of an **IAdgTransaction** object with the name and options specified
</td>
          </tr>
</table>

See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgConnection Class Members](dcsAdgConnectionMembers.html)
      <br />
      [IAdgTransaction Class](dcsIAdgTransactionClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

