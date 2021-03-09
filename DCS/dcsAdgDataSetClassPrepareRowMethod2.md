---
title: AdgDataSet.PrepareRow(string)

Id: dcsAdgDataSetClassPrepareRowMethod2
TocParent: dcsAdgDataSetClassPrepareRowMethodMain
TocOrder: 1

---

Create a **DataRow** object in preparation for adding it to the **AdgDataSet** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public  PrepareRow(
   string strFormat
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function PrepareRow( _
   ByVal strFormat As String _
) As** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc PrepareRow Access(*Public) Type()
   DclSrParm strFormat Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
          <span> *strFormat* 
          </span>
        </dt>
        <dd>
          <span/>A string identifying the format corresponding to the **DataTable**  to which the created **DataRow**  can be 
						added.
					</dd>
</dl>

Return Value

A new **System.Data.DataRow** object corresponding to *strFormat* , with column data initialized to default values.
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

Adding **DataRow** objects to **AdgDataSet** is generally a three step process. In the first step a **DataRow** object is established as the "prepared row". Secondly, fields represented in the **DataRow** columns are set to appropriate values. Finally, the **DataRow** is added to the **DataTable** . **PrepareRow** performs the first step by creating the **DataRow** object.

The **DataRow** object returned by this method is not a member of the **DataTable** corresponding to the format specified, until it has been explicitly inserted via [ AddPreparedRowAndSetActive](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html), [ FileAdapter.AddRecord](dcsFileAdapterClassAddRecordMethod.html), or a method of **DataTable** .

Column data of the **DataRow** object returned by this method is initialized with the value of the **DefaultValue** property of the corresponding **DataColumn** . When an **AdgDataSet** is constructed (for example, by the [FileAdapter.OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html) method), **DataColumn** objects are created to represent the fields of a record format. If a field is capable of containing "null" data (null-capable), the **DefaultValue** of that **DataColumn** is set to **System.DBNull.Value** . Otherwise, the **DefaultValue** is set to a reasonable "zero value" for the data type representing the field. The following table summarizes format field types, their corresponding natural .NET type representations, and the **DefaultValue** property contents used to initialize the column data in **PrepareRow** .
<br />

<table class="dtTABLE" id="Table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 19.99%" />
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 40%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
											Database Field DataTypes or null-capable
										</th>
            <th colspan="1" rowspan="1">
											DataColumn<br />
											.DataType
										</th>
            <th colspan="1" rowspan="1">
											DataColumn<br />
											.DefaultValue
										</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Binary
										</td>
            <td colspan="1" rowspan="1">System.Decimal
										</td>
            <td colspan="1" rowspan="1">0
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Boolean
										</td>
            <td colspan="1" rowspan="1">System.Boolean
										</td>
            <td colspan="1" rowspan="1">False
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Char
										</td>
            <td colspan="1" rowspan="1">System.String
										</td>
            <td colspan="1" rowspan="1">"" (an empty string of length zero)
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Date
										</td>
            <td colspan="1" rowspan="1">System.DateTime
										</td>
            <td colspan="1" rowspan="1">System.DateTime.MinValue
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.DBCS
										</td>
            <td colspan="1" rowspan="1">System.String
										</td>
            <td colspan="1" rowspan="1">"" (an empty string of length zero)
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Float
										</td>
            <td colspan="1" rowspan="1">System.Decimal
										</td>
            <td colspan="1" rowspan="1">0
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Hex
										</td>
            <td colspan="1" rowspan="1">Array of System.Byte
										</td>
            <td colspan="1" rowspan="1">Array of length N, where N is the length in bytes of the field; each element is 
											initialized to 0.
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Integer
										</td>
            <td colspan="1" rowspan="1">System.Int or System.Short
										</td>
            <td colspan="1" rowspan="1">0
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Packed
										</td>
            <td colspan="1" rowspan="1">System.Decimal
										</td>
            <td colspan="1" rowspan="1">0
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Time
										</td>
            <td colspan="1" rowspan="1">System.DateTime
										</td>
            <td colspan="1" rowspan="1">System.DateTime.MinValue
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Timestamp
										</td>
            <td colspan="1" rowspan="1">System.DateTime
										</td>
            <td colspan="1" rowspan="1">System.DateTime.MinValue
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">DataTypes.Zoned
										</td>
            <td colspan="1" rowspan="1">System.Decimal
										</td>
            <td colspan="1" rowspan="1">0
										</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">Any of the above types, null-capable
										</td>
            <td colspan="1" rowspan="1">As above
										</td>
            <td colspan="1" rowspan="1">System.DBNull.Value
										</td>
          </tr>
</table>

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
      [OpenNewAdgDataSet Method](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
      <br />
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

