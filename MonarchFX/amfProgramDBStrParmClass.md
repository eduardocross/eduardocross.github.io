---
title: Program.DBStrParm Class

Id: amfProgramDBStrParmClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 170

keywords: Program.DBStrParm class, about Program.DBStrParm class
keywords: Program.DBStrParm class
keywords: classes [ASNA.Monarch], Program.DBStrParm class
keywords: SQL parameters
keywords: SQL parameters, string

---

The **Program.DBStrParm** is a derived class that inherits **Program.DBParm** . It further defines an object representing a string parameter to a SQL statement where the length is specified.

For a list of all members of this type, see [ Program.DBStrParm Class Members](amfProgramDBStrParmClassMembers.html).

#### Inheritance Hierarchy
<pre>[ASNA.Monarch](amfMonarchNamespace.html)       
    [ASNA.Monarch.Program](amfProgramClass.html)
        [ASNA.Monarch.Program.DBParm](amfProgramDBParmClass.html)
 **ASNA.Monarch.Program.DBStrParm**  </pre>

#### Syntax
<pre class="syntax"> **BegClass Program.DBStrParm Access(public) Inherits (Program.DBParm)**       </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
See the [ DBParm](amfProgramDBParmClass.html) class for parameters where the length can be determined by its type and [ DBScaledParm](amfProgramDBScaledParmClass.html) for decimal parameters.
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
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [ Program.DBStrParm Class Members](amfProgramDBStrParmClassMembers.html) <br /> [Program Class](amfProgramClass.html) <br /> [ Program.SqlQueryResults Field](amfProgramClassSqlQueryResultsField.html) <br /> [ Program.DBParm Class](amfProgramDBParmClass.html) <br /> [ Embedded SQL Overview](amfconSQLStatementExamples.html) 
