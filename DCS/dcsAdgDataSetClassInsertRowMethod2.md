---
title: AdgDataSet.InsertRow(string, integer)

Id: dcsAdgDataSetClassInsertRowMethod2
TocParent: dcsAdgDataSetClassInsertRowMethods
TocOrder: 1

---

Insert a record into the DataSet table for a particular format and relative record position.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void InsertRow(
   string strFormat,
   integer rrn
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub InsertRow( _
   ByVal strFormat As String _
   ByVal rrn As Integer
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr InsertRow Access(*Public)
   DclSrParm strFormat Type(*string) Len(45)
   DclSrParm rrn Type(*integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
 *strFormat* 
        </dt>
        <dd>

**String** . The name of the format corresponding to the table to which the prepared row will be added. Use the [ GetFormatName](dcsAdgDataSetClassGetFormatNameMethod.html) method to obtain the format name.
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

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
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

The value for *strFormat* specifies an invalid name. Use **GetFormatName** method to obtain the format name.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NoNullAllowedException
</td>
            <td colspan="1" rowspan="1">

The addition tries to put a null in a DataColumn where AllowDBNull is false.
</td>
          </tr>
</table>

Remarks

<span> **InsertRow** </span> inserts a prepared row into the table specified by *strFormat* at the position indicated by the *rrn* . A prepared row can be created using one of the [PrepareRow Method](dcsAdgDataSetClassPrepareRowMethodMain.html) methods of [AdgDataSet](dcsAdgDataSetClass.html).

The usual pattern of use involves first staging the prepared DataRow object via **PrepareRow** , setting the field values in the DataRow as necessary, then calling **InsertRow** to insert the row into the table.

Note that prior to calling this method, you must call **PrepareRow** to stage a prepared row for insertion to the table. Also, upon return from this method, the prepared row of the table remains the row added to the table. Calling **InsertRow** , [AddRow](dcsAdgDataSetClassAddRowMethods.html) or [AddPreparedRowAndSetActive](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html) again before calling **PrepareRow** will cause an exception.
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
      [AddRow Methods](dcsAdgDataSetClassAddRowMethods.html)
      <br />
      [PrepareRow Methods](dcsAdgDataSetClassPrepareRowMethodMain.html)
      <br />
      [AddPreparedRowAndSetActive 
					Method](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html)
      <br />
      [GetFormatName Method](dcsAdgDataSetClassGetFormatNameMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

