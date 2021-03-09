---
title: FileAdapter.SeekRRN Method

Id: dcsFileAdapterClassSeekRRNMethod
TocParent: dcsFileAdapterMethods
TocOrder: 28

keywords: SeekRRN method
keywords: FileAdapter.SeekRRN method
keywords: SeekMode enumeration, used by
keywords: enumerations [DCS 16.0 SeekMode, used by
keywords: records, seeking by RRN
keywords: seeking, records randomly by RRN

---

Moves the record pointer associated with the currently open file without reading records by RRN.
<pre>        <span class="lang">[C#]</span>
 **Public void SeekRRN(
   SeekMode mode,
   Long RRN
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub SeekRRN( _
   ByVal mode As [SeekMode](dcsSeekModeEnumeration.html) _
   ByVal RRN As Long _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr SeekRRN Access(*Public)
   DclSrParm mode Type(SeekMode)
   DclSrParm RRN Type(*Integer) Len(8)** 
      </pre>
      <pre />

Parameters

<dl>
        <dt>
 *mode* 
        </dt>
        <dd>[ASNA.DataGate.Common.SeekMode](dcsSeekModeEnumeration.html). 
						Specifies the manner in which the record is to be located, relative to the 
						absolute positions in the file (First, Last) or relative to *RRN*  (Equal, 
						Greater, SetGT, SetGE, SetLL). </dd>
        <dt>
 *RRN* 
        </dt>
        <dd>		The relative record number of the record to seek.</dd>
</dl>

Exceptions

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="x-cell-content-align: Top" cellspacing="0">
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
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
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

dgEsAS400ERROR
</td>
            <td colspan="1" rowspan="1">

The database server encountered a system error. Details may be available via the SystemError and Text fields of dgException.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaEOF
</td>
            <td colspan="1" rowspan="1">

The record access operation resulted in an end-of-file condition.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOTFND
</td>
            <td colspan="1" rowspan="1">

The record specified by *RRN* was not found. It may have been deleted, it may never have existed, or the key may have been changed.
</td>
          </tr>
</table>

Remarks

**SeekRRN** positions the file pointer to a particular record using the specified relative record number ( *RRN* ) and *mode* as a point of reference. The record pointed to by this method will be either relative to the *RRN* parameter ( *mode* **Equal** , **Greater** , **SetGT** , **SetGE** , or **SetLL** ); or, relative to the absolute position in the file ( *mode* **First** or **Last** ). If the record sought does not exist in the file, the method throws dgException with an Error property value of dgEaNOTFND.

When **SeekMode.SetLL** or **SeekMode.SetGT** values for *mode* are specified and the record sought is not found, the file pointer is placed at the end of the file and then dgException is thrown.

Calling this method cancels "range mode". A prior successful call to [ReadRange](dcsFileAdapterClassReadRangeMethod.html) or [SeekRange](dcsFileAdapterClassSeekRangeMethod.html) places the **FileAdapter** in range mode, in which only records with keys in a specified range are accessed. This method cancels the restriction. 
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
      [Open Method](dcsFileAdapterClassOpenMethod.html) <br />
      [ReadRange 
					Method](dcsFileAdapterClassReadRangeMethod.html)<br />
	[SeekRange Method](dcsFileAdapterClassSeekRangeMethod.html)<br />
	[SeekMode Enumeration](dcsSeekModeEnumeration.html)<br />
	[ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

