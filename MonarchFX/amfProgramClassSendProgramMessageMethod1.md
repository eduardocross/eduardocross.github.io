---
title: Program.SendProgramMessage Method (string)

Id: amfProgramClassSendProgramMessageMethod1
TocParent: amfProgramClassSendProgramMessageMethods
TocOrder: 10

keywords: MessageQueueNotFoundException

---

Appends an immediate message to the program message queue associated with the caller's caller.

#### Syntax
<pre class="syntax"> **BegFunc SendProgramMessage Access(*Protected) Type(*String)
   DclSrParm *text*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *text* 
        </dt>
        <dd>String. Specifies the immediate message text.</dd>
</dl>

#### Return Value
String. A unique value used to identify the message sent to the queue.

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
       <colgroup>
            <col style="FONT-WEIGHT: bold;WIDTH: 40%" />
            <col style="WIDTH: 50%" />
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
This version of **SendProgramMessage** creates a message of type MessageTypes.Informational and containing user-formatted text. The message is appended to the program message queue associated with the invocation prior to the caller's. No message file is referenced or required when using this method.

Note that using this version of **SendProgramMessage** is precisely the same as calling one of the three-parameter overloads as follows:

SendProgramMessage( *text* , "*PRV *", MessageTypes.Informational)

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
