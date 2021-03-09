---
title: Program.DBStrParm Constructor (DbType,Object,int)

Id: amfProgramDBStrParmClassConstructor3
TocParent: amfProgramDBStrParmClassConstructors
TocOrder: 20

---

Constructs a new instance of a **DBStrParm** object with the data type, value, and length indicated.

#### Syntax
<pre class="syntax"> **BegConstructor DBStrParm
   DclSrParm *Type*  Type(DbType)
   DclSrParm *Value*  Type(*object)
   DclSrParm *Size*  Type(*integer)**       </pre>

#### Parameters
<dl>
        <dt>
 *Type* 
        </dt>
        <dd>
          [ASNA.Monarch](http://msdn2.microsoft.com/en-us/library/System.Data.DbType.aspx">
        System.Data.DbType</a>. Enumeration value defining the data
        type of the parameter.</dd>
        <dt>
 *Value* 
        </dt>
        <dd>Object instance representing the value of the
        parameters.</dd>
        <dt>
 *Size* 
        </dt>
        <dd>Integer. The length of the parameter.</dd>
</dl>

#### Examples
The following shows an example of a DELETE statement with one parameter. If the legacy source contains:
<pre class="libCScode">
0296.00     C/EXEC SQL
0297.00     C+ DELETE FROM DEPARTMENT WHERE :DEPTNO# = 'D11'
0298.00     C/END-EXEC
</pre>

Migrated codes appears as:
<pre class="example">
ExecuteSQL_Statement ( +
"DELETE FROM DEPARTMENT WHERE @sql_parm_1 = 'D11';", +
 *New **DBStrParm**  (DbType.String, DEPTNO#, %Len (DEPTNO#)) +
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
[ Program.DBStrParm Class](amfProgramDBStrParmClass.html) <br /> [ Program.DBStrParm Class Members](amfProgramDBStrParmClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
