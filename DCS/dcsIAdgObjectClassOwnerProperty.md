---
title: IAdgObject.Owner Property

Id: dcsIAdgObjectClassOwnerProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 10

keywords: Owner property
keywords: IAdgObject.Owner property
keywords: owner names, return group or user profile for database object
keywords: owner name for database objects
keywords: how to, determine owner name for database object
keywords: database objects, owner name of group or user profile

---

**Owner** is the user or group account that owns the database object represented by **IAdgObject** .
<pre>        <span class="lang">[C#]</span>
 **Public string Owner { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property Owner As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Owner Access(*Public) Type(*String) Len(45)
   BegGet** 
      </pre>

Property Value

**String** . Read only. The name of the user or group account that owns the object. 
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

<table class="dtTABLE" id="Table3" cellspacing="0"> <colgroup span="1"> <col align="middles" span="1" style="FONT-WEIGHT: bold" width="20%" /> <col span="1" width="70%" /> </colgroup> <tr> <th colspan="1" rowspan="1"> Value of dgException.Error </th> <th colspan="1" rowspan="1"> Condition </th> </tr> <tr> <td colspan="1" rowspan="1"> <p>dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

The path name specified when the **IAdgObject** instance was created does not reference an existing database object, or the property is not available for this object type. 
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

dgEgNONSECUREDB
</td>
            <td colspan="1" rowspan="1">

The property value is unavailable because the database does not have the user security feature.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOAUTHLOCK
</td>
            <td colspan="1" rowspan="1">

The user of the session does not have "management" authority to the existing database object represented by **IAdgObject** .
</td>
          </tr>
</table>

Remarks

This read-only property is the name of the group or user profile assigned ownership of the database object represented by **IAdgObject** . If [OwnerIsGroup](dcsIAdgObjectClassOwnerIsGroupProperty.html) is **True** , then **Owner** names a group profile. If **OwnerIsGroup** is **False** , **Owner** names a user profile.

Depending upon the database provider, **IAdgObject** queries for security attributes, such as **Owner** , only once in the lifetime of the **IAdgObject** instance. If attributes change after the query, the change will not be reflected in the property values of the **IAdgObject** . 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [OwnerIsGroup Property](dcsIAdgObjectClassOwnerIsGroupProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

