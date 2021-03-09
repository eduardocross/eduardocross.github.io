---
title: Program.SqlCursor.SqlQueryResultsByIndex Method

Id: amfProgramSqlCursorClassSqlQueryResultsByIndexMethod
TocParent: amfProgramSqlCursorClassMethods
TocOrder: 40

keywords: SqlQueryResultsByIndex method
keywords: SqlCursor.SqlQueryResultsByIndex method
keywords: Program.SqlCursor.SqlQueryResultsByIndex method
keywords: SQL, query results by cursor index
keywords: SQL cursor, query results by cursor index
keywords: how to, SQL query results by cursor index

---

Returns an object from the SqlCursor result set by index.

#### Syntax
<pre class="syntax"> **BegFunc SqlCursor.SqlQueryResultsByIndex Access(*Public) Type(Object)
        DclSrParm *index*  Type (*Integer)**       </pre>

#### Parameters
<dl>
        <dt>
 *index* 
        </dt>
        <dd>A reference to an instance of a row in the query
        results set.</dd>
</dl>

#### Returns
SqlCursor object referred to by the index.

#### Example
Assumes SqlCursor **SelF1CSR** already declared and opened.
<pre class="libCScode">
0337.00   C/EXEC SQL
0338.00   C+ SqlQueryResultsByIndex NEXT FROM SelF1CSR
0339.00   C+ INTO :F1DATE, :F1ORD#, :F1SEQ#, F1EMP#, :F1WFGR, :F1DIST
0340.00   C/END-EXEC</pre>

The following migrated code is generated for just the statement above:
<pre class="syntax"> If (SelF1CSR.SqlQueryResultsByIndex(ASNA.Monarch.PRogram.SqlCursor.SqlQueryResultsByIndexOrientations.Next) )
    F1DATE = SelF1CSR.SqlQueryResultsByIndex(0) *AsFld F1DATE
    F1ORD# = SelF1CSR.SqlQueryResultsByIndex(1) *AsFld F1ORD#
    F1SEQ# = SelF1CSR.SqlQueryResultsByIndex(2) *AsFld F1SEQ#
    F1EMP# = SelF1CSR.SqlQueryResultsByIndex(3) *AsFld F1EMP#
    F1WFGR = SelF1CSR.SqlQueryResultsByIndex(4) *AsFld F1WFGR
    F1DIST = SelF1CSR.SqlQueryResultsByIndex(5) *AsFld F1DIST
 EndIf </pre>

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
[ Program.SqlCursor Class](amfProgramSqlCursorClass.html) <br /> [ Program.SqlCursor Class Members](amfProgramSqlCursorClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
