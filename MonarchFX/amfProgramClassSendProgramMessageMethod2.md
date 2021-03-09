---
title: Program.SendProgramMessage Method (string, string, MessageTypes)

Id: amfProgramClassSendProgramMessageMethod2
TocParent: amfProgramClassSendProgramMessageMethods
TocOrder: 20

keywords: MessageQueueNotFoundException
keywords: MessageTypes enumeration, used by
keywords: enumerations [ASNA.Monarch], MessageTypes, used by

---

Appends an immediate message to a specified program message queue.

#### Syntax
<pre class="syntax"> **BegFunc SendProgramMessage Access(*Protected) Type(*String)
   DclSrParm *text*  Type(*String)
   DclSrParm *pgmQ*  Type(*String)
   DclSrParm *type*  Type([ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html))** </pre>

#### Parameters
<dl>
        <dt>
 *text* 
        </dt>
        <dd>String. Specifies the immediate message text.</dd>
        <dt>
 *pgmQ* 
        </dt>
        <dd>String. The name or location of the program queue to
        send the message to.</dd>
        <dt>
 *type* 
        </dt>
        <dd>
 **ASNA.Monarch.MessageTypes** . Specifies the
        type of message being sent. i.e. Completion, Diagnostic,
        Escape, Informational, Inquiry, Notify, Request, or
        Status.</dd>
</dl>

#### Return Value
String. A unique value used to identify the message sent to the queue.

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />

          </colgroup>
          <tr>
            <th>Value</th>
            <th>Condition</th>
          </tr>
          <tr>
            <td> **MessageQueueNotFoundException** </td>
            <td>The message queue was not
            found in the invocation stack, or the value of the
            first token in an indirect 
 *pgmQ*  reference was not "*PRV" or "*SAME" (see
            Remarks).</td>
          </tr>
</table>

#### Remarks
Use this method to create a message containing user-formatted text and append it to a program message queue associated with a particular invocation on the program call stack. No message file is referenced or required when using this method.

*pgmQ* may either be specified as a program name, for direct access to a particular program queue, or as a location string, for indirect or relative access to a program queue associated with a particular invocation on the call stack. For indirect access, the value of *pgmQ* must be a string consisting of two string tokens, separated by one or more space characters. The second token indicates a program invocation, and must be either the name of a particular invocation, or the keyword "*", to indicate the caller's program invocation. The first token must be one of two values, "*SAME" or "*PRV", to indicate, respectively, the program queue of the current invocation, or the program queue of the invocation just prior to the named invocation on the call stack.

*type* categorizes the message as Diagnostic, Escape, Informational, Inquiry, Notify, Request, or Status. See [ ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html) for a summary of each category.

The method returns a message key which may be used to identify the message on the queue - for example, with RemoveMessage.
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
<dl>
        <dd>[Program
        Class](amfProgramClass.html)</dd>
        <dd>
        [Program
        Class Members](amfProgramClassMembers.html)</dd>
<dd>[
        ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html)</dd>
<dd>[ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
</dl>

