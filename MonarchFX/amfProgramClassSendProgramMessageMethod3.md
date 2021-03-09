---
title: Program.SendProgramMessage Method (string,string,string)

Id: amfProgramClassSendProgramMessageMethod3
TocParent: amfProgramClassSendProgramMessageMethods
TocOrder: 30

keywords: MessageQueueNotFoundException

---

Appends an informational message to the program message queue associated with the caller's caller.

#### Syntax
<pre class="syntax"> **BegFunc SendProgramMessage Access(*Protected) Type(*String)
   DclSrParm *id*  Type(*String)
   DclSrParm *file*  Type(*String)
   DclSrParm *data*  Type(*String)** </pre>

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
        for the substitution variables in the message.  The
        format of each variable must be defined in the message
        description.  If the substitution variable can be
        a variable length, the length of the variable
        must be included in this string, i.e. "{23}Invalid
        employee number". </dd>
        <dd />
        <dd>If an immediate message is being sent, there are no 
 *data*  fields.</dd>
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
            <td>            MessageQueueNotFoundException</td>
            <td>The "*PRV" message queue
            was not found in the invocation stack.</td>
          </tr>
</table>

#### Remarks
This version of **SendProgramMessage** creates a message of type MessageTypes.Informational. The message is appended to the program message queue associated with the invocation prior to the caller's. This version permits the conventional use of message file-formatted texts.

The *id* parameter may be used to identify a predefined message contained in a message file named by the *file* parameter. In this case, the message object added to the queue would be suitable for use with the [ MessageFormatter.FormatMessage](amfMessageFormatterClassFormatMessageMethod.html) method. Also, the *data* parameter may be used to provide values required by any substitution variables defined in the predefined message. Note that this describes the conventional use of *id* , *file* , and *data* , as supported by some Monarch Framework utility functions such as **FormatMessage** . Customized usage of these parameters is allowed, to say, create an "immediate" message that does not require predefined message files.

Note that using this version of **SendProgramMessage** is precisely the same as calling the five-parameter overload as follows:

SendProgramMessage( *id* , *file* , *data* , "*PRV *", MessageTypes.Informational)

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
