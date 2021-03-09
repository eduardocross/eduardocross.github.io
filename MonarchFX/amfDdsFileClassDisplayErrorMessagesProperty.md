---
title: DdsFile.DisplayErrorMessages Property

Id: amfDdsFileClassDisplayErrorMessagesProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 110

keywords: DisplayErrorMessages property
keywords: DdsFile.DisplayErrorMessages property
keywords: how to, control display of messages
keywords: error messages, controlling display
keywords: messages, controlling errors displayed
keywords: web controls, controlling errors displayed
keywords: display files, controlling errors displayed

---

Gets or sets a boolean value True if messages will be rendered inside this control, otherwise False.

#### Syntax
<pre class="prettyprint"> **BegProp DisplayErrorMessages Access(*Public) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Value
Boolean **True** if messages are to rendered inside this control, otherwise **False** .

#### Remarks
To set this property at design-time, click on the right of the **DisplayErrorMessages** property and the select true or false from the drop-down list.

This property must be **False** in order for the [ DdsMessagePanel](amfDdsMessagePanelClass.html) to become visible when a [ DdsCharField](amfDdsCharFieldClass.html) or [ DdsDecField](amfDdsDecFieldClass.html) control's [ ErrorMessage](amfDdsFieldClassErrorMessageProperty.html) or [ ErrorMessageID](amfDdsFieldClassErrorMessageIdProperty.html) condition is **True** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ DdsFile.FuncKeys Property](amfDdsFileClassFuncKeysProperty.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
