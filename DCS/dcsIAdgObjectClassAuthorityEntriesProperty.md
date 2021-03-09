---
title: IAdgObject.AuthorityEntries Property

Id: dcsIAdgObjectClassAuthorityEntriesProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 2

keywords: AuthorityEntries property
keywords: IAdgObject.AuthorityEntries property
keywords: how to, determine database object's authorities
keywords: how to, return authorities objects for a database object
keywords: database objects, obtaining authorities currently set
keywords: database authorities, obtaining currently set for a database object
keywords: authorities, obtaining currently set for a database object

---

**AuthorityEntries** is an array of [ AuthorityEntry](dcsAuthorityEntryClass.html) objects collectively describing the user authorities the database provider has assigned to the database object represented by **IAdgObject** . 
<pre>        <span class="lang">[C#]</span>
 **Public AuthorityEntry[] AuthorityEntries { get; set; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Property AuthorityEntries As [AuthorityEntry](dcsAuthorityEntryClass.html)()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp AuthorityEntries Type(AuthorityEntry) Rank(1) Access(*Public) 
   BegGet,    BegSet** 
      </pre>

Property Value

Single-dimension [AuthorityEntry](dcsAuthorityEntryClass.html) array. Elements in the array are not ordered. The maximum **Length** of the array is **System.Int32.MaxValue** .
Exceptions

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" valign="top" width="30%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							ExceptionType</th>
            <th colspan="1" rowspan="1">
							Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException 
</td>
            <td colspan="1" rowspan="1">

The [AdgConnection](dcsAdgConnectionClass.html) or path name specified when the **IAdgObject** instance was created is null. 
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

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col span="1" valign="top" width="20%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of dgException.Error</th>
            <th colspan="1" rowspan="1">
							Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

The path name specified when the **IAdgObject** instance was created does not reference an existing database object. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOTIMPL 
</td>
            <td colspan="1" rowspan="1">

This property is unavailable from the current database provider. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNONSECUREDB 
</td>
            <td colspan="1" rowspan="1">

The property is unavailable because the database does not have the user security feature. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOAUTHLOCK 
</td>
            <td colspan="1" rowspan="1">

The property is unavailable because the database provider could not allocate the pertinent security records. 
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

dgEmINV400OP 
</td>
            <td colspan="1" rowspan="1">

The database provider does not support this property for the object type represented by **IAdgObject** . 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExDENIED 
</td>
            <td colspan="1" rowspan="1">

Access to the property was denied by the database provider's "exit point" security support. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExINVLIC 
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support encountered an exit point validation routine for the property but the license for this support is invalid or not found. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExMISSING 
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support discovered a registration for an exit point validation routine for the property but the validation routine itself was not found. 
</td>
          </tr>
</table>

Remarks

Database providers may assign user authorizations to individual database objects. These authorizations are defined, per user or group profile, with the elements of the array value of **AuthorityEntries** . Each element of the array defines a single user or group profile, and its authority to the database object represented by **IAdgObject** (see **AuthorityEntry** ).

Reading the value of **AuthorityEntries** results in a database query to obtain the current authorization set for the object. The value of **AuthorityEntries** is cached in **IAdgObject** , such that reading the value after the first read returns the same value as the first. Any intervening changes to the database object's authorization set are not reflected by **AuthorityEntries** .

The database object's authorization set can be changed by assigning a value to **AuthorityEntries** . Changing the value of the array reference returned by **AuthorityEntries** has no effect on the database object, until the value is explicitly assigned back to **AuthorityEntries** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [AuthorityEntry Class](dcsAuthorityEntryClass.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

