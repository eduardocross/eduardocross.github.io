---
title: FuncKey Property

Id: amfDdsPushButtonFieldChoiceClassFuncKeyProperty
TocParent: amfDdsPushButtonFieldChoiceClassPropertiesMain

keywords: FuncKey property
keywords: available aid keys
keywords: FuncKeys, setting values
keywords: Aid Property Dialog, setting values
keywords: DdsPushButtonFieldChoice.FuncKey property
keywords: Web server controls [ASNA.Monarch], dds button FuncKeys
keywords: how to, set dds button FuncKeys
keywords: how to, get dds button FuncKeys
keywords: display files, setting dds button FuncKeys
keywords: display files, getting dds button FuncKeys
keywords: web controls, setting dds button FuncKeys
keywords: web controls, getting dds button FuncKeys
keywords: dds button, FuncKeys
keywords: field controls, dds button, FuncKeys

---

Gets or sets the function key that will be enetered when this choice is selected.

#### Syntax
<pre class="syntax"> **BegProp FuncKey Access(*Public) Type(ASNA.Monarch.WebDspF.AidKey)
   BegGet:  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.AidKey.** One of the enumeration values from [ AidKeyIBM](amfAidKeyIBMEnumeration.html) containing the function key value assigned to the button when it is pressed. (Default: "Enter.")

#### Remarks
To set the **FuncKey** property at design-time, click on the right hand side of the property window and select the key from the drop-down list. This key must also be defined in either the [FuncKeys](amfDdsRecordClassFuncKeysProperty.html) or, more rarely, [DdsPushButtonFieldChoices](amfDdsRecordClassDdsPushButtonFieldChoicesProperty.html) property of the [DdsRecord](amfDdsRecordClass.html), [DdsFile](amfDdsFileClass.html), [DdsSubfile](amfDdsSubfileClass.html) or [DdsSubfileControl](amfDdsSubfileClass.html) control that contains it.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsPushButtonFieldChoice Description](amfUnderstandingSelectionFields.html)<br /> [DdsPushButtonFieldChoice Class](amfDdsPushButtonFieldChoiceClass.html) <br /> [DdsPushButtonFieldChoice Class Members](amfDdsPushButtonFieldChoiceClassMembers.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
