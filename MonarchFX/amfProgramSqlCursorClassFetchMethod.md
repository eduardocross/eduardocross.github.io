---
title: Program.SqlCursor.Fetch Method

Id: amfProgramSqlCursorClassFetchMethod
TocParent: amfProgramSqlCursorClassMethods
TocOrder: 20

keywords: Fetch method
keywords: SqlCursor.Fetch method
keywords: Program.SqlCursor.Fetch method
keywords: SQL, fetching cursor
keywords: SQL cursor, fetching
keywords: how to, fetch SQL cursor
keywords: enumerations [ASNA.Monarch], Program.SqlCursor.FetchOrientations, used by
keywords: Program.SqlCursor.FetchOrientations enumeration, used by

---

Determines if results are available and conditions the lines that retrieve the query results by the [ SqlCursor.FetchOrientations](amfProgramSqlCursorFetchOrientationsEnumeration.html) value.

#### Syntax
<pre class="syntax"> **BegFunc SqlCursor.Fetch Access(public) Type(Boolean)
   DclSrParm *orientation*  Type(SqlCursor.FetchOrientations)**       </pre>

#### Parameters
<dl>
        <dt>
 *orientation* 
        </dt>
        <dd>
          [
        SqlCursor.FetchOrientations](amfProgramSqlCursorFetchOrientationsEnumeration.html) enumeration value defining
        the orientation of the cursor for the fetch.</dd>
</dl>

#### Returns
**Boolean** . *True indicates results are available; *False indicates the results are *Nothing.

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="50%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th>
           <th>Condition</th>
          </tr>
          <tr>
            <td>UnsupportedOperationException</td>
            <td>The operation has not yet
            been implemented.</td>
          </tr>
</table>

#### Example
Assumes SqlCursor **SelF1CSR** already declared and opened.
<pre class="syntax">
0337.00   C/EXEC SQL
0338.00   C+ FETCH NEXT FROM SelF1CSR
0339.00   C+ INTO :F1DATE, :F1ORD#, :F1SEQ#, F1EMP#, :F1WFGR,
:F1DIST
0340.00   C/END-EXEC
</pre>

The following migrated code is generated for just the statement above:
<pre class="syntax"><span style="color:blue">If</span> ( SelF1CSR.Fetch(SqlCursor.FetchOrientations.Next ) )
    F1DATE = SelF1CSR.SqlQueryResultsByIndex(0) <span style="color:blue">*AsFld</span> F1DATE
    F1ORD# = SelF1CSR.SqlQueryResultsByIndex(1) <span style="color:blue">*AsFld</span> F1ORD#
    F1SEQ# = SelF1CSR.SqlQueryResultsByIndex(2) <span style="color:blue">*AsFld</span> F1SEQ#
    F1EMP# = SelF1CSR.SqlQueryResultsByIndex(3) <span style="color:blue">*AsFld</span> F1EMP#
    F1WFGR = SelF1CSR.SqlQueryResultsByIndex(4) <span style="color:blue">*AsFld</span> F1WFGR
    F1DIST = SelF1CSR.SqlQueryResultsByIndex(5) <span style="color:blue">*AsFld</span> F1DIST
<span style="color:blue">EndIf</span></pre>

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
        <dd>[
        Program.SqlCursor Class](amfProgramSqlCursorClass.html)</dd>
        <dd>[
        Program.SqlCursor Class Members](amfProgramSqlCursorClassMembers.html)</dd>
        <dd>[
        Program.SqlCursor.FetchOrientations Enumeration](amfProgramSqlCursorFetchOrientationsEnumeration.html)</dd>
        <dd>[ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
</dl>

