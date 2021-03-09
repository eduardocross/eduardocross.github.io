---
title: DdsSignature.InvalidEmptySignatureErrorText Property

Id: amfDdsSignatureClassInvalidEmptySignatureErrorTextProperty
TocParent: amfDdsSignatureClassPropertiesMain
TocOrder: 30

keywords: InvalidEmptySignatureErrorText property
keywords: DdsSignature.InvalidEmptySignatureErrorText Property
keywords: Empty Signature Error Text
keywords: Invalid Empty Signature Error Text
keywords: Error Text, Empty Signature

---

This property sets the alert text to display when a user accepts without signing. 

#### Syntax
<pre class="prettyprint"> **BegProp InvalidEmptySignatureErrorText Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string that will populate the alert text displayed when a user touches the **Done** button before signing. Defaults to **Signature required!** 

If set to an empty string, validation is disabled and the blank image (with date if specified by the [DateStampWhenSigning](amfddsSignatureClassDateStampWhenSigningProperty.html) property) will be saved to the [ValueField](amfddsSignatureClassValueFieldProperty.html) rather than leaving it blank.

#### Remarks
This sets the text to display when a user taps or clicks the **Done** button before signing.

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

