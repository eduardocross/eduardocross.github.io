---
title: IAdgObject.Duplicate Method

Id: dcsIAdgObjectClassDuplicateMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 1

keywords: Duplicate method
keywords: IAdgObject.Duplicate method
keywords: DuplicateOptions enumeration, used by
keywords: enumerations [DCS 16.0 DuplicateOptions, used by
keywords: database objects, duplicate with new location and name
keywords: how to, duplicate database objects

---

**Duplicate** creates a duplicate of the database object represented by **IAdgObject** with parameters for specifying the location and name of the duplicated object.
<pre>        <span class="lang">[C#]</span>
 **Public void IAdgObject Duplicate(<br />   string ScopePath ,<br />   string TargetPath ,<br />   string NewName ,<br />[DuplicateOptions](dcsDuplicateOptionsEnumeration.html) options<br />);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Function Duplicate(_<br />     ByVal ScopePath As string_<br />     ByVal TargetPath As string_<br />     ByVal NewName As string_<br />     ByVal options As [DuplicateOptions](dcsDuplicateOptionsEnumeration.html)<br />) As IAdgObject** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc Duplicate Access(*Public) Type(IAdgObject)<br />   DclSrParm ScopePath Type(*string)<br />   DclSrParm TargetPath Type (*string)<br />   DclSrParm NewName Type(*string)<br />   DclSrParm options Type([DuplicateOptions](dcsDuplicateOptionsEnumeration.html))** 
      </pre>

Parameters

<dl>
        <dt>
 *ScopePath* 
        </dt>
        <dd>
**String** . The path name of an existing library representing the boundary of object path references in the duplicated object. The string value must be equal to a prefix of the path name of the database object represented by **IAdgObject** .
</dd>
        <dt>
 *TargetPath* 
        </dt>
        <dd>
**String** . The absolute path name of the library where the duplicate object should reside.
</dd>
        <dt>
 *NewName* 
        </dt>
        <dd>
**String** . The name of the duplicate object.
</dd>
        <dt>
 *options* 
        </dt>
        <dd>
[DuplicateOptions](dcsDuplicateOptionsEnumeration.html). Options for handling the objects contained by objects to be duplicated.
</dd>
</dl>

Returns

A new instance of an **IAdgObject** representing the duplicate object.
Exceptions

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" valign="top" width="20%" style="FONT-WEIGHT: bold" />
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

*ScopePath* , *TargetPath* , or *NewName* is a null reference.
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

<br />

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="20%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1" style="height: 23px">
							Value of dgException.Error</th>
            <th colspan="1" rowspan="1" style="height: 23px">
							Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINV400OP
</td>
            <td colspan="1" rowspan="1">

The IBM i database provider only supports this method when **IAdgObject** represents a file object, and then only when *options* includes the **Members** value.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

One of the following conditions exists: 

- The source or destination library specified does not exist.
- The **Members**  and/or **Data**  values were specified 
										by *options* , but the database provider does not support these 
									values.
- *ScopePath*  is not a prefix of the path name of the database object 
										represented by **IAdgObject** .

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

dgENOTIMPL
</td>
            <td colspan="1" rowspan="1">

The database provider does not support the method for the object type represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOOBJAUTH
</td>
            <td colspan="1" rowspan="1">

The user of the session does not have "use" authority to the existing database object represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ
</td>
            <td colspan="1" rowspan="1">

The current session could not be granted a "share-no-update" lock on the object represented by **IAdgObject** .
</td>
          </tr>
</table>

Remarks

Use **Duplicate** to copy an existing database object represented by **IAdgObject** . *TargetPath* and *NewName* specify the location and name respectively, of the new copy. *options* specifies various options for creating the copy.

*ScopePath* must specify a prefix of the path name of the **IAdgObject** (that is, *ScopePath* names a library that directly or indirectly contains the object to copy). This prefix is replaced with *TargetPath* in the base object paths specified by DCS when the duplicate object is created. This provides some flexibility when copying logical files and their base files.

Current database providers only support the **Duplicate** method on **IAdgObject** instances representing database file objects, and not all options are supported by all providers.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro 
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [IAdgObject Class Members](dcsIAdgObjectMembers.html)
      <br />
      [DuplicateOptions Enumeration](dcsDuplicateOptionsEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

