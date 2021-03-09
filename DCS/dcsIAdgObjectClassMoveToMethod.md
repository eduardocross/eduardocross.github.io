---
title: IAdgObject.MoveTo Method

Id: dcsIAdgObjectClassMoveToMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 4

keywords: MoveTo method
keywords: IAdgObject.MoveTo method
keywords: database objects, move to new library
keywords: move database objects to new library
keywords: how to, move database objects to new library

---

**MoveTo** moves a database library or file represented by **IAdgObject** to a specified library.
<pre>        <span class="lang">[C#]</span>
 **Public void IAdgObject MoveTo(<br />   string LibraryPath<br />);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic]</span>
 **Public Sub MoveTo(_<br />   ByVal LibraryPath As string<br />) As IAdgObject** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr MoveTo Access(*Public) Type(IAdgObject
   DclSrParm LibraryPath Type(*string) Len(45)** 
      </pre>

Parameters

<dl>
        <dt>
 *LibraryPath*  
					</dt>
        <dd>
**String** . he absolute path of the library to which the the database object will be moved.
</dd>
</dl>

Exceptions

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" style="FONT-WEIGHT: bold" width="30%" />
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

*LibraryPath* is a null reference. 
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
            <col align="middles" span="1" style="FONT-WEIGHT: bold" width="20%" />
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

One or more of the following conditions is true:

- *LibraryPath* 
								is not a valid, absolute path to a library object.
- The path name specified when the **IAdgObject** 
								instance was created does not reference an existing database object.
- The method is not available for this object type.

</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINV400OP 
</td>
            <td colspan="1" rowspan="1">

The IBM i database provider does not support the method on this particular object type. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR 
</td>
            <td colspan="1" rowspan="1">

The IBM i database provider encountered a system-level error. Details provided in the **dgException.Message** property. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmDNOTFND
</td>
            <td colspan="1" rowspan="1">

The object represented by **IAdgObject** is a library, and the library was not found.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmFNOTFND
</td>
            <td colspan="1" rowspan="1">

The object represented by **IAdgObject** is a file, and the file was not found.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOOBJAUTH
</td>
            <td colspan="1" rowspan="1">

The user of the session does not have "management" authority to the existing database object represented by **IAdgObject.** 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTONQTEMP
</td>
            <td colspan="1" rowspan="1">

The database object represented by **IAdgObject** is the special library "/QTEMP", and the method is not permitted against "/QTEMP".
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNODIRDEL
</td>
            <td colspan="1" rowspan="1">

The user of the session does not have "delete" authority to the library containing the existing database object represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOPERMINTEMP
</td>
            <td colspan="1" rowspan="1">

One of the following conditions is true:

- The object represented by **IAdgObject** 
								is a permanent object, and the target library is a temporary object.
- The object represented by **IAdgObject**  is a temporary object, 
									and the target library is a permanent object.

</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBADCAT 
</td>
            <td colspan="1" rowspan="1">

The database provider has detected a catalog error. The database should be repaired. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ
</td>
            <td colspan="1" rowspan="1">

The current session was not granted one of the following lock requests:

- The source library containing the object represented by **IAdgObject** , 
								for "exclusive-read".
- The target library, where the object represented by **IAdgObject** 
								is to be moved, for "exclusive-read".
- The object represented by **IAdgObject** , for "exclusive".

</td>
          </tr>
</table>

Remarks

The **MoveTo** method moves a database object from one library to another. The source library is specified as the library containing the object represented by **IAdgObject** (named by the object path specified when the **IAdgObject** instance was created). The target library is specified by *LibraryPath* . Note that a member object cannot be moved from the file containing it.

Upon successful completion of the method, **IAdgObject** represents the object in its new location and the string returned by [ ToString](dcsIAdgObjectClassToStringMethod.html) method will reflect the new object path. 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro 
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [ToString Method](dcsIAdgObjectClassToStringMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

