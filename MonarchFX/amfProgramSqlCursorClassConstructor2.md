---
title: Program.SqlCursor Constructor (DbConnection,string)

Id: amfProgramSqlCursorClassConstructor2
TocParent: amfProgramSqlCursorClassConstructors
TocOrder: 20

---

Constructs a new instance of a **SqlCursor** object specifying the database connection and select statement without parameters.

#### Syntax
<pre class="syntax"> **BegConstructor SqlCursor
   DclSrParm *sqlConnection*  Type(Common.DbConnection)
   DclSrParm *SelectStatement*  Type(*String)**       </pre>

#### Parameters
<dl>
        <dt>
 *sqlConnection* 
        </dt>
        <dd>
          [ASNA.Monarch](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx">
        System.Data.Common.DbConnection</a>. The database
        connection.</dd>
        <dt>SelectStatement</dt>
        <dd>String. The text of the SELECT statement without
        parameters.</dd>
</dl>

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td><a href="amfMonarchNamespace.html)</td>
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
