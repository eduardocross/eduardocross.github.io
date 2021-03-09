---
title: IFileObject.Copy Method

Id: dcsIFileObjectClassCopyMethod
TocParent: dcsIFileObjectMethods
TocOrder: 0

keywords: Copy method
keywords: IFileObject.Copy method
keywords: copy a database file
keywords: database files, copy
keywords: how to, copy a database file

---

**Copy** creates a copy of the database file represented by **IFileObject** with the name and location specified.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public IFileObject Copy(<br />   string targetDir ,<br />   string newName ,<br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function Copy(_<br />    ByVal targetDir As string _<br />    ByVal newName As string _<br />) As IFileObject** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc Copy Access(*Public) Type(IFileObject)<br />   DclSrParm targetDir Type (*string)<br />   DclSrParm newName Type(*string)** 
      </pre>

Parameters

<dl>
        <dt>
 *targetDir* 
        </dt>
        <dd>

String. The target library path name for the new copy of the file.
</dd>
        <dt>
 *newName* 
        </dt>
        <dd>

String. The name for the new copy of the file. This must not be a path name.
</dd>
</dl>

Exceptions

<br />

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

*targetDir* or *newName* are null references. 
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

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells"> <colgroup span="1"> <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" /> <col span="1" style="WIDTH: 70%" /> </colgroup> <tr> <th colspan="1" rowspan="1"> Value of dgException.Error </th> <th colspan="1" rowspan="1"> Condition </th> </tr> <tr> <td colspan="1" rowspan="1"> <p>dgEmFNOTFND 
</td>
            <td colspan="1" rowspan="1">

The path name of **IFileObject** (copy source path) does not reference a database file. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOOBJAUTH
</td>
            <td colspan="1" rowspan="1">

The current session does not have "read" authority to the file represented by **IFileObject** (the copy source).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ
</td>
            <td colspan="1" rowspan="1">

The database provider failed to obtain a "share no update" lock for the file represented by **IFileObject** (the copy source).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOATTR, dgErBADSRC, dgEaBADFRMTID, or dgErADENOTFND 
</td>
            <td colspan="1" rowspan="1">

The internal database file inconsistency was found by the database provider. The file represented by IFileObject (the copy source) should be repaired or restored.
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
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTFND
</td>
            <td colspan="1" rowspan="1">

The library specified by *targetDir* does not exist.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNODIRADD
</td>
            <td colspan="1" rowspan="1">

The current session does not have "add" and/or "execute" authority to the library specified by *targetDir* .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmDUPOBJ
</td>
            <td colspan="1" rowspan="1">

An object in library *targetDir* with the name *newName* already exists.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

*targetDir* , *newName* , and/or the path name of the file represented by this IFileObject are invalid database object names/paths.
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

Access to the method was denied by the database provider's "exit point" security support.
</td>
          </tr>
</table>

Remarks

**Copy** creates a new database file using the formats of the file represented by **IFileObject** (the copy source). Member objects of the copy source are duplicated in the new file but physical file member data is not. This method provides functionality similar to the CRTDUPOBJ command of the iSeries. The "basing" rules for copying logical files are provider-dependent but in general, physical base files are not automatically copied to the target library when the copy source is a logical file.

The new database file will reside in the *targetDir* library with the name *newName* . The current session must have "read" authority to the copy source file and "add" authority to *targetDir* . The copy source is locked for "share no update" access for the duration of the method. Upon successful completion, **Copy** returns an instance of **IFileObject** , which represents the new file. 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [IFileObject Class Members](dcsIFileObjectMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

