---
title: DdsSignature.ValueField Property

Id: amfDdsSignatureClassValueFieldProperty
TocParent: amfDdsSignatureClassPropertiesMain
TocOrder: 99

keywords: ValueField property
keywords: DdsSignature.ValueField Property
keywords: Signature Link Text
keywords: SignatureLinkText
keywords: Link Text, DdsSignature

---

This property sets the name of the value field.

#### Syntax
<pre class="prettyprint"> **BegProp ValueField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the name of the value field where the signature image will be stored. Defaults to blank.

#### Remarks
This sets the field where the image generated by completed signatures will be stored. This property will not function unless [ValueFieldLength](amfddsSignaturClassValueFieldLengthProperty.html) is also set.

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
