---
title: Program.SQL_CommunicationsArea.SqlCommandText Field

Id: amfProgramSQL_CommunicationsAreaClassSqlCommandTextField
TocParent: amfProgramSQL_CommunicationsAreaClassFields
TocOrder: 30

keywords: SqlCommandText property
keywords: SQL_CommunicationsArea.SqlCommandText field
keywords: Program.SQL_CommunicationsArea.SqlCommandText field
keywords: SQL, command text
keywords: SqlCommandText
keywords: how to, determine SQL command text
keywords: SQL, SQLCA command text
keywords: SQL, communications area, command text
keywords: SQL communications area, text
keywords: SQLCA, command text

---

Read-only actual SQL command text.

#### Syntax
<pre class="syntax">
 **BegProp Readonly SqlCommandText Access(*Public)
Type(*String)** 
      </pre>

#### Field Value
**String** containing the actual SQL command text.

#### Remarks
When SQLCA is instantiated, the original SQL command is passed into this field for access by the programming - generally for debugging.

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
[ Program.SQL_CommunicationsArea Class](amfProgramSQL_CommunicationsAreaClass.html) <br /> [ Program.SQL_CommunicationsArea Class Members](amfProgramSQL_CommunicationsAreaClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
