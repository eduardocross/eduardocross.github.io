---
title: DdsBarcode.AidKey Property

Id: amfDdsBarcodeClassAidKeyProperty
TocParent: amfDdsBarcodeClassProperties
TocOrder: 10

keywords: AidKey property
keywords: available aid keys
keywords: aidkeys, setting values
keywords: Aid Property Dialog, setting values
keywords: DdsBarcode.AidKey property
keywords: Web server controls [ASNA.Monarch], dds barcode aidkeys
keywords: how to, set dds barcode aidkeys
keywords: how to, get dds barcode aidkeys
keywords: display files, setting dds barcode aidkeys
keywords: display files, getting dds barcode aidkeys
keywords: web controls, setting dds barcode aidkeys
keywords: web controls, getting dds barcode aidkeys
keywords: dds barcode, aidkeys
keywords: field controls, dds barcode, aidkeys

---

Optional property that sets an IBM i Aid Key from the [ AidKeyIBM](amfAidKeyIBMEnumeration.html) enumeration to be submitted as soon as the barcode is identified.

#### Syntax
<pre class="syntax"> **BegProp AidKey Access(*Public) Type(ASNA.Monarch.WebDspF.AidProperty)
   BegGet:  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.AidProperty.** One of the enumeration values from [ AidKeyIBM](amfAidKeyIBMEnumeration.html) containing the function key value assigned to the button when it is pressed.

#### Remarks
To set the **AidKey** property at design-time, click on the right hand side of the property window and select the key from the drop-down list. Note that if the user enters a code manually, this property will not take effect.

Also note that the AidKey specified must be defined in the [FuncKeys](amfDdsRecordClassFuncKeysProperty.html) property of the [DdsRecord](amfDdsRecordClass.html) that contains it. Otherwise the AidKey function will not work.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBarcode Description](amfUnderstandingBarcodes.html)<br /> [DdsBarcode Class](amfDdsBarcodeClass.html) <br /> [DdsBarcode Class Members](amfDdsBarcodeClassMembers.html) <br />[DdsRecord Class](amfDdsRecordClass.html)<br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
