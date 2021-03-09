---
title: AdgFactory.NewLibraryList Method

Id: dcsAdgFactoryClassNewLibraryListMethod

keywords: NewLibraryList method
keywords: AdgFactory.NewLibraryList method
keywords: path names, create for database library list
keywords: create database library list
keywords: database library lists, create
keywords: how to, create database library lists

---

The **NewLibraryList** method creates a new instance of [ ILibraryList](dcsILibraryListClass.html) representing a library list for object management functions.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public ILibraryList NewLibraryList(
   [AdgConnection](dcsAdgConnectionClass.html) cn** 
);</pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub NewLibraryList(_ 
   ByVal cn As [AdgConnection](dcsAdgConnectionClass.html) _
) As ILibraryList** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewLibraryList Access(*Public) Type(ILibraryList)
   DclSrParm cn Type([AdgConnection](dcsAdgConnectionClass.html))** 
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
</dl>

Returns

An instance of an **ILibraryList** object.
<br />

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

The *cn* parameter is a null references.
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

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

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

The **AdgConnection** specified is a connection to an SQL Server database provider, and DCS currently does not support the **ILibraryList** interface for those providers.
</td>
          </tr>
</table>

Remarks

This method creates a new [ILibraryList](dcsILibraryListClass.html) based on the database containing the library list, which is specified as *cn* , an [AdgConnection](dcsAdgConnectionClassStateProperty.html) object. Note that this method does not throw an exception if *cn* do not reference a valid, pre-existing database library. Subseqent usage of the returned **ILibraryList** object's methods may raise such exceptions, however. 

To create a new library list, first call **NewLibraryList** with the desired **AdgConnection** object. Then, with the **ILibraryList** reference returned, call the [Create](dcsIAdgObjectClassCreateMethod.html) method. A database library list may also be created via [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethods.html).

If the [State](dcsAdgConnectionClassStateProperty.html) property of the *cn* parameter is not **ConnectionState.Open** , **NewLibraryList** may temporarily open the database provider connection via [AdgConnection.Open](dcsAdgConnectionClassOpenMethod.html). In this case only, upon successful return from **NewLibraryList** , the **State** property of *cn* will be **ConnectionState.Closed** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See 
Also

<dl />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [ReadXml Methods](dcsAdgFactoryClassReadXmlMethods.html)
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

