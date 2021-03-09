---
title: AdgDataSet.AddRow(integer)

Id: dcsAdgDataSetClassAddRowMethod1
TocParent: dcsAdgDataSetClassAddRowMethods
TocOrder: 0

---

Add a prepared row to the table for a particular format.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void AddRow(
   int iFormat
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub AddRow(
   ByVal iFormat As Integer
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr AddRow Access(*Public)
   DclSrParm iFormat Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
 *iFormat* 
        </dt>
        <dd>

The zero-relative index of the format corresponding to the table to which the prepared row will be added. A suitable value for *iFormat* could be passed to the [GetFormatName](dcsAdgDataSetClassGetFormatNameMethod.html) method to obtain the format name.
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

There is no prepared row to set active. **PrepareRow** should be called first to create a prepared row.
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

<span> **AddRow** </span> appends a prepared row to the table specified by *<span>i</span><span>Format</span>* . A prepared row can be created, or an existing DataRow can be set as a prepared row, using one of the [PrepareRow](dcsAdgDataSetClassPrepareRowMethodMain.html) methods of **AdgDataSet.** 

The usual pattern of use involves first staging the prepared DataRow object via <span> **PrepareRow** </span>, setting the field values in the DataRow as necessary, then calling <span> **AddRow** </span> or [AddPreparedRowAndSetActive](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html) to append the row to the table.

<span>Note</span> that prior to calling this method, you must call <span> **PrepareRow** </span> to stage a prepared row for insertion to the table. Also, upon return from this method, the prepared row of the table remains the row added to the table. Calling **AddRow** or <span> **AddPreparedRowAndSetActive** </span> again before calling <span> **PrepareRow** </span> will cause an exception.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      <span>
        [AdgDataSet Class](dcsAdgDataSetClass.html)
        <br />
        [AdgDataSet Class Members](dcsAdgDataSetMembers.html)
        <br />
        [AddPreparedRowAndSetActive 
						Method](dcsAdgDataSetClassAddRowMethod.shtm">AddRow Method</a>
        <br />
        <a href="dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html)
        <br />
        [GetFormatName Method](dcsAdgDataSetClassGetFormatNameMethod.html)
        <br />
        [PrepareRow Method](dcsAdgDataSetClassPrepareRowMethod2.html)
      </span>
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

