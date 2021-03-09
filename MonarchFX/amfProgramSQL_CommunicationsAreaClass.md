---
title: Program.SQL_CommunicationsArea Class

Id: amfProgramSQL_CommunicationsAreaClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 190

keywords: Program.SQL_CommunicationsArea class, about Program.SQL_CommunicationsArea class
keywords: Program.SQL_CommunicationsArea class
keywords: classes [ASNA.Monarch], Program.SQL_CommunicationsArea class
keywords: SQL_CommunicationsArea class
keywords: SQL, communications area
keywords: SQLCA

---

The **Program.SQL_CommunicationsArea** (nested) class defines an object that represents the SQLCA to trap and report run-time errors for a SQL statement.

For a list of all members of this type, see [ Program.SQL_CommunicationsArea Class Members](amfProgramSQL_CommunicationsAreaClassMembers.html).
<!--mine -->

#### Inheritance Hierarchy
<pre style="height: 47px">[ASNA.Monarch](amfMonarchNamespace.html)
    [ASNA.Monarch.Program](amfProgramClass.html)
 **ASNA.Monarch.Program.SQL_CommunicationsArea** </pre>

#### Syntax
<pre class="syntax">
 **BegClass Program.SQL_CommunicationsArea Access(public) Inherits ASNA.Monarch.Program** 
      </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
The instance of this object will have a value of *nothing before executing any SQL command. After execution of any SQL command, this object can be accessed to determine the success or failure of the SQL statement. The most common use is to test [ SQLCOD](amfProgramSQL_CommunicationsAreaClassSQLCODField.html) to find if the operation was successful or not. [ SQLSTT](amfProgramSQL_CommunicationsAreaClassSQLSTTField.html) contains an additional return code for more detail; while [ SQL_Exception](amfProgramSQL_CommunicationsAreaClassSQL_ExceptionField.html) contains a reference to an instance of a [ SqlCommandText](http://msdn2.microsoft.com/en-us/library/system.exception_members(VS.71).aspx"> System.Exception</a> with complete detail information on an exception. As part of the debugging process, <a href="amfProgramSQL_CommunicationsAreaClassSqlCommandTextField.html) is provided to contain the actual command statement.

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
        <dd>[ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
        <dd>[
        Program.SQL_CommunicationsArea Class Members](amfProgramSQL_CommunicationsAreaClassMembers.html)</dd>
        <dd>[Program
        Class](amfProgramClass.html)</dd>
        <dd>[
        Embedded SQL Overview](amfconSQLStatementExamples.html)</dd></dl>

