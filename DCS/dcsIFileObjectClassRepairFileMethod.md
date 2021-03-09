---
title: IFileObject.RepairFile Method

Id: dcsIFileObjectClassRepairFileMethod
TocParent: dcsIFileObjectMethods
TocOrder: 5

keywords: RepairFile method
keywords: IFileObject.RepairFile method
keywords: RepairOptions enumeration, used by
keywords: enumerations [DCS 16.0 RepairOptions, used by
keywords: AdgObserver delegate, used by
keywords: delegates [DCS 16.0 AdgObserver, used by
keywords: database files, repair single file
keywords: repair single database file
keywords: how to, repair database file
keywords: how to, invoke automatic diagnostic and repair function for a file

---

**RepairFile** repairs the database file represented by **IFileObject** as specified by [RepairOptions](dcsRepairOptionsEnumeration.html).
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void RepairFile(<br />[RepairOptions](dcsRepairOptionsEnumeration.html) repairOptions,
   [AdgObserver](dcsAdgObserverDelegate.html) observer
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub RepairFile(_
   ByVal repairOptions As [RepairOptions](dcsRepairOptionsEnumeration.html)_<br />   ByVal observer As [AdgObserver](dcsAdgObserverDelegate.html)<br /> ) As Void** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc RepairFile Access(*Public) Type(Void)<br />   DclSrParm repairOptions Type([RepairOptions](dcsRepairOptionsEnumeration.html))<br />   DclSrParm observer Type([AdgObserver](dcsAdgObserverDelegate.html))** 
      </pre>

Parameters

<dl>
        <dt />
</dl>

*repairOptions* 
<dl>
        <dd>

[RepairOptions](dcsRepairOptionsEnumeration.html). How files will be repaired.
</dd>
        <dt />
</dl>

*observer* 
<dl>
        <dd>

[AdgObserver](dcsAdgObserverDelegate.html). A delegate to provide the user with feedback in the form of text messges relating to the progress of the repair operation. Optionally specify a null reference here, if no feedback is desired.
</dd>
</dl>

Exceptions

<br />

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 22.18%; font-weigth: bold" />
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

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
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

The path name given for this IFileObject does not correspond to a database library. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOMEM 
</td>
            <td colspan="1" rowspan="1">

The database provider encountered an "out of memory" exception. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINV400OP
</td>
            <td colspan="1" rowspan="1">

The database provider does not support the automated diagnostic check and repair function.
</td>
          </tr>
</table>

Remarks

This method invokes the database provider's automated diagnostic check and repair function on a multiformat logical or physical file represented by **IFileObject** . A similar method, [IDirectory.RepairObjects](dcsIDirectoryClassRepairObjectsMethod.html) can be invoked for all files in a given library. Certain database providers recommend use of these methods as periodic maintenence, while others do not support them.

<p>Several options are available with *repairOptions* (see **RepairOptions** ). The optional delegate *observer* is called from **RepairFile** to report progress; if no such report is desired, specify a null reference.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span>
See Also

<dl />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [RepairObjects Method](dcsIDirectoryClassRepairObjectsMethod.html)
      <br />
      [RepairOptions Enumeration](dcsRepairOptionsEnumeration.html)
      <br />
      [AdgObserver Delegate](dcsAdgObserverDelegate.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

