---
title: AdgFactory.NewDirectory Method

Id: dcsAdgFactoryClassNewDirectoryMethod
TocParent: dcsAdgFactoryMethods
TocOrder: 0

keywords: NewDirectory method
keywords: AdgFactory.NewDirectory method
keywords: path names, create for database libraries
keywords: create database libraries
keywords: database libraries, create
keywords: how to, create database libraries

---

The **NewDirectory** method creates a new instance of [IDirectory](dcsIDirectoryClass.html) representing a database library for object management functions.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public IDirectory NewDirectory(
   [AdgConnection](dcsAdgConnectionClass.html) cn
   string PathName
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub NewDirectory(_ 
   ByVal cn As [AdgConnection](dcsAdgConnectionClass.html)_
   ByVal PathName As string_ 
) As IDirectory** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewDirectory Access(*Public) Type(IDirectory)
   DclSrParm cn Type([AdgConnection](dcsAdgConnectionClass.html))
   DclSrParm PathName Type(*string)** 
      </pre>

Parameters

<dl>
        <dt />
</dl>

*cn* 
<dl>
        <dd>

An instance of [AdgConnection](dcsAdgConnectionClass.html) representing a database connection to the server.
</dd>
        <dt />
</dl>

*PathName* 
<dl>
        <dd>

String. The path name of a new or existing database library object.
</dd>
</dl>

Returns

An instance of an **IDirectory** object.
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

The *cn* and/or *PathName* parameters are null references.
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
<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
								Value of
								<br />
								dgException.Error
							</th>
            <th colspan="1" rowspan="1">
								Condition
							</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVSQLOP
</td>
            <td colspan="1" rowspan="1">

The **AdgConnection** specified is a connection to an SQL Server database provider, and DCS currently does not support the **IDirectory** interface for those providers.
</td>
          </tr>
</table>

Remarks

This method creates a new [IDirectory](dcsIDirectoryClass.html) based upon a new or existing database library (whose path is specified by *PathName* ). The database containing the library is specified as *cn* , an [ AdgConnection](dcsAdgConnectionClassStateProperty.html) object. Note that this method does not throw an exception if *PathName* and *cn* do not reference a valid, pre-existing database library. Subseqent usage of the returned **IDirectory** object's methods may raise such exceptions, however. 

To create a new library, first call **NewDirectory** with the desired name for the new library in *PathName* . Then, with the **IDirectory** reference returned, call the [Create](dcsIAdgObjectClassCreateMethod.html) method. A database library may also be created via [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethods.html).

If the [State ](dcsAdgConnectionClassStateProperty.html) property of the *cn* parameter is not **ConnectionState.Open** , **NewDirectory** may temporarily open the database provider connection, via [AdgConnection.Open](dcsAdgConnectionClassOpenMethod.html). In this case only, upon successful return from **NewDirectory** , the **State** property of *cn* will be **ConnectionState.Closed** .
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8</span> Pro
See 
Also

<dl />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [ReadXml Method](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Create Method](dcsIAdgObjectClassCreateMethod.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [State Property](dcsAdgConnectionClassStateProperty.html)
      <br />
      [Open Method](dcsAdgConnectionClassOpenMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

