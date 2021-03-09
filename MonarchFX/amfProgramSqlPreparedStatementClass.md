---
title: Program.SqlPreparedStatement Class

Id: amfProgramSqlPreparedStatementClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 210

keywords: Program.SqlPreparedStatement class, about Program.SqlPreparedStatement class
keywords: Program.SqlPreparedStatement class
keywords: classes [ASNA.Monarch], Program.SqlPreparedStatement class
keywords: SQL prepared statement
keywords: SQL, prepared statement

---

The **Program.SqlPreparedStatement** is a nested class representing a prepared executable version of a SQL command statement.

For a list of all members of this type, see [ Program.SqlPreparedStatement Class Members](amfProgramSqlPreparedStatementClassMembers.html).

#### Inheritance Hierarchy
<pre>[ASNA.Monarch](amfMonarchNamespace.html)
    [ASNA.Monarch.Program](amfProgramClass.html)
 **ASNA.Monarch.Program.SqlPreparedStatement**       </pre>

#### Syntax
<pre class="syntax"> **BegClass Program.SqlPreparedStatement Access(public) Inherits (ASNA.Monarch.Program)**       </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
When a PREPARE statement is executed, the statement string is parsed and checked for errors. If the statement is valid, a prepared statement is created. A prepared statement can then be executed multiple times within the scope of the source program in which it is defined.

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
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [ Program.SqlPreparedStatement Class Members](amfProgramSqlPreparedStatementClassMembers.html) <br /> [Program Class](amfProgramClass.html) <br /> [ Program.SqlQueryResults Field](amfProgramClassSqlQueryResultsField.html) <br /> [ Program.DBParm Class](amfProgramDBParmClass.html) <br /> [ Embedded SQL Overview](amfconSQLStatementExamples.html) 
