---
title: Program.ExecuteSQL_Query Method (string, DBParm)

Id: amfProgramClassExecuteSQL_QueryMethod1
TocParent: amfProgramClassExecuteSQL_QueryMethods
TocOrder: 20

---

Executes a SQL query specifying the SQL statement and statement parameters.
<!-- start -->

#### Syntax
<pre class="syntax"> **BegFunc ExecuteSQL_Query Access(*Public) Type(System.Collections.Generic.Dictionary)
   DclSrParm *sqlText*  Type(*String)
   DclSrParm *parameters*  Type (DBParm) Rank(1)**       </pre>

#### Parameters
<dl>
        <dt>
 *sqlText* 
        </dt>
        <dd>String. The SQL query statement
        with a substitution variable defined for each
        parameter.</dd>
        <dt>
 *parameters*  </dt>
        <dd>
          [
        DBParm](amfProgramDBParmClass.html). An array containing the query parameters.</dd>
</dl>

#### Returns
**System.Collections.Generic.Dictionary** (string and object) representing the query results allowing values for a particular column to be accessed by name.
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
[Program Class](amfProgramClass.html) <br /> [Program Class Members](amfProgramClassMembers.html) <br /> [ SqlQueryResults Field](amfProgramClassSqlQueryResultsField.html) <br /> [ Program.DBParm Class](amfProgramDBParmClass.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
