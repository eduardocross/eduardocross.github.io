---
title: DdsButton.AidKey Property

Id: amfDdsButtonClassAidKeyProperty
TocParent: amfDdsButtonClassProperties
TocOrder: 10

keywords: AidKey property
keywords: available aid keys
keywords: aidkeys, setting values
keywords: Aid Property Dialog, setting values
keywords: DdsButton.AidKey property
keywords: Web server controls [ASNA.Monarch], dds button aidkeys
keywords: how to, set dds button aidkeys
keywords: how to, get dds button aidkeys
keywords: display files, setting dds button aidkeys
keywords: display files, getting dds button aidkeys
keywords: web controls, setting dds button aidkeys
keywords: web controls, getting dds button aidkeys
keywords: dds button, aidkeys
keywords: field controls, dds button, aidkeys

---

Gets or sets the function key defined in the **DdsRecord** to which this button control corresponds.

#### Syntax
<pre class="syntax"> **BegProp AidKey Access(*Public) Type(ASNA.Monarch.WebDspF.AidProperty)
   BegGet:  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.AidProperty.** One of the enumeration values from [ AidKeyIBM](amfAidKeyIBMEnumeration.html) containing the function key value assigned to the button when it is pressed.

#### Remarks
To set the **AidKey** property at design-time, click on the right hand side of the property window and select the key from the drop-down list. This key must also be defined in either the [FuncKeys](amfDdsRecordClassFuncKeysProperty.html) or, more rarely, [AttnKeys](amfDdsRecordClassAttnKeysProperty.html) property of the [DdsRecord](amfDdsRecordClass.html), [DdsFile](amfDdsFileClass.html), [DdsSubfile](amfDdsSubfileClass.html) or [DdsSubfileControl](amfDdsSubfileClass.html) control that contains it.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsButton Description](amfUnderstandingButtons.html)<br /> [DdsButton Class](amfDdsButtonClass.html) <br /> [DdsButton Class Members](amfDdsButtonClassMembers.html) <br />[DdsRecord Class](amfDdsRecordClass.html)<br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
