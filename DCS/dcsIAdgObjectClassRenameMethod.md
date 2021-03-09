---
title: IAdgObject.Rename Method

Id: dcsIAdgObjectClassRenameMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 7

keywords: Rename method
keywords: IAdgObject.Rename method
keywords: database objects, rename bases
keywords: rename database objects bases
keywords: base objects, rename
keywords: how to, rename database base objects

---

The **Rename** method renames an object without changing its location in the database.
<pre>        <span class="lang">[C#]</span>
 **Public void IAdgObject Rename(<br />   string NewName<br />);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub Rename(_<br />   ByVal NewName As string<br />) As IAdgObject** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Rename Access(*Public) Type(IAdgObject)
   DclSrParm NewName Type(*string) Len(45)** 
      </pre>

Parameters

<dl>
        <dt>
 *NewName* 
        </dt>
        <dd>
String. The new name for the [IAdgObject](dcsIAdgObjectClass.html).
</dd>
</dl>

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

NullReferenceException 
</td>
            <td colspan="1" rowspan="1">

*NewName* is a null reference. 
</td>
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

The path name specified when the **IAdgObject** instance was created does not reference an existing database object or the method is not available for this object type. 
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

dgEmNOPARENTUPD
</td>
            <td colspan="1" rowspan="1">

The database object represented by **IAdgObject** is contained by a parent file or library object and "update" access is not permitted by the parent.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTONQTEMP
</td>
            <td colspan="1" rowspan="1">

The database object represented by **IAdgObject** is the special library "/QTEMP" and the method is not permitted for QTEMP.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmROOTDIR 
</td>
            <td colspan="1" rowspan="1">

The database object represented by **IAdgObject** is the special root library "/" and the method is not permitted for root. 
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

dgEmINVOBJNAME 
</td>
            <td colspan="1" rowspan="1">

*NewName* fails the database provider's syntax check for valid object names due to invalid or reserved characters. 
</td>
          </tr>
</table>

Remarks

This method permits the renaming of an existing database object represented by **IAdgObject** . *NewName* must conform to the database provider's conventions for object names and the user of the session must have requisite authority to the object.

**Rename** only changes the base name of the object. To change the path name of the object, consider using [MoveTo](dcsIAdgObjectClassMoveToMethod.html), [Duplicate](dcsIAdgObjectClassDuplicateMethod.html), or another method capable of creating an equivalent object in a different location.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [MoveTo Method](dcsIAdgObjectClassMoveToMethod.html)
      <br />
      [Duplicate Method](dcsIAdgObjectClassDuplicateMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

