---
title: Program.DBParm Constructor (DbType,ParameterDirection, Object)

Id: amfProgramDBParmClassConstructor2
TocParent: amfProgramDBParmClassConstructors
TocOrder: 30

---

Constructs a new instance of a DBParm object with the data type, direction, and value indicated.

#### Syntax
<pre class="syntax"> **BegConstructor DBParm
   DclSrParm *Type*  Type(DbType)
   DclSrParm *Direction*  Type(ParameterDirection)
   DclSrParm *Value*  Type(*object)**       </pre>

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
 *Direction* 
        </dt>
        <dd>
          <a href="http://msdn2.microsoft.com/en-us/library/system.data.parameterdirection.aspx">
        System.Data.ParameterDirection</a>.  Enumeration value
        defining the type of parameter relative to the dataset.
        Values can indicate the parameter as input, output,
        inputoutput, or returnvalue.</dd>
        <dt>
 *Value* 
        </dt>
        <dd>Object instance representing the value of the
        parameters.</dd>
</dl>

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
[ Program.DBParm Class](amfProgramDBParmClass.html) <br /> [ Program.DBParm Class Members](amfProgramDBParmClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
