---
title: IAdgObject.ObjectID Property

Id: dcsIAdgObjectClassObjectIDProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 9

keywords: ObjectID property
keywords: IAdgObject.ObjectID property
keywords: object identifiers, for database objects
keywords: object identifiers
keywords: database objects, return object identifier
keywords: how to, return object identifier for database objects

---

**ObjectID** identifies the object represented by **IAdgObject** .
<pre>        <span class="lang">[C#]</span>
 **Public int ObjectID { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property ObjectID As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp ObjectID Access(*Public) Type(*Integer)
   BegGet** 
      </pre>

Property Value

**Integer** . ReadOnly. The object identifier. 
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

The property is not available for this object type, or the object name does not reference an existing database object. 
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

Certain database providers assign a unique integer identifier to each object in the database. **ObjectID** is the identifier of the existing database object represented by **IAdgObject** , for database providers which support object identifiers.

If the database provider does not support object identifiers, the value of **ObjectID** is zero.

**IAdgObject** queries the database provider for certain object attributes, such as **ObjectID** only once in the lifetime of the **IAdgObject** instance. If attributes change after the query, the change will not be reflected in the property values the **IAdgObject** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

