---
title: IDirectory.AttachRemoteDirectory Method

Id: dcsIDirectoryClassAttachRemoteDirectoryMethod
TocParent: dcsIDirectoryMethods
TocOrder: 0

keywords: AttachRemoteDirectory method
keywords: IDirectory.AttachRemoteDirectory method
keywords: remote directories, attach to database library
keywords: remote directories, Acceler8DB compatibility
keywords: database libraries, attach remote directories to
keywords: how to, attach remote directories to database library

---

**AttachRemoteDirectory** attaches a remote directory to an database library object.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **Public void IDirectory AttachRemoteDirectory(_<br />   string remotePathName <br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub AttachRemoteDirectory(<br />   ByVal remotePathName As string,<br />) As IDirectory** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr AttachRemoteDirectory Access(*Public) Type(IDirectory)
   DclSrParm remotePathName Type(*string)** 
      </pre>

Parameters

<dl>
        <dt>
 *remotePathName* 
        </dt>
        <dd>
String. Specifies the full pathname of the directory to be attached to the library.
</dd>
</dl>

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

*remotePathName* is a null reference. 
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

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. he following table summarizes these conditions, and the corresponding value of the dgException.Error property.
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

dgEmINV400OP 
</td>
            <td colspan="1" rowspan="1">

This method is not supported by the database provider. 
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
          <tr>
            <td colspan="1" rowspan="1">

dgEmDUPOBJ
</td>
            <td colspan="1" rowspan="1">

A database library already exists in the location referenced by **IDirectory** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

*remotePathName* does not name a valid directory. 
</td>
          </tr>
</table>

Remarks

This method is provided for compatibility with legacy Acceler8DB database systems. Only Windows-based "datalink" database providers support this method.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IDirectory Class](dcsIDirectoryClass.html) <br />[IDirectory Members](dcsIDirectoryMembers.html)<br />[ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

