---
title: Program.SqlQueryResults Field

Id: amfProgramClassSqlQueryResultsField
TocParent: amfProgramClassFields
TocOrder: 20

keywords: SqlQueryResults field
keywords: Program.SqlQueryResults field
keywords: SQL, nonquery results
keywords: SQL nonquery, results
keywords: SQL statement, results
keywords: SQL, statement results
keywords: how to, SQL results
keywords: programs, embedded SQL

---

This field contains a collection representing the query results.

#### Syntax
<pre class="syntax"> **BegProp SqlQueryResults Access(*Public)Type(System.Collections.Generic.Dictionary)** </pre>

#### Field Value
**System.collections.Generic.Dictionary** . A collection representing the query results (string and object) allowing values for a particular column to be accessed by names.

#### Example
The following legacy source:
<pre class="libCScode">
0296.00     C/EXEC SQL
0297.00     C+ Select wddate, wdseq#, wdemp# Into :F1Date, :F1Seq#,:F1Emp#
0298.00     C+ From wfmmst Join wfmdet On wmemp# = wdemp#
0299.00     C+ Where wdmsc4 &lt;&gt; 'A' and wdetim = 0 and wdord#= :F1Ord# and
0300.00     C+       wdmsc1 = 'P'
0301.00     C/END-EXEC
</pre>

#### Generates
<pre class="example">
SqlQueryResults = ExecuteSQL_Query ( +
"Select wddate, wdseq#, wdemp#                          " + +
" From wfmmst Join wfmdet On wmemp# = wdemp#"  + + 
" Where wdmsc4 &lt;&gt;  'A' and wdetim = 0 and wdord# = @sql_parm_1 and" + +
"       wdmsc1 = 'P';", + 
 *New DBStrParm(DbType.String, F1Ord#, %Len (F1Ord#)) + 
)
F1Date = SqlQueryResults["WDDATE"] *AsFld F1Date
F1Seq# = SqlQueryResults["WDSEQ#"] *AsFld F1Seq#
F1Emp# = SqlQueryResults["WDEMP#"] *AsFld F1Emp#
</pre>

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
[Program Class](amfProgramClass.html) <br /> [Program Class Members](amfProgramClassMembers.html) <br /> [ Program.DBParm Class](amfProgramDBParmClass.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
