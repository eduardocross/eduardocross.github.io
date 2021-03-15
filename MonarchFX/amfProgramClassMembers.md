---
title: Program Class Members

Id: amfProgramClassMembers
TocParent: amfProgramClass
TocOrder: 5

keywords: Program class, all members
keywords: members [ASNA.Monarch], Program class

---

[Program Class Overview](amfProgramClass.html) 
<!-- start public properties table -->	

#### Public Constructor
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Constructor</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->
          <tr valign="top">
            <td><img id="IMG1" style="WIDTH: 16px; HEIGHT: 16px" alt="constructor" src="Images/Constructor.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              Program](amfProgramClassProgramConstructors.html)
            </td>
            <td>Creates a new instance of
            the 
 **Program**  object.</td>
          </tr>
</table>

<!-- start public properties table -->	

#### Protected Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />DataArea_In</td>
            <td>Deprecated. Use the Visual
            RPG "IN" command.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />DataArea_Out</td>
            <td>Deprecated. Use the Visual
            RPG "OUT" command.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />DataArea_Unlock</td>
            <td>Deprecated. Use the Visual
            RPG "UNLOCK" command.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              ExecCommand](amfProgramClassExecCommandMethod.html)
            </td>
            <td>Executes the Program
            command specified in 
 *cmdText* .</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />GetLdaField</td>
            <td>Deprecated.  Use the
            Visual RPG "IN" command.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              RemoveMessage](amfProgramClassRemoveMessageMethods.html)
            </td>
            <td>Overloaded. Remove messages
            from the program message queue of the caller's
            caller or specific program message queue.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              SendExternalMessage](amfProgramClassSendExternalMessageMethod.html)
            </td>
            <td>Append a message to
            the external message queue.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              SendProgramMessage](amfProgramClassSendProgramMessageMethods.html)
            </td>
            <td>Overloaded.
            Appends different message types to the
            program message queue associated with the caller's
            caller or to the specified program message queue.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />SetLdaField</td>
            <td>Deprecated. Use the Visual
            RPG "OUT" command.</td>
          </tr>
</table>

<!-- start public properties table -->	

#### Public Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->
          <tr valign="top">
            <td><img id="Img3" style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [Dispose](amfProgramClassDisposeMethod.html)
            </td>
            <td>Releases managed and
            unmanaged or just unmanaged resources used by the
            object.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
              ExecuteSQL_Query](amfProgramClassExecuteSQL_QueryMethods.html)
            </td>
            <td>Overloaded methods to
            execute a SQL query command.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
              ExecuteSQL_QueryVerbatim](amfProgramClassExecuteSQL_QueryVerbatimMethods.html)
            </td>
            <td>Overloaded methods to
            execute a SQL query command with the string
            text exactly as contained in the original
            legacy source code</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
              ExecuteSQL_Statement](amfProgramClassExecuteSQL_StatementMethods.html)
            </td>
            <td>Overloaded methods to
            execute a SQL command statement.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
              ExecuteSQL_StatementVerbatim](amfProgramClassExecuteSQL_StatementVerbatimMethods.html)
            </td>
            <td>Overloaded methods to
            execute a SQL command statement with the string
            text exactly as contained in the original
            legacy source code.</td>
          </tr>
</table>

<br />

#### Protected Properties
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td><img id="Img2" style="WIDTH: 16px; HEIGHT: 16px" alt="protected property" src="Images/
Protectedproperty.bmp" border="0" x-maintain-ratio="TRUE" />
              [
              MonarchJob](amfProgramClassMonarchJobProperty.html)
            </td>
            <td>Gets the name of the 
            [
            ASNA.Monarch.Job](amfJobClass.html) under which the Program
            <strong />is running.</td>
          </tr>
</table>

#### Public Fields
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Field</th>
            <th>Description</th>
          </tr>
          <tr valign="top">
            <td><img id="Img6" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="Images/Field.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              SqlQueryResults](amfProgramClassSqlQueryResultsField.html)
            </td>
            <td>A field containing a
            collection representing the query results.</td>
          </tr>
</table>

#### Protected Fields
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Field</th>
            <th>Description</th>
          </tr>
          <tr>
            <td><img id="Img4" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="Images/ProtectedField.bmp" width="15" border="0" x-maintain-ratio="TRUE" /> 
            [
            SQLCA](amfProgramClassSQLCAField.html)</td>
            <td>[
            SQL_CommunicationsArea](amfProgramSQL_CommunicationsAreaClass.html) object that represents
            the SQLCA to trap and report run-time errors
            for the 
 **Program** .</td>
          </tr>
          <tr valign="top">
            <td><img id="Img5" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="Images/ProtectedField.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              StartupMoment](amfProgramClassStartupMomentField.html)
            </td>
            <td>A read-only field
            containing the System.DateTime of when the program
            started.</td>
          </tr>
</table>

#### See Also
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [Program Class](amfProgramClass.html) 
