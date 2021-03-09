---
title: IMember.ActiveRecords Property

Id: dcsIMemberClassActiveRecordsProperty
TocParent: dcsIMemberProperties
TocOrder: 0

keywords: ActiveRecords property
keywords: IMember.ActiveRecords property
keywords: number of, active records in database file member
keywords: database file members, number of active records in
keywords: database files, number of active records in database file member
keywords: how to, determine number of active records in database file member

---

The number of active records in the database file member object represented by **IMember** 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public long ActiveRecord { get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public ReadOnly Property ActiveRecord As Long** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp ActiveRecord Type(*long) Len(8) Access(*Public)
   BegGet** 
      </pre>

Property Value

**Integer** . Read-only. A non-negative value.
Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
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

The property values of this **IMember** are being accessed for the first time and the resulting query to the database provider caused an exception to occur. See table below. 
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
</td>
            <td colspan="1" rowspan="1">

The path name referenced by this **IMember** instance does not locate a valid database object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmMNOTFND 
</td>
            <td colspan="1" rowspan="1">

The path name referenced by this **IMember** instance may locate a valid database object but the object is not a member. 
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
</table>

Remarks

Use **ActiveRecords** to examine the number of active records contained in an existing member object. For a count of deleted records, use the [DeletedRecords](dcsIMemberClassDeletedRecordsProperty.html) property. 

The value of this read-only property is established only once in the lifetime of the **IMember** instance. Accesses of the property value after the first return a cached value which may not reflect intervening changes to the member object. To obtain a refreshed count, access the property value of a new instance of **IMember** . 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [DeletedRecords Property](dcsIMemberClassDeletedRecordsProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

