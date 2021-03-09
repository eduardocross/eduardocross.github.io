---
title: FileAdapter.Dispose Method

Id: dcsFileAdapterClassDisposeMethod
TocParent: dcsFileAdapterMethods
TocOrder: 9

keywords: database files, close and release unmanaged resources
keywords: files, close and release unmanaged resources
keywords: close files and release unmanaged resources
keywords: how to, close files and release unmanaged resources
keywords: resources, release unmanaged
keywords: release unmanaged resources
keywords: unmanaged resources, release
keywords: release, unmanaged resources
keywords: Dispose method
keywords: FileAdapter.Dispose method

---

Releases unmanaged resources and closes the currently open file (synonymous with [Close](dcsFileAdapterClassCloseMethod.html)).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public virtual new Dispose();** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Overridable NotOverridable Dispose()** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr Dispose Modifier(*Overrides) Access(*Public)** 
      </pre>

Exceptions

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
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

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the **dgException.Error** property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of dgException.Error
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

The database server encountered a system error. Details may be available via the SystemError and Text fields of dgException.
</td>
          </tr>
</table>

Remarks

Use the **Close** or **Dispose** methods to close a file opened by a previous call to one of the 'open' methods ([Open](dcsFileAdapterClassOpenMethod.html) and [OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)). After a successful **Close** or **Dispose** call, the file may be subsequently reopened using the same **FileAdapter** object’s open methods.

**Dispose** and **Close** also release unmanaged resources associated with the **FileAdapter** , which allow the object to be safely finalized.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [Close Method](dcsFileAdapterClassCloseMethod.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [OpenNewAdgDataSet Method](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

