---
title: DdsConstant.EncodedLiteral Method

Id: amfDdsConstantClassEncodedLiteralMethod
TocParent: amfDdsConstantClassMethods
TocOrder: 10

keywords: EncodedLiteral method
keywords: DdsConstant.EncodedLiteral method
keywords: Web server controls [ASNA.Monarch], encoding valid XML field excluding spaces
keywords: how to, encode valid XML field excluding spaces
keywords: display files, encoding valid XML field excluding spaces
keywords: web controls, encoding valid XML field excluding spaces
keywords: field controls, encoding valid XML excluding spaces
keywords: XML, encoding field controls excluding spaces

---

This method takes a string value and encodes it to a valid XML element.

#### Syntax
<pre class="syntax"> **BegFunc EncodedLiteral Access(*Public) Type(*String)
  DclSrParm *text*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *text* 
        </dt>
        <dd>The text value to be encoded.</dd>
</dl>

#### Return Value
String containing the *text* value with any replacement characters. &lt;, &gt;, and &amp; become &amp;lt;, &amp;gt;, and &amp;amp respectively. Embedded spaces are not encoded with a replacement character.

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

