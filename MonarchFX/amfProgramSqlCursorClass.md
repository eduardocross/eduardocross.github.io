---
title: Program.SqlCursor Class

Id: amfProgramSqlCursorClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 200

keywords: Program.SqlCursor class, about Program.SqlCursor class
keywords: Program.SqlCursor class
keywords: classes [ASNA.Monarch], Program.SqlCursor class
keywords: SQL cursor
keywords: SQL, cursor

---

The **Program.SqlCursor** is a nested class representing a SQL cursor for a multi-row dataset on which the cursor methods operate.

For a list of all members of this type, see [ Program.SqlCursor Class Members](amfProgramSqlCursorClassMembers.html).

#### Inheritance Hierarchy
<pre>[ASNA.Monarch](amfMonarchNamespace.html)
    [ASNA.Monarch.Program](amfProgramClass.html)
 **ASNA.Monarch.Program.SqlCursor** </pre>

#### Syntax
<pre class="syntax"> **BegClass Program.SqlCursor Access(public) Inherits (ASNA.Monarch.Program)** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
When the query is done using a cursor, the set of rows returned consists of all the rows that satisfy the conditions in the WHERE clause of the statement. As long as the cursor remains open, the logic can scroll via [Fetch](amfProgramSqlCursorClassFetchMethod.html) to get data-rows from the result set.

This is in contrast to the single-row ExecuteSQL_Query, which results in only one data row that matches the search criteria.

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

#### See Also
<dl>
        <dd>[ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
        <dd>[
        Program.SqlCursor Class Members](amfProgramSqlCursorClassMembers.html)</dd>
        <dd>[Program
        Class](amfProgramClass.html)</dd>
        <dd>[
        Program.SqlQueryResults Field](amfProgramClassSqlQueryResultsField.html)</dd>
       <dd>[
        Program.DBParm Class](amfProgramDBParmClass.html)</dd>
       <dd>[
        Embedded SQL Overview](amfconSQLStatementExamples.html)</dd>
</dl>

