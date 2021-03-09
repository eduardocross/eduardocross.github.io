---
title: Message.Data Field

Id: amfMessageClassDataField
TocParent: amfMessageClassFields
TocOrder: 40

keywords: Data field
keywords: Message.Data field
keywords: substition message variables
keywords: messages, substition variable length
keywords: messages, substition variables
keywords: message files, substition variables
keywords: how to, access substition variable for messages
keywords: how to, use substition variable specifying length

---

The readonly substitution variables or name of the field containing the substitution variables for the message.

#### Syntax
<pre class="prettyprint"> **BegProp ReadOnly Data Access(*Public) Type(*String)** </pre>

#### Field Value
String. The substitution variables or name of the field containing the substitution variables for the message. If the substitution variable can be a variable length, the length of the variable will be included in this string, i.e. "{23}Invalid employee number". 
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
[Message Class](amfMessageClass.html) <br /> [Message Class Members](amfMessageClassMembers.html) <br /> [ASNA.Monarch ](amfMonarchNamespace.html)
