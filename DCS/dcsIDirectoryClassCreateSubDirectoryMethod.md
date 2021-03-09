---
title: IDirectory.CreateSubDirectory Method

Id: dcsIDirectoryClassCreateSubDirectoryMethod
TocParent: dcsIDirectoryMethods
TocOrder: 1

keywords: CreateSubDirectory method
keywords: IDirectory.CreateSubDirectory method
keywords: database libraries, create sub-directories for
keywords: sub-directories, create
keywords: how to, create library sub-directories

---

**CreateSubDirectory** creates a new library contained by the library represented by [IDirectory](dcsIDirectoryClass.html).
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **Public void IDirectory CreateSubDirectory(_<br />   string name_<br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub CreateSubDirectory(<br />   ByVal name As string,<br />) As IDirectory** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc CreateSubDirectory Access(*Public) Type(IDirectory)
  DclSrParm name Type(*string) Len(45)** 
      </pre>

Parameters

<dl>
        <dt>
 *name* 
        </dt>
        <dd>
String. Specifies the base name of the new library. This must not be a full or relative path name.
</dd>
</dl>

Returns

**IDirectory** . The returned instance represents the newly created library.
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

NullReferenceException 
</td>
            <td colspan="1" rowspan="1">

*name* is a null reference. 
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

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
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

dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

*name* contains a path name, rather than a base name, or is otherwise an invalid name according to the database provider. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmDUPOBJ 
</td>
            <td colspan="1" rowspan="1">

An object named *name* already exists in the library. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExDENIED
</td>
            <td colspan="1" rowspan="1">

Access to the method was denied by the database provider's "exit point" security support.
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

dgExMISSING
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support discovered a registration for an exit point validation routine for the method but the validation routine itself was not found.
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

dgEmNODIRADD
</td>
            <td colspan="1" rowspan="1">

The current session does not have "add" authority to the parent of the library represented by **IDirectory** .
</td>
          </tr>
</table>

Remarks

Use this method to create a library whose parent library is represented by **IDirectory** . Note that creating such a "sub-library" is a database provider-dependent function. For example, on System i databases, only the root library "/" (also known as QSYS) can contain other libraries. 

**CreateSubDirectory** returns a new instance of **IDirectory** , which represents the newly-created library. 

**CreateSubDirectory** creates libraries that are direct descendants of the library represented by **IDirectory** and therefore *name* must not contain a path name (i.e., no file separator characters such as "/"). Alternatively, to create a library in a random location in the database, use the [ AdgFactory.NewDirectory](dcsAdgFactoryClassNewDirectoryMethod.html) method, naming the location for the new library. Then call [IAdgObject.Create](dcsIAdgObjectClassCreateMethod.html) on the returned **IDirectory** instance.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [IDirectory Members](dcsIDirectoryMembers.html)
      <br />
      [AdgFactory.NewDirectory Method](dcsAdgFactoryClassNewDirectoryMethod.html)
      <br />
      [IAdgObject.Create Method](dcsIAdgObjectClassCreateMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

