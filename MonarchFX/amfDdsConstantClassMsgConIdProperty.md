---
title: DdsConstant.MsgConId Property

Id: amfDdsConstantClassMsgConIdProperty
TocParent: amfDdsConstantClassPropertiesMain
TocOrder: 20

keywords: MsgConId property
keywords: DdsConstant.MsgConId property
keywords: Web server controls [ASNA.Monarch], setting MSGCON message id
keywords: how to, set MSGCON message id
keywords: how to, get MSGCON message id
keywords: message files, setting MSGCON message ide
keywords: message files, getting MSGCON message id
keywords: web controls, setting MSGCON message id
keywords: web controls, getting MSGCON message id
keywords: field controls, MSGCON message id
keywords: MSGCON, message id

---

Gets or sets the Message-ID specifying the text to use as the value of the constant field. 

#### Syntax
<pre class="prettyprint"> **BegProp MsgConId Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the id of a message in the Message File specifying the text to use as the value of the constant field.

#### Remarks
Together with [MsgConFile](amfDdsConstantClassMsgConFileProperty.html) and [MsgConLength](amfDdsConstantClassMsgConLengthProperty.html), **MsgConId** is used to implement the MSGCON DDS keyword.

See [MsgConLength](amfDdsConstantClassMsgConLengthProperty.html) for an example.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsConstant Class](amfDdsConstantClass.html)</dd>
        <dd>[DdsConstant Class Members](amfDdsConstantClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[DdsConstant MsgConFile Property](amfDdsConstantClassMsgConFileProperty.html)</dd>
        <dd>[DdsConstant MsgConLength Property](amfDdsConstantClassMsgConLengthProperty.html)</dd>
        <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
</dl>

