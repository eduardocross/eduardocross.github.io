---
title: FileAdapter.ReuseRRN Method

Id: dcsFileAdapterClassReUseRRNMethod
TocParent: dcsFileAdapterMethods
TocOrder: 25

keywords: ReuseRRN method
keywords: FileAdapter.ReuseRRN method
keywords: database files, change deleted record status to undeleted and update by RRN
keywords: files, change deleted record status to undeleted and update by RRN
keywords: records, change deleted status to undeleted and update by RRN
keywords: relative record numbers, change record status and update by
keywords: how to, change deleted record status to undeleted and update by RRN

---

Change the status of a deleted record to undeleted and update its contents. 
<pre>        <span class="lang">[C#]</span>
 **Public void ReuseRRN(
   AdgDataSet ds,
   long RRN
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub ReuseRRN( _
   ByVal ds As [AdgDataSet](dcsAdgDataSetClass.html) _
   ByVal RRN As Long _
)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr ReuseRRN Access(*Public)
   DclSrParm ds Type(AdgDataSet)
   DclSrParm RRN Type(*Integer) Len(8)** 
      </pre>

Parameters

<dl>
        <dt>
 *ds* 
        </dt>
        <dd>The DataSet object ([AdgDataSet](dcsAdgDataSetClass.html)) containing 
						the updated record to be reused. </dd>
        <dt>
 *RRN* 
        </dt>
        <dd>		The relative record number of the record to reuse.
							</dd>
</dl>

Exceptions

<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
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

FileAdapter [Open](dcsFileAdapterClassOpenMethod.html) method has not been called (file is not open).
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

<table class="dtTABLE" id="table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The *RRN* specified is not valid.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOTUPD
</td>
            <td colspan="1" rowspan="1">

The file was not opened for update. To use **ReuseRRN** , the [ AccessMode](dcsFileAdapterClassAccessModeProperty.html) property must be set to a value which includes the [ AccessMode.Change](dcsAccessModeEnumeration.html) flag, prior to opening the file.
</td>
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

<span> **ReuseRRN** </span> updates the contents of the specified record of an open file and marks the record as undeleted.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [AccessMode Property](dcsFileAdapterClassAccessModeProperty.html)
      <br />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AccessMode Enumeration](dcsAccessModeEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

