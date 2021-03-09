---
title: AdgDataSet.InsertRow(integer, integer)

Id: dcsAdgDataSetClassInsertRowMethod1
TocParent: dcsAdgDataSetClassInsertRowMethods
TocOrder: 0

---

Insert a row into the Dataset table for a particular format and relative record position.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void InsertRow(
   int iFormat,<br />   int rrn
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub InsertRow(_
   ByVal iFormat As Integer_
   ByVal rrn as Integer
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr InsertRow Access(*Public)
   DclSrParm iFormat Type(*Integer) Len(4)
   DclSrParm rrn Type (*Integer) Len(45)** 
      </pre>

Parameters

<dl>
        <dt>
 *iFormat* 
        </dt>
        <dd>

**Int32** . The zero-relative index of the format corresponding to the table to which the prepared row will be added. A suitable value for *iFormat* could be passed to the [GetFormatName](dcsAdgDataSetClassGetFormatNameMethod.html) method to obtain the format name.
</dd>
        <dt>
 *rrn* 
        </dt>
        <dd>

**Int32** . A positive integer value reflecting the position of the record after insertion into the table. Specifying a value greater than the number of records in the table results in the record being appended to the end of the table.
</dd>
</dl>

Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 75%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
									Value of dgException.Error
								</th>
            <th colspan="1" rowspan="1">
									Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ArgumentNullException
</td>
            <td colspan="1" rowspan="1">

There is no prepared row to be inserted. **PrepareRow** should be called first to create a prepared row.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ArgumentException
</td>
            <td colspan="1" rowspan="1">

The prepared row either belongs to another table or already belongs to this table.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ConstraintException
</td>
            <td colspan="1" rowspan="1">

The addition invalidates a constraint.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

The value for *iFormat* specifies an invalid format index. Valid values can be passed to the **GetFormatName** method to obtain the format name.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NoNullAllowedException
</td>
            <td colspan="1" rowspan="1">

The addition tries to put a null in a DataColumn where AllowDBNull is false
</td>
          </tr>
</table>

Remarks

<span> **InsertRow** </span> inserts a prepared row to the table specified by *i* *Format* at the position indicated by the *rrn* . A prepared row can be created using one of the [ PrepareRow](dcsAdgDataSetClassPrepareRowMethodMain.html) methods of [AdgDataSet](dcsAdgDataSetClass.html). 

The usual pattern of use involves first staging the prepared DataRow object via <span> **PrepareRow** </span>, setting the field values in the DataRow as necessary, then calling <span> **InsertRow** </span> to insert the row into the table.

<span>Note</span> that prior to calling this method, you must call <span> **PrepareRow** </span> to stage a prepared row for insertion to the table. Also, upon return from this method, the prepared row of the table remains the row added to the table. Calling **InsertRow** , [ AddRow](dcsAdgDataSetClassAddRowMethods.html) or [AddPreparedRowAndSetActive](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html) again before calling **PrepareRow** will cause an exception.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Class Members](dcsAdgDataSetMembers.html)
      <br />
      [AddRow Method](dcsAdgDataSetClassAddRowMethods.html)
      <br />
      [PrepareRow Method](dcsAdgDataSetClassPrepareRowMethodMain.html)
      <br />
      [AddPreparedRowAndSetActive 
					Method](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html)
      <br />
      [GetFormatName Method](dcsAdgDataSetClassGetFormatNameMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

