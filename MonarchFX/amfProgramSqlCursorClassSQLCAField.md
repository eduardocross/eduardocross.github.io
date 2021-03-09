---
title: Program.SqlCursor.SQLCA Field

Id: amfProgramSqlCursorClassSQLCAField
TocParent: amfProgramSqlCursorClassFields
TocOrder: 30

keywords: SQLCA field
keywords: SqlCursor.SQLCA field
keywords: Program.SqlCursor.SQLCA field
keywords: SQL, SQLCA
keywords: SQL cursor, SQLCA
keywords: SQLCA

---

[ SQL_CommunicationsArea](amfProgramSQL_CommunicationsAreaClass.html) object that represents the SQLCA to trap and report run-time errors for the **SqlCursor** .

#### Syntax
<pre class="syntax">
 **BegProp SQLCA Access(*Public) Type(SQL_CommunicationsArea)**       </pre>

#### Field Value
[ SQL_CommunicationsArea](amfProgramSQL_CommunicationsAreaClass.html) object that represents the SQLCA to trap and report run-time errors for the **SqlCursor** .

#### Example
Assumes SqlCursor **SelF1CSR** already declared and opened.
<pre class="libCScodee">
0337.00   C/EXEC SQL
0338.00   C+ FETCH NEXT FROM SelF1CSR
0339.00   C+ INTO :F1DATE, :F1ORD#, :F1SEQ#, F1EMP#, :F1WFGR, :F1DIST
0340.00   C/END-EXEC
0341.00   C                   If        SQLCOD = 0
 success - do something 0345.00                       Else
 failure - exit 0347.00                       Leave</pre>

The following migrated code is generated for the statement above:
<pre class="prettyprint">If ( SelF1CSR.Fetch(SqlCursor.FetchOrientations.Next ) )
    F1DATE = SelF1CSR.SqlQueryResultsByIndex(0) *AsFld F1DATE
    F1ORD# = SelF1CSR.SqlQueryResultsByIndex(1) *AsFld F1ORD#
    F1SEQ# = SelF1CSR.SqlQueryResultsByIndex(2) *AsFld F1SEQ#
    F1EMP# = SelF1CSR.SqlQueryResultsByIndex(3) *AsFld F1EMP#
    F1WFGR = SelF1CSR.SqlQueryResultsByIndex(4) *AsFld F1WFGR
    F1DIST = SelF1CSR.SqlQueryResultsByIndex(5) *AsFld F1DIST
EndIf
SQLCA = SelF1CSR.SQLCA
If (SQLCA.SQLCOD = 0)
     sucecss - do something
     Else  
     failure - exit
EndIf</pre>

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
