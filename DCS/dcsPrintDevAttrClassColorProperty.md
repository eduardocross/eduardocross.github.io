---
title: PrintDevAttr.Color Property

Id: dcsPrintDevAttrClassColorProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 1

keywords: Color property
keywords: PrintDevAttr.Color property
keywords: printing, color
keywords: printer device parameters, color
keywords: printers, device parameters, color
keywords: how to, print in color
keywords: colors, printing in

---

The **Color** property indicates that non-monochrome output is to be produced by color-capable printers when this property is set to **True** .
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public bool Color { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property Color As Boolean** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Color Access(*Public) Type(*Boolean)
   BegGet,    BegSet** 
      </pre>

Property Value

Boolean. Returns or sets a value indicating whether the printed output will be printed in color. 
Remarks

Setting this property to **True** will allow the print out to be printed in color, as long as a color printer is specified.
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

