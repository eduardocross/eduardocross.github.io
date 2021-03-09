---
title: Program.ExecuteSQL_QueryVerbatim Method (DbConnection,string,DBParm[])

Id: amfProgramClassExecuteSQL_QueryVerbatimMethod2
TocParent: amfProgramClassExecuteSQL_QueryVerbatimMethods
TocOrder: 40

---

Executes a SQL query specifying the database connection, SQL statement (exactly as stated in the RPG code), and statement parameters.
<!-- start -->

#### Syntax
<pre class="syntax"> **BegFunc ExecuteSQL_QueryVerbatim Access(*Public) Type(System.Collections.Generic.Dictionary)
   DclSrParm *sqlConnection*  Type(System.Data.Common.DbConnection)
   DclSrParm *sqlText*  Type(*String)
   DclSrParm *parameters*  Type (DBParm) Rank(1)**       </pre>

#### Parameters
<dl>
        <dt>
 *sqlConnection* 
        </dt>
        <dd>
          [
        DBParm](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx">
        System.Data.Common.DbConnection</a>. The database
        connection.</dd>
        <dt>
 *sqlText* 
        </dt>
        <dd>String. The SQL statement
        with a substitution variable defined for each
        parameter.</dd>
        <dt>
 *parameters* 
        </dt>
        <dd>
          <a href="amfProgramDBParmClass.html). An array containing the query parameters.</dd>
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
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
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
[Program Class](amfProgramClass.html) <br /> [Program Class Members](amfProgramClassMembers.html) <br /> [ SqlQueryResults Field](amfProgramClassSqlQueryResultsField.html) <br /> [ Program.DBParm Class](amfProgramDBParmClass.html) <br /> [ASNA.Monarch Namespace](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx"> System.Data.Common.DbConnection</a> <br /> <a href="amfMonarchNamespace.html) 
