---
title: Program.ExecuteSQL_Statement Method (string,DBParm[])

Id: amfProgramClassExecuteSQL_StatementMethod1
TocParent: amfProgramClassExecuteSQL_StatementMethods
TocOrder: 20

---

Executes a SQL command statement specifying the SQL statement and statement parameters.
<!-- start -->

#### Syntax
<pre class="syntax"> **BegFunc ExecuteSQL_Statement Access(*Public) Type(void)
   DclSrParm *sqlText*  Type(*String)
   DclSrParm *parameters*  Type (DBParm) Rank(1)**       </pre>

#### Parameters
<dl>
        <dt>
 *sqlText* 
        </dt>
        <dd>String. The SQL statement
        with a substitution variable defined for each
        parameter.</dd>
        <dt>
 *parameters*  </dt>
        <dd>
          [
        DBParm](amfProgramDBParmClass.html). An array containing the statement
        parameters.</dd>
</dl>

#### Examples
The following shows an example of a DELETE statement. The legacy source contains:
<pre class="libCScode">
0296.00     C/EXEC SQL
0297.00     C+ DELETE FROM DEPARTMENT WHERE :DEPTNO# = 'D11'
0298.00     C/END-EXEC</pre>

Gets migrated as:
<pre class="example">ExecuteSQL_Statement ( +
"DELETE FROM DEPARTMENT WHERE @sql_parm_1 = 'D11';", +
<span style="color:blue">*New</span>  DBStrParm(DbType.String, DEPTNO#, <span style="color:blue">%Len</span>(DEPTNO#)) +
)</pre>

Using the same example but with a second parameter - legacy source containing:
<pre class="libCScode">
0296.00     C/EXEC SQL
0297.00     C+ DELETE FROM DEPARTMENT WHERE :DEPTNO# = 'D11'and :DEPTST# = 'INA'
0298.00     C/END-EXEC</pre>

Gets migrated as:
<pre class="example">ExecuteSQL_Statement ( +
"DELETE FROM DEPARTMENT WHERE @sql_parm_1 = 'D11' and @sql_parm2 = 'INA';", +
<span style="color:blue">*New</span>  DBStrParm(DbType.String, DEPTNO#, <span style="color:blue">%Len</span>(DEPTNO#)) +
<br /><span style="color:blue">*New</span>  DBStrParm(DbType.String, DEPTST#, <span style="color:blue">%Len</span>(DEPTST#)) + 
)
</pre>

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

#### See Also
<dl>
        <dd>[Program
        Class](amfProgramClass.html)</dd>
        <dd>
        [Program
        Class Members](amfProgramClassMembers.html)</dd>
<dd>[
        Program.DBParm Class](amfProgramDBParmClass.html)</dd>
<dd>[ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
</dl>

