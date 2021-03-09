---
title: Program.DBParm Class

Id: amfProgramDBParmClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 150

keywords: Program.DBParm class, about Program.DBParm class
keywords: Program.DBParm class
keywords: classes [ASNA.Monarch], Program.DBParm class
keywords: SQL parameters

---

The **Program.DBParm** (nested) class defines an object that represents a parameter to a SQL statement where the length can be determined by its type.

For a list of all members of this type, see [ Program.DBParm Class Members](amfProgramDBParmClassMembers.html).

#### Inheritance Hierarchy
<pre> [
        ASNA.Monarch](amfMonarchNamespace.html)
        [
        ASNA.Monarch.Program](amfProgramClass.html)
 **ASNA.Monarch.Program.DBParm** 
      </pre>

#### Syntax
<pre class="syntax"> **BegClass Program.DBParm Access(public) Inherits (ASNA.Monarch.Program)**       </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
DBParm is defined as a nested class of ASNA.Monarch.Program and can directly use names, type names, names of static members, and enumerators only from the enclosing class. To use names of other class members, you must use pointers, references, or object names.

See the inherited classes [ DBStrParm](amfProgramDBStrParmClass.html) for string parameters and [ DBScaledParm](amfProgramDBScaledParmClass.html) for decimal parameters.
<!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" style="width: 60%; height: 100px">
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
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [ Program.DBParm Class Members](amfProgramDBParmClassMembers.html) <br /> [Program Class](amfProgramClass.html) <br /> [ Program.SqlQueryResults Field](amfProgramClassSqlQueryResultsField.html) <br /> [ Embedded SQL Overview](amfconSQLStatementExamples.html) 
