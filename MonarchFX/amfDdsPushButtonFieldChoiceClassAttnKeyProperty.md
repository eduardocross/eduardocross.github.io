---
title: AttnKey Property

Id: amfDdsPushButtonFieldChoiceClassAttnKeyProperty
TocParent: amfDdsPushButtonFieldChoiceClassPropertiesMain

keywords: AttnKey property
keywords: available aid keys
keywords: AttnKeys, setting values
keywords: Aid Property Dialog, setting values
keywords: DdsPushButtonFieldChoice.AttnKey property
keywords: Web server controls [ASNA.Monarch], dds button AttnKeys
keywords: how to, set dds button AttnKeys
keywords: how to, get dds button AttnKeys
keywords: display files, setting dds button AttnKeys
keywords: display files, getting dds button AttnKeys
keywords: web controls, setting dds button AttnKeys
keywords: web controls, getting dds button AttnKeys
keywords: dds button, AttnKeys
keywords: field controls, dds button, AttnKeys

---

Gets or sets the function key defined in the **DdsRecord** to which this button control corresponds.

#### Syntax
<pre class="syntax"> **BegProp AttnKey Access(*Public) Type(ASNA.Monarch.WebDspF.AidKey)
   BegGet:  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.AidKey.** One of the enumeration values from [ AidKeyIBM](amfAidKeyIBMEnumeration.html) containing the attention key value assigned to the button when it is pressed. (Default: Unknown")

#### Remarks
To set the **AttnKey** property at design-time, click on the right hand side of the property window and select the key from the drop-down list. This key must also be defined in either the [FuncKeys](amfDdsRecordClassFuncKeysProperty.html) or, more rarely, [DdsPushButtonFieldChoices](amfDdsRecordClassDdsPushButtonFieldChoicesProperty.html) property of the [DdsRecord](amfDdsRecordClass.html), [DdsFile](amfDdsFileClass.html), [DdsSubfile](amfDdsSubfileClass.html) or [DdsSubfileControl](amfDdsSubfileClass.html) control that contains it.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsPushButtonFieldChoice Description](amfUnderstandingSelectionFields.html)<br /> [DdsPushButtonFieldChoice Class](amfDdsPushButtonFieldChoiceClass.html) <br /> [DdsPushButtonFieldChoice Class Members](amfDdsPushButtonFieldChoiceClassMembers.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
