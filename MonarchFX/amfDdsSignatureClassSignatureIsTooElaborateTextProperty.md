---
title: DdsSignature.SignatureIsTooElaborateWarningText Property

Id: amfDdsSignatureClassSignatureIsTooElaborateWarningTextProperty
TocParent: amfDdsSignatureClassPropertiesMain
TocOrder: 37

keywords: SignatureIsTooElaborateWarningText property
keywords: DdsSignature.SignatureIsTooElaborateWarningText Property
keywords: Signature Warning Text
keywords: Signature Too Elaborate
keywords: Warning Text, DdsSignature

---

This property sets the text that is displayed if the user attempts to enter a signature that is too elaborate for the system to easily store.

#### Syntax
<pre class="prettyprint"> **BegProp SignatureIsTooElaborateWarningText Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the warning message. Defaults to: ""Signature is too elaborate, some strokes will be lost."

#### Remarks
This sets the text for the specific instance of the signature being too elaborate. The warning is called when there is not enough space in [ValueField](amfDdsSignatureClassValueFieldProperty.html) to store all the strokes that make up the signature. Some strokes will be lost when submitting the signature. If this happens frequently it is recommended that the length of the ValueField be increased by changing the [ValueFieldLength](amfDdsSignatureClassValueFieldLengthProperty.html) property.

For more information see the [Signature Storage Considerations](amfUnderSignatureStorage.html) page.

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

