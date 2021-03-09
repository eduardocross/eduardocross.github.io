---
title: DdsSignature.ValueFieldLength Property

Id: amfDdsSignatureClassValueFieldLengthProperty
TocParent: amfDdsSignatureClassPropertiesMain
TocOrder: 100

keywords: ValueFieldLength property
keywords: DdsSignature.ValueFieldLength Property
keywords: Signature Link Text
keywords: SignatureLinkText
keywords: Link Text, DdsSignature

---

This property sets the length of the Value Field.

#### Syntax
<pre class="prettyprint"> **BegProp ValueFieldLength Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Int. A integer specifiying the total number of charactes in the Value Field. Default value is **8192** . Image data is recommened to have a value of at least 8k in length.

#### Remarks
This sets the total number of characters to be used in the Value Field where the image will be stored. This property will not function unless [ValueField](amfDdsSignatureClassValueFieldProperty.html) is populated with a valid string.

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

