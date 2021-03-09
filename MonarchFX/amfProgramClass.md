---
title: Program Class

Id: amfProgramClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 15

keywords: Program class, about Program class
keywords: Program class
keywords: classes [ASNA.Monarch], Program class
keywords: program data areas
keywords: message queues
keywords: program control

---

The **Program** class provides activation/invocation semantics. It conforms to certain conventions allowing it to be the Target of a Call operation.

This class provides support in the areas of:

- Message Queues
- Program Control
- Embedded SQL support

For a list of all members of this type, see [Program Class Members](amfProgramClassMembers.html).
<!-- start -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch](amfMonarchNamespace.html)
 **ASNA.Monarch.Program** </pre>

<!-- start -->

#### Syntax
<pre class="syntax"> **BegClass Program Access(public) Inherits (System.Object)**      </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
**Message Queues** 

- A message is a communication sent from one user,
        program, or procedure to another. There are two types of
        messages. Immediate and Predefined. Immediate messages are
        created by the program or system user when they are sent
        and are not permanently stored in the system. Predefined
        messages are created before they are used. These messages
        are placed in a 
 **message file**  when they are created, and
        retrieved from that file when they are used. Messages are
        sent to and received from 
 **message queues** , which are separate objects
        on the system. When a message is sent to a procedure, a
        program, or a system user, it is placed on a message queue
        associated with that procedure, program, or user. The 
        [
        SendExternalMessage](amfProgramClassSendExternalMessageMethod.html) method sends an immediate or
        predefined external program message and returns a response
        depending on the 
        [
        type](amfMessageTypesEnumeration.html) of message sent. The response may be entered by the
        user, the default message (if any), or *N. The overloaded 
        [
        SendProgramMessage](amfProgramClassSendProgramMessageMethods.html) method sends an immediate or
        predefined program message. The different overloaded
        methods allow messages to be sent to specific message files
        and program queues and to return a response depending on
        the ** *type* **  of message sent. The overloaded 
        [
        RemoveMessage](amfProgramClassRemoveMessageMethods.html) method removes a message by message key or
        message key and program queue.

**Program Control** 

- The 
        [
        ExecCommand](amfProgramClassExecCommandMethod.html) method executes the program command specified. The 
        [
        MonarchJob](amfProgramClassMonarchJobProperty.html) read-only property contains the name of the 
 **ASNA.Monarch.Job**  under which the 
 **Program**  is running. The 
        [Dispose](amfProgramClassDisposeMethod.html) returns 
 **true**  if the program is in the process of
        being disposed of.

**Embedded SQL Support** 

- For SQL, the Program Class provides 
        [
        ExecuteSQL_Query](amfProgramClassExecuteSQL_QueryMethods.html) and 
        [
        ExecuteSQL_Statement](amfProgramClassExecuteSQL_StatementMethods.html) methods for the execution of
        query and non-query SQL statements respectively.  (For
        debugging 
        [
        ExecuteSQL_QueryVerbatim](amfProgramClassExecuteSQL_QueryVerbatimMethods.html) and 
        [
        ExecuteSQL_StatementVerbatim](amfProgramClassExecuteSQL_StatementVerbatimMethods.html) methods are also
        provided.)  Results data sets are contained in the
        protected
        [
        SqlQueryResults](amfProgramClassSqlQueryResultsField.html) field.  Nested classes for
        SQL include: 
        [
        DBParm](amfProgramDBParmClass.html), 
        [
        DBScaledParm,](amfProgramDBScaledParmClass.html) and 
        [
        DBStrParm](amfProgramDBStrParmClass.html) for defining parameters, 
        [
        SQL_CommunicationsArea](amfProgramSQL_CommunicationsAreaClass.html) for the global SQLCA, 
        [
        SqlCursor](amfProgramSqlCursorClass.html) for multi-row dataset on which the
        cursor methods operate, and 
        [
        SqlPreparedStatement](amfProgramSqlPreparedStatementClass.html) for the prepared version of a
        SQL command.

<!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width= "15%" style="font-weight:bold" />
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
    <dd>[Monarch Job and Program Classes Concepts](amfconMonarchJobandProgramClasses.html)</dd>
          <dd>[ASNA.Monarch Namespace](amfMonarchNamespace.html)</dd>
          <dd>[Program Class Members](amfProgramClassMembers.html)</dd>
          <dd>[ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html)</dd>
          <dd>[Embedded SQL Overview](amfconSQLStatementExamples.html)</dd>
</dl>

