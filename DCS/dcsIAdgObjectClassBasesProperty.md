---
title: IAdgObject.Bases Property

Id: dcsIAdgObjectClassBasesProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 3

keywords: Bases property
keywords: IAdgObject.Bases property
keywords: base objects path name for a database object
keywords: path names, return the base object(s) path name for a database object
keywords: path names, set the base object(s) path name for a database object
keywords: how to, return path names of base objects for a database object
keywords: how to, set path names of base objects for a database object
keywords: database objects, return base object(s) path names

---

**Bases** is a single-dimension array of strings containing path names denoting the set of objects upon which the database object represented by **IAdgObject** is based.
<pre>        <span class="lang">[C#]</span>
 **public string[] Bases { get; set; }** 
 **** </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Property Bases As string()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Bases Access(*Public) Type(*String) Rank(1)<br />  BegGet   BegSet** 
      </pre>

Property Value

**String** array. The **Length** of the array is equal to the number of base objects and may be no greater than **ASNA.DataGate.Common.MaxBaseFiles** . 
Exceptions

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="30%" style="FONT-WEIGHT: bold" />
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
            <col span="1" width="20%" style="FONT-WEIGHT: bold" />
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

Reading the value of **Bases** caused a database query for base path names but the path name of the database object represented by **IAdgObject** (specified when **IAdgObject** was created) does not name a valid database object or names an object type that cannot have base objects.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOOBJAUTH
</td>
            <td colspan="1" rowspan="1">

Reading the value of **Bases** caused a database query for base path names but the current session does not have "operational" authority to the object represented by **IAdgObject.** 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ
</td>
            <td colspan="1" rowspan="1">

Reading the value of **Bases** caused a database query for base path names but the database provider could not obtain a shared-read lock for the object represented by **IAdgObject** in the current session.
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
</table>

Remarks

Logical files and members have one or more base objects upon which their definitions are based. **Bases** names these base objects by their absolute path names. The value of **Bases** for **IAdgObject** instances representing libraries, physical files, and physical members is an empty array.

When **IAdgObject** represents an existing database object, reading the value of **Bases** results in a query to the database provider to fetch the base paths, if **Bases** has not been set previously or has been set to a null reference.

When **IAdgObject** represents a database object to be created with the [Create](dcsIAdgObjectClassCreateMethod.html) method, **Bases** must be set to the paths of the base objects prior to calling **Create** . When creating a logical file, **Bases** must name physical files with format identifiers matching the base format identifiers of the file definition or an exception will occur in **Create** . The **Length** of the string array must be no greater than **ASNA.DataGate.Common.MaxBaseFiles** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Create Method](dcsIAdgObjectClassCreateMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

