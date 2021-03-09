---
title: Program.RemoveMessage Method (string, string)

Id: amfProgramClassRemoveMessageMethod2
TocParent: amfProgramClassRemoveMessageMethods
TocOrder: 20

keywords: MessageQueueNotFoundException
keywords: UnsupportedOperationException

---

Removes messages from the program queue.

#### Syntax
<pre class="prettyprint"> **BegSr RemoveMessage Access(*Protected) Type(Void)
   DclSrParm *pgmQ*  Type(*String)
   DclSrParm *messageKey*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *pgmQ* 
        </dt>
        <dd>String. The name or location of the program queue from
        which the message is to be removed.</dd>
        <dt>
 *messageKey* 
        </dt>
        <dd>String. The unique message identification key of the
        message to remove, or a keyword identifying a class of one
        or more messages to remove (see Remarks below).</dd>
</dl>

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
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
 *pgmQ*  reference was not "*PRV" or
            "*SAME" (see Remarks).</td>
          </tr>
          <tr>
            <td>            UnsupportedOperationException</td>
            <td>Currently, the Monarch
            Framework only supports the keyword "*ALL"
            for the value of 
 *messageKey* .</td>
          </tr>
</table>

#### Remarks
**RemoveMessage** may be used to remove one or more messages placed on a program message queue by a call to [ SendProgramMessage](amfProgramClassSendProgramMessageMethods.html). Messages are removed from the program message queue identified by *pgmQ* . The particular messages to remove from the queue are identified by *messageKey* . 

*pgmQ* may either be specified as a program name, for direct access to a particular program queue, or as a location string, for indirect or relative access to a program queue associated with a particular invocation on the call stack. For indirect access, the value of *pgmQ* must be a string consisting of two string tokens, separated by one or more space characters. The second token indicates a program invocation, and must be either the name of a particular invocation, or the keyword "*", to indicate the caller's program invocation. The first token must be one of two values, "*SAME" or "*PRV", to indicate, respectively, the program queue of the current invocation, or the program queue of the invocation just prior to the named invocation on the call stack.

*messageKey* may be a value returned by a preceding call to **SendProgramMessage** . In this case, the message in the **SendProgramMessage** call is removed. Alternately, the value of *messageKey* may be the keyword "*ALL", indicating that all messages on the program message queue should be removed.
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

#### See Also
[Program Class](amfProgramClass.html) <br /> [Program Class Members](amfProgramClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
