---
title: IAdgObject.AdgSubType Property

Id: dcsIAdgObjectClassAdgSubTypeProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 1

keywords: AdgSubType property
keywords: IAdgObject.AdgSubType property
keywords: AdgSubTypes enumeration, used by
keywords: enumerations [DCS 16.0 AdgSubTypes, used by
keywords: types, database object sub-types
keywords: database types, identifying sub-types
keywords: database sub-types, identifying
keywords: database files, identifying sub-type
keywords: database file members, identifying sub-type
keywords: database libraries, identifying sub-type
keywords: how to, identify sub-type of database object

---

**AdgSubType** identifies the secondary type of the database object represented by **IAdgObject** . 
<pre>        <span class="lang">[C#]</span>
 **Public [AdgSubTypes](dcsAdgSubTypesEnumeration.html) AdgSubType { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property AdgSubType As [AdgSubTypes](dcsAdgSubTypesEnumeration.html)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp AdgSubType Type([AdgSubTypes](dcsAdgSubTypesEnumeration.html)) Access(*Public) 
     BegGet** 
      </pre>

Property Value <p> [AdgSubTypes](dcsAdgSubTypesEnumeration.html). ReadOnly. A sub-classification of the database object, such as Join, Physical, etc. 
<br />

Exceptions

<br />

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

**AdgSubType** is a secondary type which may be assigned by the database provider to further classify the primary type (see [ AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html)) of the database object represented by **IAdgObject** . The following table lists the possible values of **AdgSubType** for the various values of **AdgObjectType** .
<br />

<table class="dtTABLE" id="Table4" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <tr>
            <th colspan="1" rowspan="1">
							Value of AdgObjectType (primary type)
						</th>
            <th colspan="1" rowspan="1">
							Possible values for AdgSubTypes<br />
							 (secondary type)
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Directory
</td>
            <td colspan="1" rowspan="1">

Local
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

File
</td>
            <td colspan="1" rowspan="1">

Join, Merge, Physical, SqlLogical, Simple (logical), OlePrint, NetPrint, Unknown
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Member
</td>
          </tr>
</table>

<table> <tbody> <tr> <td colspan="1" rowspan="1"> <p>Join, Merge, Physical, SqlLogical, Simple (logical), Unknown
</td>
            </tr>
          </tbody>
</table>

<br />

When the database provider does not support, or cannot readily determine the secondary type for a particular object, the **Unknown** value is assigned to **AdgSubType** . If **AdgSubType** is **Unknown** for a file object, the secondary type information can be obtained via the file definition regardless of the database provider (see [ IFileObject.WriteDefinition](dcsIFileObjectClassWriteDefinitionMethod.html) or [ IFileObject.WriteXml](dcsIFileObjectClassWriteDefinitionMethod.html)).

**IAdgObject** queries the database provider for certain object attributes such as **AdgSubType** only once in the lifetime of the **IAdgObject** instance. If attributes change after the query, the change will not be reflected in the property values of **IAdgObject** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [AdgObjectType Property](dcsIAdgObjectClassAdgObjectTypeProperty.html)
      <br />
      [AdgSubType Enumeration](dcsAdgSubTypesEnumeration.html)
      <br />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [WriteDefinition Method](dcsIFileObjectClassWriteDefinitionMethod.html)
      <br />
      [WriteXml Methods](dcsIFileObjectClassWriteDefinitionMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

