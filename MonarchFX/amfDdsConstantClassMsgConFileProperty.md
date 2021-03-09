---
title: DdsConstant.MsgConFile Property

Id: amfDdsConstantClassMsgConFileProperty
TocParent: amfDdsConstantClassPropertiesMain
TocOrder: 10

keywords: MsgConFile property
keywords: DdsConstant.MsgConFile property
keywords: Web server controls [ASNA.Monarch], setting MSGCON file name
keywords: how to, set MSGCON file name
keywords: how to, get MSGCON file name
keywords: message files, setting MSGCON file name
keywords: message files, getting MSGCON file name
keywords: web controls, setting MSGCON file name
keywords: web controls, getting MSGCON file name
keywords: field controls, MSGCON file name
keywords: MSGCON, file name

---

Gets or sets a string containing the Name of the Message File without the **amfx** extension.

#### Syntax
<pre class="prettyprint"> **BegProp MsgConFile Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the Name of the Message File without the **amfx** extension.

#### Remarks
The absolute path to the Message File will be generated at run-time by appending the **MsgConFile** value to the value of **MonarchMessageFileFolder** entry in Web.Config. Together with [MsgConId](amfDdsConstantClassMsgConIdProperty.html) and [MsgConLength](amfDdsConstantClassMsgConLengthProperty.html), **MsgConFile** is used to implement the MSGCON DDS keyword.

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
        <dd>[DdsConstant MsgConId Property](amfDdsConstantClassMsgConIdProperty.html)</dd>
        <dd>[DdsConstant MsgConLength Property](amfDdsConstantClassMsgConLengthProperty.html)</dd>
        <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
</dl>

