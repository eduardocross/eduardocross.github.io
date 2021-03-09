---
title: AdgDataSet.PrepareRow(string, System.Data.DataRow)

Id: dcsAdgDataSetClassPrepareRowMethod3
TocParent: dcsAdgDataSetClassPrepareRowMethodMain
TocOrder: 2

keywords: DataRow objects, prepare existing object to be inserted into DataTable
keywords: how to, prepare existing DataRow object for insertion into DataTable

---

Establish an existing **DataRow** object as the currently prepared row, for subsequently adding it to the **AdgDataSet** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void PrepareRow(
   string strFormat,
   DataRow row
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub PrepareRow( _
   ByVal strFormat As String, _
   ByVal row As DataRow
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr PrepareRow Access(*Public)
   DclSrParm strFormat Type(*String)
   DclSrParm row Type(DataRow)** 
      </pre>

Parameters

<dl>
        <dt>
 *strFormat* 
        </dt>
        <dd>A string identifying the format corresponding to the **DataTable**  
						to which the **DataRow**  can be added. </dd>
        <dt>
 *row* 
        </dt>
        <dd>A **DataRow**  object to be set as the currently prepared row.</dd>
</dl>

Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
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

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

Can occur if *strFormat* specifies an invalid format name.
</td>
          </tr>
</table>

Remarks

Adding **DataRow** objects to **AdgDataSet** is generally a three step process. In the first step a **DataRow** object is established as the "prepared row". Secondly, fields represented in the **DataRow** columns are set to appropriate values. Finally, the **DataRow** is added to the **DataTable** .

This version of **PrepareRow** stages a pre-existing **DataRow** object, rather than creating a new one. Since a valid **DataRow** is not created, care should be taken to ensure that *row* is a valid **DataRow** object for the record format corresponding to *strFormat* . A valid **DataRow** may be obtained from one of the other versions of **PrepareRow** or from .NET framework methods in the **System.Data** namespace.

The **DataRow** object returned by this method is not a member of the **DataTable** corresponding to the format specified, until it has been explicitly inserted via [ AddPreparedRowAndSetActive](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html), [ FileAdapter.AddRecord](dcsFileAdapterClassAddRecordMethod.html), or a method of **DataTable** .

Note that **PrepareRow** performs no validation of the *strFormat* parameter.
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
      [AddPreparedRowAndSetActive 
					Method](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [AddRecord Method](dcsFileAdapterClassAddRecordMethod.html)
      <br />
      [ASNA.DataGate.Client 
					Namespace](dcsDataGateClientNamespace.html)

