---
title: IMember.Clear Method

Id: dcsIMemberClassClearMethod
TocParent: dcsIMemberMethods
TocOrder: 0

keywords: Clear method
keywords: IMember.Clear method
keywords: database file members, remove all active and deleted records
keywords: records, remove all active and deleted from database file member
keywords: records, active, remove from database file member
keywords: records, deleted, remove from database file member
keywords: database files, remove all active and deleted records in database file member
keywords: how to, remove all active and deleted records in database file member

---

**Clear** deletes all records in the member.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void Clear();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Sub Clear() As Void** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Clear Access(*Public) Type(Void)** 
      </pre>

Parameters

None.
Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1" style="height: 44px">
							Exception Type
						</th>
            <th colspan="1" rowspan="1" style="height: 44px">
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

<p>ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells"> <colgroup span="1"> <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" /> <col span="1" style="WIDTH: 70%" /> </colgroup> <tr> <th colspan="1" rowspan="1"> Value of dgException.Error </th> <th colspan="1" rowspan="1"> Condition </th> </tr> <tr> <td colspan="1" rowspan="1"> <p>dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The path name referenced by this **IMember** instance does not locate a valid database object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOLOCK, or dgEmBUSYOBJ 
</td>
            <td colspan="1" rowspan="1">

The database provider could not obtained the requisite lock(s) to perform this function, including an "exclusive" lock on the database member object. 
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

dgEaINVFTOP
</td>
            <td colspan="1" rowspan="1">

This method is not supported for the type of file containing the member object represented by **IMember** .
</td>
          </tr>
</table>

Remarks

**Clear** removes all data records, active and deleted, from the database file member object represented by **IMember** . DCS does not implement this function but rather invokes the database provider's function to perform the task.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span>
See Also

<dl />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

