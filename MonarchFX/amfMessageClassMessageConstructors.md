---
title: Message Constructors

Id: amfMessageClassMessageConstructors
TocParent: amfMessageClass
TocOrder: 10

keywords: Message.Message constructors
keywords: Message class, constructors
keywords: constructors [ASNA.Monarch], Message class
keywords: message files, constructing immediate messages
keywords: messages, constructing immediate messages
keywords: messages, constructing predefined messages
keywords: messages files, constructing predefined messages
keywords: how to, construct immediate messages
keywords: how to, construct predefined messages
keywords: how to, use message files for predefined messages
keywords: how to, use message files for immediate messages
keywords: immediate messages
keywords: predefined messages
keywords: messages, immediate
keywords: messages, predefined

---

The overloaded method constructs a new instance of a **Message** object for an immediate or predefined message.

#### Overloaded List
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th>Description</th>
          </tr>
          <tr>
            <td>[Message ( *string, MessageTypes* )](amfMessageClassMessageConstructor1.html)
            </td>
            <td>Constructs a new instance of
          an immediate message supplying text and message
          type.</td>
          </tr>
          <tr>
            <td>[Message ( *string, string, string, MessageTypes* )](amfMessageClassMessageConstructor2.html)
            </td>
            <td>Constructs a new instance of
          a predefined message supplying the message id,
          substitution variable, file name, and message type.</td>
          </tr>
</table>

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
[Message Class](amfMessageClass.html)<br />[Message Class Members](amfMessageClassMembers.html)<br />[ ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html)<br />[ASNA.Monarch Namespace](amfMonarchNamespace.html)
