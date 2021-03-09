---
title: Program.ExecuteSQL_StatementVerbatim Method (string,DBParm[])

Id: amfProgramClassExecuteSQL_StatementVerbatimMethod1
TocParent: amfProgramClassExecuteSQL_StatementVerbatimMethods
TocOrder: 20

---

Executes a SQL command statement specifying the SQL statement (exactly as stated in the RPG code) and statement parameters.
<!-- start -->

#### Syntax
<pre class="prettyprint"> **BegFunc ExecuteSQL_StatementVerbatim Access(*Public) Type(void)
   DclSrParm *sqlText*  Type(*String)
   DclSrParm *parameters*  Type (DBParm) Rank(1)** </pre>

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
        DBParm](amfProgramDBParmClass.html). An array containing the command
        parameters.</dd>
</dl>

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
