---
title: DdsSignature.PenDownOutsideSignatureWarningText Property

Id: amfDdsSignatureClassPenDownOutsideSignatureWarningTextProperty
TocParent: amfDdsSignatureClassPropertiesMain
TocOrder: 33

keywords: PenDownOutsideSignatureWarningText property
keywords: DdsSignature.PenDownOutsideSignatureWarningText Property
keywords: Pen Down Outside Signature Warning
keywords: Pen Down Warning
keywords: Pen Outside Warning Text, DdsSignature

---

This property sets the text that is displayed if pen input is detected outside of the signature area.

#### Syntax
<pre class="prettyprint"> **BegProp PenDownOutsideSignatureWarningText Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the warning message. Defaults to: "Sign Here!"

#### Remarks
This sets the text for the specific instance of the user making contact with parts of the page that are neither buttons nor the signature area. The text appears in large red letters inside of the signature area.

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

