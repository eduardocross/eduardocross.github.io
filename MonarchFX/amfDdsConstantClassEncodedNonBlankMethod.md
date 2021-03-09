---
title: DdsConstant.EncodedNonBlank Method

Id: amfDdsConstantClassEncodedNonBlankMethod
TocParent: amfDdsConstantClassMethods
TocOrder: 20

keywords: EncodedNonBlank method
keywords: DdsConstant.EncodedNonBlank method
keywords: Web server controls [ASNA.Monarch], encoding valid XML field including spaces
keywords: how to, encode valid XML field including spaces
keywords: display files, encoding valid XML field including spaces
keywords: web controls, encoding valid XML field including spaces
keywords: field controls, encoding valid XML including spaces
keywords: XML, encoding field controls including spaces

---

This method takes a string value and encodes it to a valid XML element.

#### Syntax
<pre class="syntax"> **BegFunc EncodedNonBlank Access(*Public) Type(*String)
  DclSrParm text Type(*String)** </pre>

#### Parameters
<dl>
        <dt>text</dt>
        <dd>String. The value to be encoded.</dd>
</dl>

#### Return Value
String containing the *text* value with any replacement characters. "&lt;", "&gt;", and "&amp;" become "&amp;lt;" "&amp;gt;", and "&amp;amp" respectively. In addition, consecutive spaces (after the first) are replaced with "&amp;nbsp;".

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsConstant Class](amfDdsConstantClass.html)</dd>
        <dd>[DdsConstant Class Members](amfDdsConstantClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

