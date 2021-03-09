---
title: DdsDataField.MessageId Property

Id: amfDdsDataFieldClassMessageIdProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 60

keywords: MessageId property
keywords: DdsDataField.MessageId property
keywords: MessageID Property Editor, setting values
keywords: Web server controls [ASNA.Monarch], setting field message ids
keywords: how to, set field control message ids
keywords: how to, get field control message ids
keywords: display files, setting field control message ids
keywords: display files, getting field control message ids
keywords: web controls, setting field control message ids
keywords: web controls, getting field control message ids
keywords: field controls, message ids
keywords: indicator expressions, field control message ids
keywords: conditioning expressions, field control message ids

---

Gets or sets the conditional value that controls the messages to be associated with this field when a message file is used.

#### Syntax
<pre class="prettyprint"> **BegProp MessageId Access(*Public) Type(ASNA.Monarch.WebDspF.MsgIdProperty)
   BegGet;  BegSet** </pre>

#### Property Values
[ ASNA.Monarch.WebDspF.MsgIdProperty](amfMsgIdPropertyClass.html) with the conditional value that controls the messages to be associated with this field.

#### Remarks
To set the **MessageId** property, click on the right hand side of the property window, and the **MessageId Property Editor** window will display as shown below. Each conditioned message is composed of a message file (MsgFile) and a message id (MsgID); for either of these two values, you can enter a quoted literal or the name of a character field that should be part of the same record format as the field owning the MessageId property.

![](Images/zzMessageIdProperty.jpg) 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
