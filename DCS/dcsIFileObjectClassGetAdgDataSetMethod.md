---
title: IFileObject.GetAdgDataSet Method

Id: dcsIFileObjectClassGetAdgDataSetMethod
TocParent: dcsIFileObjectMethods
TocOrder: 1

keywords: GetAdgDataSet method
keywords: IFileObject.GetAdgDataSet method
keywords: DataSetOptions enumeration, used by
keywords: enumerations [DCS 16.0 DataSetOptions, used by

---

**GetAdgDataSet** method returns an instance of an [AdgDataSet](dcsAdgDataSetClass.html) modeling the formats of the database file represented by **IFileObject** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public AdgDataSet GetAdgDataSet(
    [DataSetOptions](dcsDataSetOptionsEnumeration.html) opts
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub GetAdgDataSet(_
   ByVal opts As [DataSetOptions](dcsDataSetOptionsEnumeration.html)<br /> ) As AdgDataSet** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc GetAdgDataSet Access(*Public) Type(AdgDataSet)<br />     DclSrParm opts Type([DataSetOptions](dcsDataSetOptionsEnumeration.html))** 
      </pre>

Parameters

<dl>
        <dt>
 *opts* 
        </dt>
        <dd>

[DataSetOptions](dcsDataSetOptionsEnumeration.html). Optional effects on **DataSet** and **AdgDataSet** creation.
</dd>
</dl>

#### Returns
**AdgDataSet** . **GetAdgDataSet** creates a new instance of **AdgDataSet** and customizes it to reflect the formats of the file.
Exceptions

<br />

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
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

dgException 
</td>
            <td colspan="1" rowspan="1">

See table below. 
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
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

dgEINVARG 

</td> <td colspan="1" rowspan="1"> <p>The path name referenced by this IFileObject instance does not locate a valid database object. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmFNOTFND 
</td>
            <td colspan="1" rowspan="1">

The path name referenced by this IFileObject instance locates a valid database object but the object is not a file. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExMISSING 
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support discovered a registration for an exit point validation routine for the method but the validation routine itself was not found. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExINVLIC 
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support encountered an exit point validation routine for the method but the license for this support is invalid or not found. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExDENIED 
</td>
            <td colspan="1" rowspan="1">

Access to the method was denied by the database provider's "exit point" security support. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOMEM 
</td>
            <td colspan="1" rowspan="1">

The database provider encountered an "out of memory" condition. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOOBJAUTH 
</td>
            <td colspan="1" rowspan="1">

The current session does not have "operational" authority to the file. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErADENOTFND, dgEcNEWVERSION, or dgEaBADFRMTID 
</td>
            <td colspan="1" rowspan="1">

The database provider has detected an inconsistency in the file. The file should be repaired or restored. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnOpenFileDef 
</td>
            <td colspan="1" rowspan="1">

The database provider encountered a system error when attempting to access the file's definition. The file's type may not be supported by DataGate. Please see the provider's event log for further details. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR 
</td>
            <td colspan="1" rowspan="1">

The database provider encountered a system-level error. Details provided in the **dgException.Message** property. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcSQL400FILE 
</td>
            <td colspan="1" rowspan="1">

The database provider detected that the file's type is "SQL/400". DCS does not currently support this type of file. 
</td>
          </tr>
</table>

Remarks

This method, and [FileAdapter.OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html) return an instance of [AdgDataSet](dcsAdgDataSetClass.html) with **System.Data.DataSet** structures matching the formats of a database file. **GetAdgDataSet** , unlike **OpenNewAdgDataSet,** does not open the file for record access. The **AdgDataSet** returned by this method is suitable for subsequently opening for record access of the file represented by **IFileObject** , with the [FileAdapter.Open](dcsFileAdapterClassOpenMethod.html) method.

*opts* controls the construction of the **AdgDataSet** instance including whether or not to create **DataTable** objects representing file keys.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [IFileObject Class Members](dcsIFileObjectMembers.html)
      <br />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [File Adapter Class](dcsFileAdapterClass.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [OpenNewAdgDataSet Method](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
      <br />
      [DataSetOptions Enumeration](dcsDataSetOptionsEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

