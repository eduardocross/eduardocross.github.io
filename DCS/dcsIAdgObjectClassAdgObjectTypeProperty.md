---
title: IAdgObject.AdgObjectType Property

Id: dcsIAdgObjectClassAdgObjectTypeProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 0

keywords: AdgObjectType property
keywords: IAdgObject.AdgObjectType property
keywords: AdgObjectTypes enumeration, used by
keywords: enumerations [DCS 16.0 AdgObjectTypes, used by
keywords: types, database object types
keywords: database types, identifying
keywords: database files, identifying type
keywords: database file members, identifying type
keywords: database libraries, identifying type
keywords: how to, identify type of database object

---

**AdgObjectType** identifies the type (file, library, member) of the database object represented by **IAdgObject** . 
<pre>        <span class="lang">[C#]</span>
 **Public [AdgObjectTypes](dcsAdgObjectTypesEnumeration.html) AdgObjectType { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property AdgObjectType As [AdgObjectTypes](dcsAdgObjectTypesEnumeration.html)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp AdgObjectType Type([AdgObjectTypes](dcsAdgObjectTypesEnumeration.html)) Access(*Public) <br />    BegGet** 
      </pre>

Property Value <p> [AdgObjectTypes](dcsAdgObjectTypesEnumeration.html). ReadOnly. The database object type.
Exceptions

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" valign="top" style="FONT-WEIGHT: bold" width="30%" />
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
            <col span="1" valign="top" style="FONT-WEIGHT: bold" width="20%" />
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

**IAdgObject** is the base class of the classes representing database objects ( **IDirectory** , **IFileObject** , **IMember** ). The value of **AdgObjectType** determines the implementation type of the **IAdgObject** , according to the following table:
<br />

<table class="dtTABLE" id="Table4" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" valign="top" style="WIDTH: 9%" />
            <col span="1" valign="top" style="WIDTH: 20%" />
            <col span="1" valign="top" style="WIDTH: 10%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of AdgObjectType
						</th>
            <th colspan="1" rowspan="1">
							Implementation interface of **IAdgObject** </th>
            <th colspan="1" rowspan="1">
							Database object type</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">Directory
						</td>
            <td colspan="1" rowspan="1">
              [IDirectory](dcsIDirectoryClass.html)
            </td>
            <td colspan="1" rowspan="1">Library
						</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">File
						</td>
            <td colspan="1" rowspan="1">
              [IFileObject](dcsIFileObjectClass.html)
            </td>
            <td colspan="1" rowspan="1">File</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">Member</td>
            <td colspan="1" rowspan="1">
              [IMember](dcsIMemberClass.html)
            </td>
            <td colspan="1" rowspan="1">Member</td>
          </tr>
</table>

<br />

So for example, any **IAdgObject** instance whose **AdgObjectType** property is **File** is an **IFileObject** instance. This can be useful when using methods such as [ IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html), which enumerates a set of generic **IAdgObject** instances.

**IAdgObject** and DCS do not support the **DataArea** value of **AdgObjectTypes** at this time.

**IAdgObject** queries the database provider for certain object attributes, such as **AdgObjectType** , only once in the lifetime of the **IAdgObject** instance. If attributes change after the query, the change will not be reflected in the property values of **IAdgObject** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [Enumerate Method](dcsIDirectoryClassEnumerateMethod.html)
      <br />
      [AdgObjectTypes Enumeration](dcsAdgObjectTypesEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

