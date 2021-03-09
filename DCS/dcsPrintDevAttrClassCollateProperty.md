---
title: PrintDevAttr.Collate Property

Id: dcsPrintDevAttrClassCollateProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 0

keywords: Collate property
keywords: PrintDevAttr.Collate property
keywords: printing, collate multiple copies
keywords: printer device parameters, collate multiple copies
keywords: printers, device parameters, collate
keywords: collate copies, about
keywords: copies, collate
keywords: how to, collate multiple copies

---

The **Collate** property indicates the output produced by capable printers should be collated when this property is set to **True** .
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public bool Collate { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property Collate As Boolean** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Collate Access(*Public) Type(*Boolean)
   BegGet,   BegSet** 
      </pre>

Property Value

Boolean. Returns or sets a value indicating whether the printed output should be collated when printing multiple copies. 
Remarks

Setting this property to True will allow multiple copies to be collated. However, this property is applicable only when printing multiple copies or when the [Copies](dcsPrintDevAttrClassCopiesProperty.html) property is &gt;1.
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Providers

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [PrintDevAttr Class](dcsPrintDevAttrClass.html)
      <br />
      [PrintDevAttr Class Members](dcsPrintDevAttrMembers.html)
      <br />
      [Copies Property](dcsPrintDevAttrClassCopiesProperty.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

