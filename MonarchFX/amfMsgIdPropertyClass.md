---
title: MsgIdProperty Class

Id: amfMsgIdPropertyClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 600

keywords: MsgIdProperty class, about MsgIdProperty
keywords: classes [ASNA.Monarch.WebDspF], MsgIdProperty class
keywords: MessageID Property Editor, container
keywords: message files
keywords: message ID editor

---

The **MsgIdProperty** is a derived class that is a container for the **MessageID Property Editor** dialog values.

For a list of all members of this type, see [ MsgIdProperty Members](amfMsgIdPropertyClassMembers.html).
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
        [ASNA.Monarch.WebDspF.ConditionalProperty](amfConditionalPropertyClass.html)
 **ASNA.Monarch.WebDspF.MsgIdProperty** </pre>

#### Syntax
<pre class="prettyprint"> **Public class MsgIdProperty Inherits ConditionalProperty** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of **MsgIdProperty** represents an array of condition/Message Id/Message File values set when the data field's [ MessageId](amfDdsDataFieldClassMessageIdProperty.html) property is selected. The **MessageId Property Editor** dialog is displayed as shown below.
<dl><dd>
        ![](Images/zzMessageIdProperty.jpg)
      </dd></dl>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[MsgIdProperty Class Members](amfMsgIdPropertyClassMembers.html)</dd>
        <dd>[ConditionalProperty Class](amfConditionalPropertyClass.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

