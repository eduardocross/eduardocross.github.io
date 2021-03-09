---
title: FileAdapter.ChangeRRN Method

Id: dcsFileAdapterClassChangeRRNMethod
TocParent: dcsFileAdapterMethods
TocOrder: 2

keywords: RRN, updating records by
keywords: relative record numbers, update records by
keywords: records, update by RRN
keywords: update, record by RRN
keywords: update record by RRN
keywords: how to, update record by RRN
keywords: database files, update record by RRN
keywords: files, update record by RRN
keywords: ChangeRRN method
keywords: FileAdapter.ChangeRRN method

---

Updates the database file record specified by relative record number with the contents of the specified [AdgDataSet.ActiveRow ](dcsAdgDataSetClassActiveRowProperty.html)property.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public void ChangeRRN(
   [AdgDataSet](dcsAdgDataSetClass.html) ds,
   long RRN
);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub ChangeRRN( _
   ByVal ds As [AdgDataSet](dcsAdgDataSetClass.html) _
   ByVal RRN As Long _
)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr ChangeRRN Access(*Public)
   DclSrParm ds Type([AdgDataSet](dcsAdgDataSetClass.html))
   DclSrParm RRN Type(*Integer) Len(8)** 
      </pre>

Parameters

<dl>
        <dt>
 *ds* 
        </dt>
        <dd>The DataSet object ( **ASNA.DataGate.Client.AdgDataSet**  ) used to 
						update the database file record. </dd>
        <dt>
          <span> *RRN* 
          </span>
        </dt>
        <dd>
          <span />
          <span>The relative
 record number of the record to change.</span>
        </dd>
</dl>

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

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

FileAdapter open method has not been called (file is not open).
</td>
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

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
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

dgEmINV400OP
</td>
            <td colspan="1" rowspan="1">

This method was performed using a connection to an IBM i database provider but the IBM i provider does not support this method.
</td>
          </tr>
</table>

Remarks

<span> **ChangeRRN** </span> is similar to [ChangeCurrent](dcsFileAdapterClassChangeCurrentMethod.html) , which updates database file records. Whereas <span> **ChangeCurrent** </span> allows the current record to be updated, <span> **ChangeRRN** </span> permits update to a record with a specified relative record number.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />
      <span>
        [FileAdapter Class](dcsFileAdapterClass.html) <br />[
						FileAdapter Members](dcsFileAdapterMembers.html)<br />[FileAdapter.ChangeCurrent Method](dcsFileAdapterClassChangeCurrentMethod.html)</span>

