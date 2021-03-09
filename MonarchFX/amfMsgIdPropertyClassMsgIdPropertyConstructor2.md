---
title: MsgIdProperty Constructor(String)

Id: amfMsgIdPropertyClassMsgIdPropertyConstructor2
TocParent: amfMsgIdPropertyClassConstructors
TocOrder: 20

---

This method constructs a new instance of an **MsgIdProperty** object with values established.

#### Syntax
<pre class="prettyprint"> **BegConstructor MsgIdProperty Access(*Public)
  DclSrParm *propString*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt> *propString* 
        </dt>
        <dd>String containing an array of conditional value
        expressions in the format *'Condition MsgID MsgFile'* .</dd>
</dl>

#### Remarks
*'Condition'* is the indicator evaluated to determine when the message is to be used.

*'MsgID'* is a quoted literal containing the message id or the name of a character field containing the message id.

*'MsgFile'* is a quoted literal containing the name of the message file or the name of a character field containing the name of the message file.

If either the message id or the message file are defined using a named field, the field should be part of the same record format as the control to which this object applies.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[MsgIdProperty Class](amfMsgIdPropertyClass.html)</dd>
        <dd>[MsgIdProperty Class Members](amfMsgIdPropertyClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

