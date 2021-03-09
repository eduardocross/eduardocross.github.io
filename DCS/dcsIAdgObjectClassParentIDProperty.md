---
title: IAdgObject.ParentID Property

Id: dcsIAdgObjectClassParentIDProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 12

keywords: ParentID property
keywords: IAdgObject.ParentID property
keywords: parent identifiers, for database objects
keywords: database objects, return parent identifier

---

**ParentID** identifies a parent database object of the object represented by **IAdgObject** .
<pre>        <span class="lang">[C#]</span>
 **Public int ParentID { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property ParentID As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp ParentID Access(*Public) Type(*Integer)
   BegGet** 
      </pre>

Property Value

**Integer** . ReadOnly. The parent identifier. 
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

The property is not available for this object type or the object name does not reference an existing database object. 
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

dgEmNOTFND
</td>
            <td colspan="1" rowspan="1">

The path name specified when the **IAdgObject** instance was created does not reference an existing database object.
</td>
          </tr>
</table>

Remarks

All objects in a database, except for the root library, have a parent object which contains the object. For example, the parent of a file is a library. Certain database providers assign a unique integer identifier to each object in the database. **ParentID** is the unique identifier of the parent of the existing database object represented by **IAdgObject** , for database providers which support object identifiers.

If the database provider does not support object identifiers, the value of **ParentID** is zero.

**IAdgObject** queries the database provider for certain object attributes, such as **ParentID** only once in the lifetime of the **IAdgObject** instance. If attributes change after the query, the change will not be reflected in the property values the **IAdgObject** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html) 

