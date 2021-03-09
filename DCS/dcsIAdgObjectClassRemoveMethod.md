---
title: IAdgObject.Remove Method

Id: dcsIAdgObjectClassRemoveMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 6

keywords: Remove method
keywords: IAdgObject.Remove method
keywords: database files, remove library objects from
keywords: database files, remove file member objects from
keywords: database files, remove from database
keywords: database libraries, remove from database
keywords: database file members, remove from database
keywords: how to, remove database library objects
keywords: how to, remove database file member objects
keywords: how to, remove database file objects
keywords: remove file objects from database
keywords: remove library objects from database

---

The **Remove** method removes an existing database object from the database.
<pre>        <span class="lang">[C#]</span>
 **Public void IAdgObject Remove();** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub Remove() As IAdgObject** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Remove Access(*Public) Type(IAdgObject)** 
      </pre>

Parameters

None.
Exceptions

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="30%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type</th>
            <th colspan="1" rowspan="1">
							Condition</th>
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

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="20%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
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

The path name specified when the **IAdgObject** instance was created does not reference an existing database object, or the method is not available for this object type. 
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

dgEmNOOBJAUTH 
</td>
            <td colspan="1" rowspan="1">

The user of the session does not have "operational" authority to the existing database object represented by **IAdgObject** . 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNODIRDEL
</td>
            <td colspan="1" rowspan="1">

The database object represented by **IAdgObject** is contained by a parent library object, and the current session is not authorized to remove objects from the parent library.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTEMPTY
</td>
            <td colspan="1" rowspan="1">

The database object represented by IAdgObject is a library, and the library contains other objects.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTONQTEMP 
</td>
            <td colspan="1" rowspan="1">

The database object represented by **IAdgObject** is the special library "/QTEMP", and the method is not permitted for QTEMP. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmROOTDIR
</td>
            <td colspan="1" rowspan="1">

The database object represented by **IAdgObject** is the special root library "/", and the method is not permitted for root.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ 
</td>
            <td colspan="1" rowspan="1">

Some database providers attempt to obtain an exclusive lock on the database object represented by **IAdgObject** , and an exclusive-read lock on the object's parent. This exception indicates that one of these locks could not be obtained. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmHASDEPEND
</td>
            <td colspan="1" rowspan="1">

The database object represented by **IAdgObject** is a physical file or member with object dependencies precluding its removal.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOMEMDEL
</td>
            <td colspan="1" rowspan="1">

The database object represented by **IAdgObject** is a member contained by a parent file object, and the current session is not authorized to remove members from the parent file.
</td>
          </tr>
</table>

Remarks

If **IAdgObject** is an instance of [IDirectory](dcsIDirectoryClass.html), this method removes the library object it represents. The library cannot be removed if it is the root library or "/QTEMP", or if the library is not empty.

If **IAdgObject** is an instance of [ IFileObject](dcsIFileObjectClass.html), this method removes the file object it represents. The file cannot be removed if object dependencies exist for the file or any members it contains. If the file contains members, the members are also removed.

If **IAdgObject** is an instance of [ IMember](dcsIMemberClass.html), this method removes the member object it represents. The member cannot be removed if object dependencies exist for the member.

To remove all records of a member, use the [ Clear](dcsIMemberClassClearMethod.html) method.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [IAdgObject Class Members](dcsIAdgObjectMembers.html)
      <br />
      [Clear Method](dcsIMemberClassClearMethod.html)
      <br />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

