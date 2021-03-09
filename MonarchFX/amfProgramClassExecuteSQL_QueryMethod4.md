---
title: Program.ExecuteSQL_Query Method (DbConnection,string)

Id: amfProgramClassExecuteSQL_QueryMethod4
TocParent: amfProgramClassExecuteSQL_QueryMethods
TocOrder: 30

---

Executes a SQL query specifying the database connection and SQL statement without parameters.
<!-- start -->

#### Syntax
<pre class="prettyprint"> **BegFunc ExecuteSQL_Query Access(*Public) Type(System.Collections.Generic.Dictionary)
   DclSrParm *sqlConnection*  Type(System.Data.Common.DbConnection)
   DclSrParm *sqlText*  Type(*String)**       </pre>

#### Parameters
<dl>
        <dt>
 *sqlConnection* 
        </dt>
        <dd>
          [ASNA.Monarch](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx">
        System.Data.Common.DbConnection</a>. The database
        connection.</dd>
        <dt>
 *sqlText* 
        </dt>
        <dd>String. The SQL statement.</dd>
</dl>

#### Returns
**System.Collections.Generic.Dictionary** (string and object) representing the query results allowing values for a particular column to be accessed by name.
<!-- -->

 <!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td><a href="amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[Program Class](amfProgramClass.html) <br /> [Program Class Members](amfProgramClassMembers.html) <br /> [ SqlQueryResults Field](amfProgramClassSqlQueryResultsField.html) <br /> [ASNA.Monarch Namespace](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx"> System.Data.Common.DbConnection</a> <br /> <a href="amfMonarchNamespace.html) 
