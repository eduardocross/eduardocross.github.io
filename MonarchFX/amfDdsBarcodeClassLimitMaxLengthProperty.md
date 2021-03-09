---
title: DdsBarcode.LimitMaxLength Property

Id: amfDdsBarcodeClassLimitMaxLengthProperty
TocParent: amfDdsBarcodeClassProperties
TocOrder: 17

keywords: LimitMaxLength property
keywords: LimitMaxLength, setting values
keywords: LimitMaxLength Property Dialog, setting values
keywords: DdsBarcode.LimitMaxLength roperty
keywords: dds barcode, LimitMaxLength
keywords: field controls, dds barcode, LimitMaxLength

---

Sets whether or not to limit the maximum number of characters that may be keyed into the Code Length value. (Defaults to <code>True</code>.)

#### Syntax
<pre class="syntax"> **BegProp LimitMaxLength Access(*Public) Type(*Boolean)
   BegGet:  BegSet** </pre>

#### Property Values
**Boolean.** If <code>TRUE</code>, the maximum number of characters will be the number required by the largest selected BarcodeFormat. If <code>FALSE</code>, any number of characters may be entered.

#### Remarks
To set the LimitMaxLength property at design-time, click on the right hand side of the property window and select the key from the drop-down list.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBarcode Class](amfDdsBarcodeClass.html) <br /> [DdsBarcode Class Members](amfDdsBarcodeClassMembers.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
