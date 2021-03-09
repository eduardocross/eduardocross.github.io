---
title: Message Constructor (String, MessageTypes)

Id: amfMessageClassMessageConstructor1
TocParent: amfMessageClassMessageConstructors
TocOrder: 10

keywords: MessageTypes enumeration, used by
keywords: enumerations [ASNA.Monarch], MessageTypes, used by

---

Constructs an instance of an immediate message.

#### Syntax
<pre class="syntax"> **BegConstructor Message Access(*Public)
  DclSrParm *text*  Type(*String)
  DclSrParm *type*  Type ([ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html))**       </pre>

#### Parameters
<dl>
        <dt>
 *text* 
        </dt>
        <dd>String. The message text.</dd>
        <dt>
 *type* 
        </dt>
        <dd>
 **ASNA.Monarch.MessageTypes** . Specifies the
        type of message being sent. i.e. Completion, Diagnostic,
        Escape, Informational, Inquiry, Notify, Request, or
        Status.</dd>
</dl>

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
[Message Class](amfMessageClass.html) <br /> [Message Class Members](amfMessageClassMembers.html) <br /> [ ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html) <br /> [ASNA.Monarch](amfMonarchNamespace.html)
