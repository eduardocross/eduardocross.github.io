---
title: Program.ExecuteSQL_QueryVerbatim Methods

Id: amfProgramClassExecuteSQL_QueryVerbatimMethods
TocParent: amfProgramClassMethods
TocOrder: 40

keywords: ExecuteSQL_QueryVerbatim method
keywords: Program.ExecuteSQL_QueryVerbatim method
keywords: how to, execute SQL query
keywords: SQL query, executing
keywords: SQL, executing query
keywords: programs, embedded SQL

---

Overloaded method to execute a SQL query with the SQL statement exactly as contained in the original legacy source code. A System.Collections.Generic.Dictionary is returned representing the results where you can access columns by name.

#### Overloaded List
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th>Description</th>
          </tr>

          <tr>
            <td>[
            ExecuteSQL_QueryVerbatim ( *string)* ](amfProgramClassExecuteSQL_QueryVerbatimMethod3.html)
              <em />
            </td>
            <td>Executes a SQL query
          specifying the SQL statement.</td>
          </tr>
          <tr>
            <td>[
            ExecuteSQL_QueryVerbatim ( *string, DBParm[ ]* )](amfProgramClassExecuteSQL_QueryVerbatimMethod1.html)
            </td>
            <td>Executes a SQL query
          specifying the SQL statement and statement
          parameters.</td>
          </tr>
          <tr>
            <td>[
            ExecuteSQL_QueryVerbatim ( *DbConnection, string)* ](amfProgramClassExecuteSQL_QueryVerbatimMethod4.html)
              <em />
            </td>
            <td>Executes a SQL
          query specifying the database connection and
          SQL statement.</td>
          </tr>
          <tr>
            <td>[
            ExecuteSQL_QueryVerbatim ( *DbConnection, string, DBParm[ ]* )](amfProgramClassExecuteSQL_QueryVerbatimMethod2.html)
            </td>
            <td>Executes a SQL
          query specifying the database connection, SQL
          statement, and statement parameters.</td>
          </tr>
</table>

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
[Program Class](amfProgramClass.html)<br />[Program Class Members](amfProgramClassMembers.html)<br />[Program.DBParm Class](amfProgramDBParmClass.html)<br />[ASNA.Monarch Namespace](amfMonarchNamespace.html)<br />[Embedded SQL Overview](amfconSQLStatementExamples.html)
