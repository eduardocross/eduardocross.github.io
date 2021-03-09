---
title: FileAdapter.DeleteRRN Method

Id: dcsFileAdapterClassDeleteRRNMethod
TocParent: dcsFileAdapterMethods
TocOrder: 8

keywords: database files, delete record by RRN
keywords: files, delete record by RRN
keywords: relative record numbers, delete records by
keywords: RRN, delete records by
keywords: records, delete by RRN
keywords: delete records in a file by RRN
keywords: how to, delete record by RRN
keywords: DeleteRRN method
keywords: FileAdapter.DeleteRRN method

---

Deletes the current record specified by relative record number.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public void DeleteRRN(
   long RRN
);** 
      </pre>
      <pre class="prettyprint">      <span class="lang">[Visual Basic] </span>
 **Public Sub DeleteRRN( _
   ByVal RRN As Long _
)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr DeleteRRN Access(*Public)
   DclSrParm RRN Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
 *RRN* 
        </dt>
        <dd>The relative record number of the record to delete.
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

FileAdapter [open](dcsFileAdapterClassOpenMethod.html) method has not been called (file is not open).
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

dgEsAS400ERROR
</td>
            <td colspan="1" rowspan="1">

The database server encountered a system error. Details may be available via the SystemError and Text fields of dgException.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOTFND
</td>
            <td colspan="1" rowspan="1">

A record with the specified key could not be found.
</td>
          </tr>
</table>

Remarks

**DeleteRRN** deletes a record in the open file containing a specified relative record number. First, a search for a record containing the relative record number is performed. If such a record is not found, the method throws dgException, with an Error number indicating the condition (see Exceptions above). If the record is found, it is set to be the current record of the file, and subsequently deleted.

The file should be opened with the [ AccessMode](dcsFileAdapterClassAccessModeProperty.html) property set to a value including the [AccessMode.Delete](dcsAccessModeEnumeration.html) flag, in order to permit delete access to the file.
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
      [AccessMode Property](dcsFileAdapterClassAccessModeProperty.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [AccessMode Enumeration](dcsAccessModeEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

