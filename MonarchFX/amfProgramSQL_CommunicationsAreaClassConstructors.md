---
title: Program.SQL_CommunicationsArea Constructors

Id: amfProgramSQL_CommunicationsAreaClassConstructors
TocParent: amfProgramSQL_CommunicationsAreaClass
TocOrder: 10

keywords: Program.SQL_CommunicationsArea.Program.SQL_CommunicationsArea constructors
keywords: Program.SQL_CommunicationsArea class, constructors
keywords: constructors [ASNA.Monarch], Program.SQL_CommunicationsArea class
keywords: SQL, communications area, new
keywords: SQL communications area, new
keywords: SQLCA, new
keywords: how to, construct new SQLCA

---

This overloaded method constructs a new instance of a **SQL_CommunicationsArea** object.

#### Overloaded List
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th>Description</th>
          </tr>          <tr>
            <td>[
            SQL_CommunicationsArea (string)](amfProgramSQL_CommunicationsAreaClassConstructor1.html)
            </td>
            <td>Creates a new instance of a
          SQL_CommunicationsArea object with command text.</td>
          </tr>
          <tr>
            <td>[
            SQL_CommunicationsArea (string,
 *int, int* )](amfProgramSQL_CommunicationsAreaClassConstructor2.html)
            </td>
            <td>Creates a new instance of a
          SQL_CommunicationsArea object with command text, execution status code, and state.</td>
          </tr>
          <tr>
            <td>[
            SQL_CommunicationsArea (string,
 *int, int, System.Exception* )](amfProgramSQL_CommunicationsAreaClassConstructor3.html)
            </td>
            <td>Creates a new instance of a
          SQL_CommunicationsArea object with command
          text, execution status code, state, and systems
          exception.</td>
          </tr>
          <tr>
            <td>[
            SQL_CommunicationsArea (string,
            SqlClient.SqlExcption)](amfProgramSQL_CommunicationsAreaClassConstructor4.html)
            </td>
            <td>Creates a new instance of a
          SQL_CommunicationsArea object with command text
          and SQL client data exception.</td>
          </tr>
</table>

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
<dl>
    <dd>[
    Program.SQL_CommunicationsArea Class](amfProgramSQL_CommunicationsAreaClass.html)</dd>
    <dd>[
    Program.SQL_CommunicationsArea Class Members](amfProgramSQL_CommunicationsAreaClassMembers.html)</dd>
    <dd>[ASNA.Monarch
    Namespace](amfMonarchNamespace.html)</dd>
    <dd><a href="http://msdn2.microsoft.com/en-us/library/System.Data.DbType.aspx">
    System.Data.DbType</a></dd>
    <dd><a href="http://msdn2.microsoft.com/en-us/library/system.data.parameterdirection.aspx">
    System.Data.ParameterDirection</a></dd>
</dl>

