---
title: PrintDevAttr.Scale Property

Id: dcsPrintDevAttrClassScaleProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 11

keywords: printing, scale, about this property
keywords: how to, set/return print scale
keywords: scale, set/return values
keywords: printers, scale
keywords: scale, about
keywords: printer device parameters, scale
keywords: printers, device parameters, scale
keywords: Scale property
keywords: PrintDevAttr.Scale property

---

The **Scale** specifies the percentage factor by which the printed output is to be scaled.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public int Scale { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property Scale As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Scale Access(*Public) Type(*Integer4)
   BegGet,    BegSet** 
      </pre>

Property Value

Integer. Returns or sets the percentage in which the printed output is to be scaled. 
Remarks

The specified printer must support the output to be scaled or resized.
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
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

