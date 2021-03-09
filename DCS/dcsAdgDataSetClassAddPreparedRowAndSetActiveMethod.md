---
title: AddPreparedRowAndSetActive

Id: dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod
TocParent: dcsAdgDataSetMethods
TocOrder: 0

keywords: database files, index value of
keywords: files, index value of
keywords: index value of database file
keywords: rows, set current record active and add to a table
keywords: set current record active and add row to a table
keywords: how to, set current record active and add row to a table
keywords: tables, set current record active and add row to
keywords: AddPreparedRowandSetActive method
keywords: AdgDataSet.AddPreparedRowandSetActive method

---

An integer containing the index value of the file.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public bool AddPreparedRowAndSetActive(
   int iFormat
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function AddPreparedRowAndSetActive( _
   ByVal iFormat As Integer _
) As Boolean** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc AddPreparedRowAndSetActive Access(*Public) Type(*Boolean)
   DclSrParm iFormat Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
          <span> *iFormat* 
          </span>
        </dt>
        <dd>
          <span>The zero-relative index of 
  the format corresponding to the table to which the prepared row will be added. 
   A suitable value for<span> *iFormat* </span> could be passed to the [
								GetFormatName](dcsAdgDataSetClassGetFormatNameMethod.html) 
  method to obtain the format name.</span>
        </dd>
</dl>

Return 
Value

<span><span> **True** </span> if the specified row is set as active and ready for data.</span> 
Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
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

The addition tries to put a null in a DataColumn where AllowDBNull is false. 
</td>
          </tr>
</table>

Remarks

**AddPreparedRowAndSetActive** combines the operations performed by the [AddRow](dcsAdgDataSetClassAddRowMethods.html) and [SetActive](dcsAdgDataSetClassSetActiveMethods.html) methods into a single method call. First, a prepared row is added to the specified format table, just as if **AddRow** ( *iFormat* ) had been called. Then the row just added to the table is set to be the [ ActiveRow](dcsAdgDataSetClassActiveRowProperty.html) for the **AdgDataSet** , like using **SetActive** . This is useful when adding a record format that is to be immediately used in a [ FileAdapter](dcsFileAdapterClass.html) method which operates upon the **ActiveRow** , such as [AddRecord](dcsFileAdapterClassAddRecordMethod.html).

The usual pattern of use involves first staging the prepared DataRow object via [PrepareRow](dcsAdgDataSetClassPrepareRowMethodMain.html) setting the field values in the DataRow as necessary, then calling <span> **AddRow** </span> or <span> **AddPreparedRowAndSetActive** </span> to append the row to the table.

<span>Note</span> that prior to calling this method, you must call <span> **PrepareRow** </span> to stage a prepared row for insertion to the table. Also, upon return from this method, the prepared row of the table remains the row added to the table. Calling <span> **AddRow** </span> or <span> **AddPreparedRowAndSetActive** </span> again before calling <span> **PrepareRow** </span> will cause an exception.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Class Members](dcsAdgDataSetMembers.html)
      <br />
      [AddRow Method](dcsAdgDataSetClassAddRowMethods.html)
      <br />
      [ActiveRow Method](dcsAdgDataSetClassActiveRowProperty.html)
      <br />
      [GetFormatName Method](dcsAdgDataSetClassGetFormatNameMethod.html)
      <br />
      [SetActive Method](dcsAdgDataSetClassSetActiveMethods.html)
      <br />
      [PrepareRow Method](dcsAdgDataSetClassPrepareRowMethodMain.html)
      <br />
      [FileAdapter.AddRecord Method](dcsFileAdapterClassAddRecordMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

