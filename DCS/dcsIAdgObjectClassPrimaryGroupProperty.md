---
title: IAdgObject.PrimaryGroup Property

Id: dcsIAdgObjectClassPrimaryGroupProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 13

keywords: PrimaryGroup property
keywords: IAdgObject.PrimaryGroup property
keywords: owner names, return primary group name for database object
keywords: group owner names, return for database object
keywords: primary group owner
keywords: database objects, primary group owner name

---

**PrimaryGroup** is the primary group assigned to a database object.
<pre>        <span class="lang">[C#]</span>
 **Public String PrimaryGroup { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property PrimaryGroup As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp PrimaryGroup Access(*Public) Type(*String) Len(45)
   BegGet** 
      </pre>

Property Value

**String.** ReadOnly. The primary group owner for the object. 
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

The path name specified when the **IAdgObject** instance was created does not reference an existing database object or the property is not available for this object type. 
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

This read-only property is the name of the primary group of the database object represented by **IAdgObject** . If no primary group is assigned, the value of **PrimaryGroup** is an empty string.

Depending upon the database provider, **IAdgObject** queries for security attributes, such as **PrimaryGroup** , only once in the lifetime of the **IAdgObject** instance. If attributes change after the query, the change will not be reflected in the property values of the **IAdgObject** . 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

