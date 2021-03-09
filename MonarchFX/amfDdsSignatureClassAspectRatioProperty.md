---
title: DdsSignature.AspectRatio Property

Id: amfDdsSignatureClassAspectRatioProperty
TocParent: amfDdsSignatureClassPropertiesMain
TocOrder: 05

keywords: AspectRatio property
keywords: DdsSignature.AspectRatio Property
keywords: Signature Link Text
keywords: SignatureLinkText
keywords: Link Text, DdsSignature

---

This property sets the aspect ratio for the DdsSignature control.

#### Syntax
<pre class="prettyprint"> **BegProp AspectRatio Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string following this format: **x:y** Where **x** is the relative width and **y** is the relative height. Defaults to **3:1** .

#### Remarks
This sets the Aspect ratio of the signature control. This allows for more responsive design than assigning a specific height and width.

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

