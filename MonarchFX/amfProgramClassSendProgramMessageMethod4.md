---
title: Program.SendProgramMessage Method (string,string,string,string)

Id: amfProgramClassSendProgramMessageMethod4
TocParent: amfProgramClassSendProgramMessageMethods
TocOrder: 40

keywords: MessageQueueNotFoundException

---

Appends an informational message to the specified program message queue.

#### Syntax
<pre class="syntax"> **BegFunc SendProgramMessage Access(*Protected) Type(*String)
   DclSrParm *id*  Type(*String)
   DclSrParm *file*  Type(*String)
   DclSrParm *data*  Type(*String)
   DclSrParm *pgmQ*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *id* 
        </dt>
        <dd>String. The name of the message identifier for
        predefined messages, or an immediate message.</dd>
        <dt>
 *file* 
        </dt>
        <dd>String. The name of the message file containing the
        message description for predefined messages.</dd>
        <dt>
 *data* 
        </dt>
        <dd>String. For predefined messages this contains values
        for the substitution variables in the message. The format
        of each variable must be defined in the message
        description. If the substitution variable can be a
        variable length, the length of the variable must
        be included in this string, i.e. "{23}Invalid employee
        number".</dd>
        <dd />
        <dd>If an immediate message is being sent, there are no 
 *data*  fields.</dd>
        <dt>
 *pgmQ* 
        </dt>
        <dd>String. The name of the program queue to send the
        message to.</dd>
</dl>

#### Return Value
String. A unique value used to identify the message sent to the queue.

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="20%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Value</th>
            <th>Condition</th>
          </tr>
          <tr>
            <td>            MessageQueueNotFoundException</td>
            <td>The message queue was not
            found in the invocation stack, or the value of the
            first token in an indirect 
 *pgmQ*  reference was no "*PRV" or "*SAME" (see
            Remarks).</td>
          </tr>
</table>

#### Remarks
This version of **SendProgramMessage** creates a message of type MessageTypes.Informational. The message is appended to the program message queue specified by *pgmQ* . This version permits the conventional use of message file-formatted texts, via the *id* , *file* , and *data* parameters.

The *id* parameter may be used to identify a predefined message contained in a message file named by the *file* parameter. In this case, the message object added to the queue would be suitable for use with the [ MessageFormatter.FormatMessage](amfMessageFormatterClassFormatMessageMethod.html) method. Also, the *data* parameter may be used to provide values required by any substitution variables defined in the predefined message. Note that this describes the conventional use of *id* , *file* , and *data* , as supported by some Monarch Framework utility functions such as **FormatMessage** . Customized usage of these parameters is allowed, to say, create an "immediate" message that does not require predefined message files.

*pgmQ* may either be specified as a program name, for direct access to a particular program queue, or as a location string, for indirect or relative access to a program queue associated with a particular invocation on the call stack. For indirect access, the value of *pgmQ* must be a string consisting of two string tokens, separated by one or more space characters. The second token indicates a program invocation, and must be either the name of a particular invocation, or the keyword "*", to indicate the caller's program invocation. The first token must be one of two values, "*SAME" or "*PRV", to indicate, respectively, the program queue of the current invocation, or the program queue of the invocation just prior to the named invocation on the call stack.

Note that using this version of SendProgramMessage is precisely the same as calling the five-parameter overload as follows:

SendProgramMessage( *id* , *file* , *data* , *pgmQ* , MessageTypes.Informational)

The method returns a message key which may be used to identify the message on the queue - for example, with **RemoveMessage** .
<!-- -->

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
[Program Class](amfProgramClass.html) <br /> [Program Class Members](amfProgramClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
