---
title: SQL Migration Overview

Id: amfconSQLStatementExamples
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 200

keywords: SQL
keywords: SQL, migration overview
keywords: migration, overview for embedded SQL
keywords: SQL, examples
keywords: ASNA.Monarch, SQL migration overview
keywords: ASNA.Monarch, SQL examples

---

This topic contains three sections &#8211; an Overview, Examples, and Framework Support. The Overview provides detailed statements of what happens to embedded SQL when it is migrated. The examples in this section show only snippets of code to demonstrate the statement.

The Examples have complete legacy source and migrated code more fully reflecting the statements from the Overview section.

The Framework Support shows the classes and details of note (with links) provided to support the migration of the embedded SQL.

#### Overview

1. The RPG Agent assumes an ODBC driver for database connection when migrating the code. There are four statements (in <code>MyJob.vr</code>) that define the connection field and the driver connection string (<code>connectStr</code>), and then establish the connection. For example:
<div><pre class="example">1) <span style="COLOR: #0000ff">DclFld</span> ADO_Connection <span style="COLOR: #0000ff">Type</span>(System.Data.Odbc.OdbcConnection) <span style="COLOR: #0000ff">Access</span>(*Public)</pre>
						<pre class="example">2) <span style="COLOR: #0000ff">DclFld</span> connectStr <span style="COLOR: #0000ff">Type</span>(*String)
   connectStr = string.Format(&quot;Driver={{Client Access ODBC Driver (32-bit)}};&quot; + +
	             &quot;System={0};DBQ={1},*USRLIBL;Uid={2};Pwd={3}&quot;, +
	             MyDatabase.Server, +
	             MyDatabase.DBName, +
	             MyDatabase.User,	+
	             /* Add your password here /*)</pre>
						<pre class="example">3) ADO_Connection = <span style="COLOR: #0000ff">*New</span> System.Data.Odbc.Odbc.Connection(connectStr)</pre>

In <code>MyJob.vr</code>, the RPG Agent will place messages showing the replacement values when using MS SQL Server (instead of ODBC). Basically, when using MS SQL Server, the same statements will read as follows:
<div><pre class="example">1) <span style="COLOR: #0000ff">DclFld</span> ADO_Connection <span style="COLOR: #0000ff">Type</span>( **System.Data.SwlClient.SqlConnection** ) <span style="COLOR: #0000ff">Access</span>(*Public)</pre>
						<pre class="example">2) <span style="COLOR: #0000ff">DclFld</span> connectStr <span style="COLOR: #0000ff">Type</span>(*String)
   connectStr = string.Format(&quot; **Data Source={0};Initial Catalog={1};Integrated Security=True** &quot;)</pre>
						<pre class="example">3) ADO_Connection = <span style="COLOR: #0000ff">*New</span> **System.Data.SqlClient.SqlConnection** (connectStr)</pre>
2. The SQL Commands directly supported are: <code> *PREPARE* </code>, <code> *DECLARE CURSOR* </code>, <code> *SELECT* </code>, <code> *OPEN CURSOR* </code>, <code> *CLOSE CURSOR* </code>, <code> *FETCH* </code>, <code> *INSERT* </code>, <code> *DELETE* </code>, and <code> *UPDATE* ></code>.
3. A &quot;query&quot; is migrated using one of the <code>ExecuteSQL_Query</code> methods (<code>SqlQueryResults</code> is the result set) while all other &quot;non-query&quot; SQL commands are migrated using the ExecuteSQL_Statement methods.
4. When <code> *WHERE* </code> clause host variables are used, the variable name in the legacy source is replaced within the migrated statement with a monarch-generated name as: <code> *&quot;@sql_parm_n* "</code> where <code> *n* </code> is a sequence number of the parameter in the original statement i.e. *<code>@sql_parm_1</code>* , <code> *@sql_parm_2,* </code> etc. The host variables&#39; values are then passed to the methods as a collection of parameters using instances of DBParm, DBStrParm, or DBScaledParm classes.

For example, <span style="background: lightgrey"><code> *WHERE wddate = :ODATE# and wdemp# = :F1EMP#* </code></span> is migrated as shown below. Notice the two parameters <code>@sql_parm_1</code> and <code>@sql_parm_2</code> in the statement defined with <code>DBParm</code> and <code>DBScaledParm</code> respectively.
<div><pre class="example"> . . .( + 
&quot;WHERE wddate = @sql_parm_1 and wdemp# = @sql_parm_2;&quot;, + +
. . .   
<span style="color:blue">*New</span> DBParm(DbType.Time, ODATE#),
<span style="color:blue">*New</span> DBScaledParm(DbType.Decimal, F1EMP#, <span style="color:blue">%Len</span>(F1EMP#), <span style="color:blue">%DecPos</span>(F1EMP#))
 ) </pre>
5. <code> *INSERT* </code> clause host variables are handled the same as host variables in the <code> *WHERE* </code> clause.
6. When the <code> *SELECT* </code> clause has host variables, the variables&#39; values are converted to string and concatenated as part of the <code>SELECT</code> statement.

For example, <span style="background: lightgrey"> *SELECT :#TgtDate, :F4EMP#, WDORD#* </span> is migrated as shown below. Notice how the two variables&#39; values are converted to string using the built in function <code>%Char</code> when they are concatenated to the <code>SELECT</code> statement.
<div><pre class="example">SqlQueryResults = ExecuteSQL_Query ( +
&quot;SELECT &quot; + <span style="color:blue">%Char</span>(#TgtDate) + &quot;, &quot; + <span style="color:blue">%Char</span>(F4EMP#) + &quot;, WDORD#, +
. . . ) </pre>
7. When the <code>INTO</code> keyword is used, the <code>INTO</code> section of the statement is removed and the values are propagated from the query results.

For example, <code><span style="background: lightgrey"> *SELECT wddate, wdseq# INTO :F1DATE, :F1SEQ#* </span></code> is migrated as shown below. 
<div><pre class="example">SqlQueryResults =  ExecuteSQL_Query ( +
&quot;SELECT wddate, wdseq#                         &quot; +
 . . . )
F1DATE = SqlQueryResults[&quot;wddate&quot;] <span style="color:blue">*AsFld</span> F1DATE 
F1SEQ# = SqlQueryResults[&quot;wdseq#&quot;] <span style="color:blue">*AsFld</span> F1SEQ# </pre>
8. <code>SELECT</code> statements that have an expression (instead of a list of columns) are modified by inserting <code>&quot; *as SqlExprResultColumn* &quot;</code> so that a new column is added to the result table. You can access it using <code> *SqlQueryResults[&quot;SqlExprResultColumn&quot;]* </code>.

For example, <code><span style="background: lightgrey"> *SELECT IfNull(MAX(WDSEQ#),0)+1 INTO :F4SEQ#* </span></code> is migrated as shown below.
<div><pre class="example">SqlQueryResults = ExecuteSQL_Query ( +
&quot;SELECT IfNull(MAX(WDSEQ#),0)+1 as SqlExprResultColumn                      &quot;  + +
 . . . )
F4SEQ# = SqlQueryResults[&quot;SqlExprResultColumn&quot;] <span style="color:blue">*AsFld</span> F4SEQ#</pre>
9. The migration of a prepared statement is slightly more complex in that there are several commands to define the <code>SELECT</code> statement, prepare the statement, declare the cursor, open the cursor (execute the statement), fetch from the result set, and ultimately close the cursor. However, once a statement is prepared it can then be executed multiple times within the scope of the source program. For simplicity, each of the following statements is taken individually as it relates to prepared statements.

For example, <code><span style="background: lightgrey"> SelectF1 = &#39;select wddate, wdord#, wdseq# </span>&#39;</code> is migrated in a straightforward manner as shown below.
<code><pre class="example">SelectF1 = &#39;select wddate, wdord#, wdseq# &#39; </pre></code>

For example, <code><span style="background: lightgrey">PREPARE SelF1 FROM :SelectF1</span></code> is migrated as shown below. Notice how <code>SelF1</code> is declared as <code>Type(SqlPreparedStatement)</code> then instanced with the connection and select statement (<code>SelectF1</code>). 
<pre class="example"><span style="COLOR: blue">DclFld</span> SelF1 <span style="COLOR: blue">Type</span>(SqlPreparedStatement) 
SelF1 = <span style="COLOR: blue">*New</span> SqlPreparedStatement( monarchJob.ADO_Connection, SelectF1 ) </pre>

For example, <span style="background: lightgrey"> DECLARE SelF1CSR SCROLL CURSOR FOR SELF1</span> is migrated as shown below. Notice how SelF1CSR is declared as Type(SqlCursor) then instanced with the connection and prepared statement (SELF1). A scroll type is then assigned.
<pre class="example"><span style="COLOR: blue">DclFld</span> SelF1CSR <span style="COLOR: blue">Type</span>(SqlCursor) 
SelF1CSR = <span style="COLOR: blue">*New</span> SqlCursor( monarchJob.ADO_Connection, SELF1 ) 
SelF1CSR.ScrollType = SqlCursor.ScrollTypes.Scrollable </pre>

For example, <code><span style="background: lightgrey"> OPEN SelF1CSR</span></code> is migrated as shown below. The OPEN executes the SQL statement. The cursor (<code>SelF1CSR</code>) has its own <code>SQLCA</code>, which is assigned to the global <code>SQLCA</code> so any testing of <code>SQLCA.SQLCOD</code> will still work. Although not shown, the RPG Agent will automatically qualify references to <code>SQLCOD</code> as <code>SQLCA.SQLCOD</code> since <code>SQLCA</code> is an instance of a class, and <code>SQLCOD</code> is a member field of <code>SQLCA</code>. 
<pre class="example">SelF1CSR.Open()
SQLCA = SelF1CSR.SQLCA </pre>

For example, <code><span style="background: lightgrey"> FETCH NEXT FROM SelF1CSR INTO :F1DATE, :F1ORD#, :F1SEQ#</span></code> is migrated as shown below. Notice how SelF1CSR.Fetch, which returns true when results are available, conditions the statements that retrieve the results preventing a program from accessing SqlQueryResults which is invalid (<code>*nothing</code>) when the <code>FETCH</code> is unsuccessful.
<pre class="example"><span style="color:blue">If</span> ( SelF1CSR.Fetch( SqlCursor.FetchOrientations.Next ) )
   F1DATE = SelF1CSR.SqlQueryResultsByIndex( 0 ) <span style="COLOR: blue">*AsFld</span> F1DATE
   F1ORD# = SelF1CSR.SqlQueryResultsByIndex( 1 ) <span style="COLOR: blue">*AsFld</span> F1ORD# 
   F1SEQ# = SelF1CSR.SqlQueryResultsByIndex( 2 ) <span style="COLOR: blue">*AsFld</span> F1SEQ# 
<span style="COLOR: blue">EndIf
</span>SQLCA = SelF1CSR.SQLCA </pre>

Notice how after the Fetch runs, the resulting data is retrieved using the name of the cursor <code>(SelF1CSR) + &quot;.&quot; + SqlQueryResultsByIndex</code> instead of the global <code>SqlQueryResults</code> (used for single-row queries). Each instance of <code>SqlCursor</code> class keeps its own <code>SqlQueryResults</code> collections, making it possible to use more than one cursor at a time while keeping the result datasets independent. The access by <code>Index</code> as opposed to by name (as it is done when migrating single-row) is just a migration simplicity for the convenience of the RPG Agent, since the named collection used while preparing or creating the cursor may be out of scope.

Closing the cursor, which in the legacy source is: <code><span style="background: lightgrey"> CLOSE SelF1CSR</span></code>, now becomes
<pre class="example">SelF1CSR.Close</pre>

All other SQL commands not mentioned in number 1 will be blindly migrated as <code>&quot;ExecuteSQL_Statement (statement)&quot;</code>. No attempt will be made to look for host-variables and no migration task will be produced (it is up to the data provider&#39;s implementation to accept or reject the request at application runtime).

#### Example 1
The following legacy source example shows three host variables:
<pre class="syntax">C/EXEC SQL
C+ DELETE FROM DEPARTMENT
C+  WHERE WDDATE = :ODATE# and WDEMP# = :F1EMP# and
C+        WDORD# = :F1ORD#
C/END-EXEC</pre>

The following migrated code using <code> **DBParm** , **DBStrParm** </code>, or <code> **DBScaledParm** </code> to pass the value for the three host variables. 
<pre class="example">ExecuteSQL_Statement ( +
&quot;DELETE FROM DEPARTMENT 
 WHERE WDDATE = @sql_parm_1 and WDEMP# = @sql_parm_2 +
 WDORD = @sql_parm_3;&quot;, +
<span style="color:blue">*New</span>  DBParm(DbType.Time, ODATE#), + 
<span style="color:blue">*New</span>  DBScaledParm(DbType.Decimal, F1EMP#, <span style="color:blue">%Len</span>(F1EMP#), <span style="color:blue">%DecPos</span>(F1EMP#)), +
<span style="color:blue">*New</span>  DBStrParm(DbType.String, F1ORD#, <span style="color:blue">%Len</span>(F1ORD#) + 
)</pre>

#### Example 2
The following legacy source has the <code> **Into** </code> keyword removed from the <code>Select</code> statement and replaced with blanks. The host variables are saved and used after executing the statements to retrieve their values as shown:
<pre class="syntax">C/EXEC SQL
C+ Select WDDATE, WDSEQ#, WDEMP# Into :F1Date, :F1Seq#, :F1Emp#
C+ From wfmmst Join wfmdet On wmemp# = wdemp#
C+ Where wdmsc4 &lt;&gt; &#39;A&#39; and wdetim = 0 and wdord# = :F1Ord# and
C+       wdmsc1 = &#39;P&#39;
C/END-EXEC</pre>

This migrated code is generated. 
<pre class="example">SqlQueryResults = ExecuteSQL_Query ( +
&quot;Select WDDATE, WDSEQ#, WDEMP#                          &quot; + +
&quot; From wfmmst Join wfmdet On wmemp# = wdemp#&quot;  + + 
&quot; Where wdmsc4 &lt;&gt;  &#39;A&#39; and wdetim = 0 and wdord# = @sql_parm_1 and&quot; + +
&quot;       wdmsc1 = &#39;P&#39;;&quot;, +
<span style="color:blue">*New</span>  DBStrParm(DbType.String, F1Ord#, <span style="color:blue">%Len</span>(F1Ord#)) + 
)
F1Date = SqlQueryResults[&quot;WDDATE&quot;] <span style="color:blue">*AsFld</span> F1Date
F1Seq# = SqlQueryResults[&quot;WDSEQ#&quot;] <span style="color:blue">*AsFld</span> F1Seq#
F1Emp# = SqlQueryResults[&quot;WDEMP#&quot;] <span style="color:blue">*AsFld</span> F1Emp#</pre>

Select statements that have an expression instead of a list of columns, such as <code> **Count(*)** </code>, are modified by inserting <code>&quot;as *SqlExprResultColumn* &quot;</code> so that a new column is added to the result table, which can be accessed using <code>SqlQueryResults[&quot;SqlExprResultColumn&quot;]</code> shown in the following example:
<pre class="syntax">C/EXEC SQL
C+ Select **Count(*)** 
C+ Into :#Count
C+ From wfmmst Join wfmdet
C+ On   wmemp# = wdemp#
C+ Where wdmsc4 &lt;&gt; &#39;A&#39; and wdetim = 0 and wdosst = &#39; &#39; and
C+       wdord# = :F1Ord#
C/END-EXEC</pre>

This migrated code is generated as: 
<pre class="example">SqlQueryResults = ExecuteSQL_Query ( +
&quot;Select **Count(*)**  **as SqlExprResultColumn**  &quot; + +
&quot;               : ++
&quot; From wfmmst Join wfmdet&quot;  + + 
&quot; Where wdmsc4 &lt;&gt;  &#39;A&#39; and wdetim = 0 and wdosst = &#39;&#39;  and&quot; + +
&quot;       wdord# = @sql_parm_1;&quot;, +
<span style="color:blue">*New</span>  DBStrParm(DbType.String, F1Ord#, <span style="color:blue">%Len</span>(F1Ord#)) + 
)
#Count = **SqlQueryResults[&quot;SqlExprResultColumn&quot;]**   <span style="color:blue">*AsFld</span> #Count</pre>

#### Example 3
<pre class="syntax">C/EXEC SQL 
C+ DECLARE Cursor1
C+ INSENSITIVE     SCROLL CURSOR
C+ WITHOUT HOLD WITH RETURN
C+ FOR 
C+ SELECT FLD1, FLD2, FLD3 
C+     FROM
C+        TBLA, TBLB
C+     WHERE
C+         :PARAM1 &lt; KEY1 AND
C+         :PARAM2 LIKE &quot;AAAA&quot; AND
C+         :PARAM3 &lt; KEY2
C+     ORDER BY 
C+         TBLA DESC
C+     FETCH FIRST 2 ROWS ONLY
C+     OPTIMIZE FOR 2 ROWS
C+     WITH RR 
C/END-EXEC</pre>

This migrated code is generated. 
<pre class="example"><span style="COLOR: red">/Error Unsupported: &quot;INSENSITIVE&quot; CURSOR qualifier not supported for DECLARE CURSOR.
/Error Unsupported: &quot;WITHOUT HOLD&quot; CURSOR qualifier not supported for DECLARE CURSOR.
/Error Unsupported: &quot;WITH RETURN&quot; CURSOR qualifier not supported for DECLARE CURSOR.</span>
 <span style="COLOR: blue">DclFld</span> Cursor1 <span style="COLOR: blue">Type</span>(SqlCursor)
 Cursor1 = <span style="COLOR: blue">*New</span> SqlCursor( monarchJob.ADO_Connection, &quot;SELECT FLD1, FLD2, FLD3&quot; + +
 &quot;     FROM&quot; + +
 &quot;        TBLA, TBLB&quot; + +
 &quot;     WHERE&quot; + +
 &quot;         @sql_parm_1 &lt; KEY1 AND&quot; + +
 &quot;         @sql_parm_2 LIKE &#39;AAAA&#39; AND&quot; + +
 &quot;         @sql_parm_3 &lt; KEY2&quot; + +
 &quot;     ORDER BY&quot; + +
 &quot;         TBLA DESC&quot; + +
 &quot;     FETCH FIRST 2 ROWS ONLY&quot; + +
 &quot;     OPTIMIZE FOR 2 ROWS&quot; + +
 &quot;     WITH RR;&quot;, 
 <span style="COLOR: blue">*New</span>  DBStrParm(DbType.String, PARAM1, <span style="COLOR: blue">%Len</span>(PARAM1)), +
 <span style="COLOR: blue">*New</span>  DBStrParm(DbType.String, PARAM2, <span style="COLOR: blue">%Len</span>(PARAM2)), +
 <span style="COLOR: blue">*New</span>  DBStrParm(DbType.String, PARAM3, <span style="COLOR: blue">%Len</span>(PARAM3))  +
 )
 Cursor1.ScrollType = SqlCursor.ScrollTypes.Scrollable</pre>

#### Example 4 &#8211; Prepared Statement
The following segments of legacy code (where <code>&quot;SelectF1&quot;</code> is a <code>*Char len(500)</code>) dynamically assigned to a valid <code>SELECT</code> quoted statement.
<pre class="syntax">C/EXEC SQL
C+ **PREPARE**  SelF1 **FROM**  :SelectF1
C/END-EXEC
C* Declare the SQL cursor to hold the data retrieved from the SELECT
C/EXEC SQL
C+ **DECLARE**  SelF1CSR SCROLL **CURSOR**  FOR SELF1
C/END-EXEC 
C* Open the SQL cursor. 
C/EXEC SQL
C+ **OPEN**  SelF1CSR
C/END-EXEC
C* Process the records in the SQL cursor until the return not = 0 
C                   Do        SubfilePage
C* 
C* Get the next row from the SQL cursor. 
C/EXEC SQL 
C+ **FETCH**  NEXT **FROM**  SelF1CSR 
C+ **INTO**  :F1DATE, :F1ORD#, :F1SEQ#, :F1EMP#, :F1WFGR, :F1DIST 
C/END-EXEC
C*
C                   If        SQLCOD = 0 
                         <span style="color:gray">Success - do something</span> 
C                   Else
                         <span style="color:gray">Failure, exit loop</span>  
C                   Leave 
C                   EndDo 
C/EXEC SQL 
C+ CLOSE SelF1CSR
C/END-EXEC
</pre>

Generates this migrated code: 
<pre class="prettyprint">Error: Validation of dynamic SQL statement using host variables delayed until run-time. Please review migrated code.
DclFld SelF1 Type(SqlPreparedStatement)
SelF1 = *New SqlPreparedStatement( monarchJob.ADO_Connection, SelectF1 )
//* Declare the SQL cursor to hold the data retrieved from the SELECT
DclFld SelF1CSR Type(SqlCursor)
SelF1CSR = *New SqlCursor( monarchJob.ADO_Connection, SELF1 )
SelF1CSR.ScrollType = SqlCursor.ScrollTypes.Scrollable
//* Open the SQL cursor.
SelF1CSR.Open()
//* Process the records in the SQL cursor until the return not = 0
DoToVal(SubfilePage)

//* Get the next row from the SQL cursor.
If ( SelF1CSR.Fetch( SqlCursor.FetchOrientations.Next ) )
     F1DATE = SelF1CSR.SqlQueryResultsByIndex( 0 ) *AsFld F1DATE
     F1ORD# = SelF1CSR.SqlQueryResultsByIndex( 1 ) *AsFld F1ORD#
     F1SEQ# = SelF1CSR.SqlQueryResultsByIndex( 2 ) *AsFld F1SEQ#
     F1EMP# = SelF1CSR.SqlQueryResultsByIndex( 3 ) *AsFld F1EMP#
     F1WFGR = SelF1CSR.SqlQueryResultsByIndex( 4 ) *AsFld F1WFGR
     F1DIST = SelF1CSR.SqlQueryResultsByIndex( 5 ) *AsFld F1DIST
EndIf
 SQLCA = SelF1CSR.SQLCA
If( SQLCA.SQLCOD = 0 )
       Success - do something           
Else
       Failure, exit loop         
EndIf
EndDo</pre>

#### Example 5 &#8211; INSERT
The following legacy source example shows an <code> **INSERT** </code>:
<pre class="syntax">C/EXEC SQL
C+ **INSERT**  INTO PRMPTP
C+ SELECT &#39;EMPLOYEE&#39; AS PRFLD, DIGITS(WMEMP#) AS PRVALU,
C+        WMNAME AS PRDESC
C+ FROM WFMMST
C+ WHERE EMEMP# &lt;&gt; :F1EMP#
C/END-EXEC</pre>

Migrates as: 
<pre class="example">ExecuteSQL_Statement ( + 
&quot;INSERT INTO PRMPTP&quot; + + 
&quot;SELECT &#39;EMPLOYEE&#39; AS PRFLD, DIGITS(WMEMP#) AS PRVALU,&quot; + + 
&quot;WMNAME        AS PRDESC&quot; + + 
&quot;WHERE WMEMP# &lt;&gt;  = @sql_parm_1;&quot;, +
<span style="color:blue">*New</span>  DBScaledParm(DbType.Decimal, F1EMP#, <span style="color:blue">%Len</span>(F1EMP#), <span style="color:blue">%DecPos</span>(F1EMP#)) +
)</pre>

The following legacy source example shows an <code> **INSERT** </code> with <code> **VALUES** </code> keyword:
<pre class="syntax">C/EXEC SQL
C+ **INSERT**  INTO SVCC
C+ (SCCSTS, SCCDO#, SCCDAT, SCCTIM, SCCOSC, SCCNSC, SCCUSR),
C+ **VALUES** (&#39; &#39;, :SvOrd#, :Msoedt, :#Time6, :Msostg, :@Stg, :Sdsusr
C/END-EXEC</pre>

Migrates as: 
<pre class="example">ExecuteSQL_Statement ( + 
&quot;INSERT INTO SVSCC&quot; + + 
&quot; (SCCSTS, SCCSO# SCCDAT, SCCTIM, SCCOSC, SCCNSC, SCCUSR)&quot; + +
&quot; VALUES(&#39; &#39;, @sql_parm_1, @sql_parm_2, @sql_parm_3, @sql_parm_4, @sql_parm_5, @sql_parm_6,;&quot; +
<span style="color:blue">*New</span> DBStrParm(DbType.String, System. SvOrd#, <span style="color:blue">%Len</span>(SvOrd#)), +
<span style="color:blue">*New</span>  DBScaledParm(DbType.Decimal, Msoedt, <span style="color:blue">%Len</span>(Msoedt), <span style="color:blue">%DecPos</span>(Msoedt)), +
<span style="color:blue">*New</span>  DBScaledParm(DbType.Decimal, #Time6, <span style="color:blue">%Len</span>(#Time6), <span style="color:blue">%DecPos</span>(#Time6)), +
<span style="color:blue">*New</span>  DBStrParm(DbType.String, Msostg, <span style="color:blue">%Len</span>(Msostg)), +
<span style="color:blue">*New</span>  DBStrParm(DbType.String, @Stg, <span style="color:blue">%Len</span>(@Stg)), +
<span style="color:blue">*New</span>  DBStrParm(DbType.String, Sdusr, <span style="color:blue">%Len</span>(Sdusr)) +
)</pre>

#### Example 6 Host Variable
This:
<pre class="syntax">C/EXEC SQL
C+ INSERT INTO WFMDET
C+ ( Select **:#TgtDate, :F4EMP#, :F4SEQ#,**  WDORD#, WDACTW,
C+         WDTIME, WDSTIM, WDETIM, WDSDTE, WDEDTE, WDASWU,
C+         &#39; &#39;, WDCTIM, WDCLDT, WDCLTM, WDASBY, WDASDT,
C+  . . .
C+ FROM WFMDET
C+ WHERE WDDATE = :#ODATE and WDEMP# = :F1EMP# and
C+       WDORD# = :F1ORD# and WDSEQ# = :F1SEQ#
C/END-EXEC</pre>

Migrates as: 
<pre class="example">ExecuteSQL_Statement ( + 
&quot;INSERT INTO WFMDET&quot; + + 
&quot; (Select **&quot; + %Char(#TgtDate) + &quot;, &quot; +%Char(F4EMP#) + &quot;, &quot; + %Char(F4SEQ#) + &quot;,**  WDORD#, WDACTW,&quot; + +
&quot;         WDTIME, WDSTIM, WDETIM, WDSDTE, WDEDTE, WDASWU,&quot; + +
&quot;         &#39; &#39;, WDCTIM, WDCLDT, WDCLTM, WDASBY, WDASDT,&quot; + +
&quot; . . .
&quot; FROM WFMDET&quot; + +
&quot; WHERE WDDATE = @sql_parm_1 and WDEMP# = @sql_parm_2 and&quot; + + 
&quot;       WDORD# = @sql_parm_3 and WDSEQ# = @sql_parm_4;&quot; +
<span style="color:blue">*New</span>  DBParm(DbType.Time, #ODATE), +
<span style="color:blue">*New</span>  DBScaledParm(DbType.Decimal, F1EMP#, <span style="color:blue">%Len</span>(F1EMP#), <span style="color:blue">%DecPos</span>(F1EMP#)), +
<span style="color:blue">*New</span>  DBStrParm(DbType.Decimal, F1ORD#, <span style="color:blue">%Len</span>(F1ORD#)), +
<span style="color:blue">*New</span>  DBScaledParm(DbType.String, 1SEQ#, <span style="color:blue">%Len</span>(F1SEQ#), <span style="color:blue">%DecPos</span>(F1SEQ#)), +
)</pre>

#### Framework Support
<table class="mytable" id="Table2" style="border-spacing: 4px" cellspacing="0">
					<colgroup>
						<col style="WIDTH: 20%" />
						<col style="WIDTH: 70%" />
					</colgroup>
					<tr>
						<th>
							Classes
						</th>
						<th>
							Description and Members of Note
						</th>
					</tr>
					<tr>
						<td style="height: 21px"><code>[DBParm](amfProgramDBParmClass.html)</code>

						</td>
						<td style="height: 21px">Used for [
						constructing](amfProgramDBParmClassConstructors.html)
 SQL parameters where the attributes of 
						the parameter can be determined by its DbType.
						</td>
					</tr>
					<tr>
						<td style="height: 40px"><code>[DBStrParm](amfProgramDBStrParmClass.html)</code></td>
						<td style="height: 40px">Used for [constructing](amfProgramDBStrParmClassConstructors.html)
 SQL parameters where the parameter is 
						<code>DbType.String</code> requiring the length (<code>%Len</code>) to be 
						specified.
						</td>
					</tr>
					<tr>
						<td><code>[
						DBScaledParm](amfProgramDBScaledParmClass.html)</code></td>
						<td>Used for [
						constructing](amfProgramDBScaledParmClassConstructors.html) SQL parameters where the parameter is DbType.Decimal 
						requiring the length (<code>%Len</code>) and decimal positions 
						(<code>%DecPos</code>) to be specified.
						</td>
					</tr>
					<tr>
						<td><code>[Program](amfProgramClass.html)</code></td>
						<td><code>[ExecuteSQL_Query](amfProgramClassExecuteSQL_QueryMethods.html), [ExecuteSQL_Statement](amfProgramClassExecuteSQL_StatementMethods.html), [ExecuteSQL_QueryVerbatim](amfProgramClassExecuteSQL_QueryVerbatimMethods.html), and [ExecuteSQL_StatementVerbatim](amfProgramClassExecuteSQL_StatementVerbatimMethods.html)</code>
 for the 
						execution of SQL commands and <code>[SqlQueryResults](amfProgramClassSqlQueryResultsField.html)</code>
						to contain the results.
						</td>
					</tr>
					<tr>
						<td><code>[
						SQL_CommunicationsArea](amfProgramSQL_CommunicationsAreaClass.html)</code></td>
						<td>Represents the global SQLCA to trap and report 
						run-time errors for a SQL statement. Main properties of 
						note are <code>[SQLCOD](amfProgramSQL_CommunicationsAreaClassSQLCODField.html)</code>
 and <code>[SQLSTT](amfProgramSQL_CommunicationsAreaClassSQLSTTField.html)</code>

							used to test the status of the last executed SQL 
						statement.
						</td>
					</tr>
					<tr>
						<td><code>[SqlCursor 
						Class](amfProgramSQLCursorClass.html)</code></td>
						<td>Represents a SQL cursor for a multi-row dataset on 
						which the cursor methods operate. It has its own [SQLCA](amfProgramSqlCursorClassSQLCAField.html) and <code>[SqlQueryResults](amfProgramSqlCursorClassSqlQueryResultsField.html)</code> properties as well as the <code>[SqlQueryResultsByIndex](amfProgramSqlCursorClassSqlQueryResultsByIndexMethod.html)</code>
							method for result set index access.
						</td>
					</tr>
					<tr>
						<td><code>[
						SqlPreparedStatement Class](amfProgramSQLPreparedStatementClass.html)</code></td>
						<td>Represents a prepared executable version of a SQL 
						command statement having its own [
						SQLCA](amfProgramSqlPreparedStatementClassSQLCAField.html).</td>
					</tr>
</table>

#### Next: [Multimember File Support](amfconMultiMemberSupport.html)

#### Previous: [Message Files](amfMessageFiles.html)

#### See Also
<dl><dd>[What&#39;s New](amfWhatsNewin72.html)</dd>
				<dd>[Reference Library](amfReferenceMain.html)</dd>
</dl>

