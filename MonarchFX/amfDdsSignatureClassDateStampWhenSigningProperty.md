---
title: DdsSignature.DateStampWhenSigning Property

Id: amfDdsSignatureClassDateStampWhenSigningProperty
TocParent: amfDdsSignatureClassPropertiesMain
TocOrder: 15

keywords: DateStampWhenSigning property
keywords: DdsSignature.DateStampWhenSigning Property
keywords: Signature Date
keywords: Hide DdsSignature DateStamp
keywords: Date Stamp, DdsSignature

---

This property sets whether the current date is shown as a watermark when the user is signing.

#### Syntax
<pre class="prettyprint"> **BegProp DateStampWhenSigning Access(*Public) Type(*Bool)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. If **True** the current date will be shown as a watermark while the user signs and added to the final file.

#### Remarks
This sets whether the date is shown as a watermark. The date is merged with the signature into a single file when the image is saved.

The date is styled based on the 'locale' setting of the end-user's browser, so the datestamp will automatically be presented in a familiar format.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsSignature Description](amfUnderstandingSignatures.html)</dd>
        <dd>[DdsSignature Class](amfDdsSignatureClass.html)</dd>
        <dd>[DdsSignature Class Members](amfDdsSignatureClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
</dl>

