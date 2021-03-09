---
title: Program.SendExternalMessage Method (string, string, string, ASNA.Monarch.MessageTypes)

Id: amfProgramClassSendExternalMessageMethod
TocParent: amfProgramClassMethods
TocOrder: 80

keywords: SendExternalMessage method
keywords: Program.SendExternalMessage method
keywords: MessageTypes enumeration, used by
keywords: enumerations [ASNA.Monarch], MessageTypes, used by
keywords: message queues, sending external program messages
keywords: external messages, sending to program
keywords: messages, sending external program
keywords: predefined external messages, sending to program
keywords: immediate external messages, sending to program
keywords: sending external program messages
keywords: sending immediate external program messages
keywords: sending predefined external program messages
keywords: program messages, sending external predefined
keywords: program messages, sending external immediate
keywords: how to, send external program messages
keywords: how to, send predefined external program messages
keywords: how to, send immediate external program messages

---

Append a message to the external message queue.

#### Syntax
<pre class="syntax"> **BegFunc SendExternalMessage Access(*Protected) Type(*String)
   DclSrParm *id*  Type(*String)
   DclSrParm *file*  Type(*String)
   DclSrParm *data*  Type(*String)
   DclSrParm *type*  Type([ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html))** </pre>

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
        number". </dd>

        <dd>If an immediate message is being sent, there are no 
 *data*  fields.</dd>
        <dt>
 *type* 
        </dt>
        <dd>
 **ASNA.Monarch.MessageTypes** . Specifies the
        type of message being sent: Completion, Diagnostic, Escape,
        Informational, Inquiry, Notify, Request, or Status.</dd>
</dl>

#### Return Value
String. A unique value used to identify the message sent to the queue.

#### Remarks
**SendExternalMessage** adds the specified message to the "external" or "job" message queue. The external message queue is associated with the current process. This is in contrast to [ SendProgramMessage](amfProgramClassSendProgramMessageMethods.html), which adds messages to a queue associated with a particular invocation on the program call stack.

The *id* parameter may be used to identify a predefined message contained in a message file named by the *file* parameter. In this case, the message object added to the queue would be suitable for use with the [ MessageFormatter.FormatMessage](amfMessageFormatterClassFormatMessageMethod.html) method. Also, the *data* parameter may be used to provide values required by any substitution variables defined in the predefined message.

Note that this describes the conventional use of *id* , *file* , and *data* , as supported by some Monarch Framework utility functions such as **FormatMessage** . Customized usage of these parameters is allowed, to say, create an "immediate" message that does not require predefined message files.
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
[Program Class](amfProgramClass.html) <br /> [Program Class Members](amfProgramClassMembers.html) <br /> [ ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
