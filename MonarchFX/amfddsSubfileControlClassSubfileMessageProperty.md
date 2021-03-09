---
title: DdsSubfileControl.SubfileMessage Property

Id: amfddsSubfileControlClassSubfileMessageProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 200

keywords: SubfileMessage property
keywords: SubfileMessage Property Editor, setting values
keywords: DdsSubfileControl.SubfileMessage property
keywords: conditioning expressions, controlling subfile control messages
keywords: indicator expressions, controlling subfile control messages
keywords: message files, message values
keywords: error message values
keywords: error messages, values
keywords: message files, display conditions
keywords: error messages, display condition
keywords: error message display condition
keywords: how to, set message values
keywords: how to, get message values
keywords: subfiles, messages
keywords: subfile records, setting messages
keywords: subfile records, getting messages
keywords: subfile controls, setting messages
keywords: subfile controls, getting messages
keywords: web controls, messages

---

Gets or sets a new instance of an [ ErrMsgProperty](amfErrMsgPropertyClass.html) object that identifies a message to be associated with this record.

#### Syntax
<pre class="prettyprint"> **BegProp SubfileMessage Access(*Public) Type([ErrMsgProperty](amfErrMsgPropertyClass.html))
   BegGet;  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.ErrMsgProperty** object continuing the conditional property values for the record.

#### Remarks
<p>To set this property at design-time, click on the right of the **SubfileMessage** property and the SubfileMessage Property Editor will display as shown below. Enter the value and the condition controlling the message. See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) for more information.

![](Images/zzSubfileControlSubfileMessage.JPG) 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
