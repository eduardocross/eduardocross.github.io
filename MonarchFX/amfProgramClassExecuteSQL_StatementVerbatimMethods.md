---
title: Program.ExecuteSQL_StatementVerbatim Methods

Id: amfProgramClassExecuteSQL_StatementVerbatimMethods
TocParent: amfProgramClassMethods
TocOrder: 60

keywords: ExecuteSQL_StatementVerbatim method
keywords: Program.ExecuteSQL_StatementVerbatim method
keywords: how to, execute SQL statement
keywords: SQL nonquery
keywords: SQL statement, executing
keywords: SQL, executing statement
keywords: SQL, nonquery
keywords: programs, embedded SQL

---

Overloaded method to execute a SQL command statement with the SQL statement exactly as contained in the original legacy source code.

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
            ExecuteSQL_StatementVerbatim (
 *string)* ](amfProgramClassExecuteSQL_StatementVerbatimMethod3.html)

            </td>
            <td>Executes the
          SQL command statement specified.</td>
          </tr>
          <tr>
            <td>[
            ExecuteSQL_StatementVerbatim (
 *string, DBParm[]* )](amfProgramClassExecuteSQL_StatementVerbatimMethod1.html)
            </td>
            <td>Executes a SQL command
          statement specifying the SQL statement and statement
          parameters.</td>
          </tr>
          <tr>
            <td>[
            ExecuteSQL_StatementVerbatim (
 *DbConnection, string)* ](amfProgramClassExecuteSQL_StatementVerbatimMethod4.html)
              <em />
            </td>
            <td>Executes a SQL command
          statement specifying the database connection
          and SQL statement.</td>
          </tr>
          <tr>
            <td>[
            ExecuteSQL_StatementVerbatim (
 *DbConnection, string, DBParm[]* )](amfProgramClassExecuteSQL_StatementVerbatimMethod2.html)
            </td>
            <td>Executes a SQL command
          statement specifying the database connection,
          SQL statement, and statement parameters.</td>
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
