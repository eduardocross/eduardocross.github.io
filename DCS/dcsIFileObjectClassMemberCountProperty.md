---
title: IFileObject.MemberCount Property

Id: dcsIFileObjectClassMemberCountProperty
TocParent: dcsIFileObjectProperties
TocOrder: 0

keywords: MemberCount property
keywords: IFileObject.MemberCount property
keywords: number of, database file members in database file
keywords: database files, number of database file members
keywords: how to, determine number of database file members in database file
keywords: database file members, number of in database file

---

**MemberCount** is the number of database member objects in the file represented by **IFileObject** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public int MemberCount { get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property MemberCount As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp MemberCount Access(*Public) Type(*Integer) Len(4)
   BegGet** 
      </pre>

Property Value <p> **System.Int32** . Read-only. A non-negative value reflecting the number of database member objects contained by the file. 
Exceptions

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

<br /> <table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells"> <colgroup span="1"> <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" /> <col span="1" style="WIDTH: 70%" /> </colgroup> <tr> <th colspan="1" rowspan="1"> Value of dgException.Error </th> <th colspan="1" rowspan="1"> Condition </th> </tr> <tr> <td colspan="1" rowspan="1"> <p>dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

The path name referenced by this IFileObject instance does not locate a valid database object. 
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

The current session does not have any of the following authorities to the file: "read," "add," "delete," or "update". 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ 
</td>
            <td colspan="1" rowspan="1">

The database provider could not obtain a "shared read" lock on the file object. 
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

A database file object may contain zero or more database member objects. **MemberCount** is the number of member objects currently contained by a database file. The value of **MemberCount** is equal to the number of elements of the array value of the [ Members](dcsIFileObjectClassMembersProperty.html) property.

Currently, DCS retrieves the value of **MemberCount** from the database provider only once in the lifetime of **IFileObject** , and this value is returned each time the property value is accessed. Thus, the listed exceptions are never raised after the first successful access of the property value. To obtain a refreshed value for **MemberCount** , use a newly instantiated **IFileObject** instance referencing the same database file object.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IFileObject Class](dcsIFileObjectClass.html) <br />[Members Property](dcsIFileObjectClassMembersProperty.html) <br />[ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html) 

