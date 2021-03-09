---
title: Message Constructor (String,String,String,MessageTypes)

Id: amfMessageClassMessageConstructor2
TocParent: amfMessageClassMessageConstructors
TocOrder: 20

keywords: MessageTypes enumeration, used by
keywords: enumerations [ASNA.Monarch], MessageTypes, used by

---

Constructs a new instance of a predefined message.

#### Syntax
<pre class="syntax"> **BegConstructor Message Access(*Public)
  DclSrParm *id*  Type(*String)
  DclSrParm *data*  Type (*String)
  DclSrParm *file*  Type (*String)
  DclSrParm *type*  Type ([ASNA.Monarch.MessageTypes](amfMessageTypesEnumeration.html))**       </pre>

#### Parameters
<dl>
        <dt>
 *id* 
        </dt>
        <dd>String. The name of the message identifier for the
        predefined messages.</dd>
        <dt>
 *data* 
        </dt>
        <dd>String. The values for the substitution variables in
        the message or the name of the field containing the data.
        The format of each variable must be defined in the message
        description.   If the substitution variable
        can be a variable length, the length of
        the variable must be included in this string,
        i.e. "{23}Invalid employee number". </dd>
        <dt>
 *file* 
        </dt>
        <dd>String. The name of the message file containing the
        message.</dd>
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
