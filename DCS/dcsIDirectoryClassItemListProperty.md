---
title: IDirectory.ItemList Property

Id: dcsIDirectoryClassItemListProperty
TocParent: dcsIDirectoryProperties
TocOrder: 0

keywords: ItemList property
keywords: IDirectory.ItemList property
keywords: database libraries, return list of files and libraries
keywords: how to, list files and libraries in a database library
keywords: itemlist of files and libraries in a database library

---

**ItemList** is a list of [IAdgObject](dcsIAdgObjectClass.html) references corresponding to the database object contents of an existing library.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public ArrayList ItemList { get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property ItemList() As ArrayList** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp ItemList Access(*Public) Type(ArrayList) Len(4)
   BegGet** 
      </pre>

Property Value

**System.Collections.ArrayList** . The list of database objects given as **IAdgObject** references. 
Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
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

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
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

dgEmNODIRREAD 
</td>
            <td colspan="1" rowspan="1">

The database provider's security model does not permit the current session to access lists of library contents. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The path name given for this IDirectory object does not correspond to a database library.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExMISSING
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support discovered a registration for an exit point validation routine for the method but the validation routine itself was not found.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExINVLIC
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support encountered an exit point validation routine for the method but the license for this support is invalid or not found.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExDENIED
</td>
            <td colspan="1" rowspan="1">

Access to the method property was denied by the database provider's "exit point" security support.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINTERNAL
</td>
            <td colspan="1" rowspan="1">

A database provider internal error occurred. Review the provider's event logs for more information.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOMEM
</td>
            <td colspan="1" rowspan="1">

The database provider encountered an "out of memory" exception.
</td>
          </tr>
</table>

Remarks

This read-only property provides a set of **IAdgObject** references corresponding to the files and libraries contained in the database library represented by **IDirectory** . Each element of the **ArrayList** value of the property is an instance of **IAdgObject** . The underlying type of the **IAdgObject** reference (either **IDirectory** or [IFileObject](dcsIFileObjectClass.html)) is determined by the value of the [IAdgObject.AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html) property. A library containing no libraries or files is denoted by an **ArrayList** of zero elements. 

DCS establishes the value of **ItemList** only once in the lifetime of the **IDirectory** instance. When the property value is first accessed, the list value is created. Subsequent accesses of the value do not refresh the list and therefore may not reflect intervening changes to the library's contents. To obtain a refereshed list of objects, create a new **IDirectory** instance, or use the [ Enumerate](dcsIDirectoryClassEnumerateMethod.html) method. 

Also, the list returned by **ItemList** is not a copy and hence, any changes to the list by the user program will be reflected in subsequent accesses of **ItemList** . Note that user program changes to the **ArrayList** value of **ItemList** have no effect on the contents of the database library.

**Enumerate** provides similar information but uses a delegate-based interface and **Enumerate** does not return cached results. 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [IDirectory Class Members](dcsIDirectoryMembers.html)
      <br />
      [Enumerate Method](dcsIDirectoryClassEnumerateMethod.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [AdgObjectType Property](dcsIAdgObjectClassAdgObjectTypeProperty.html)
      <br />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

