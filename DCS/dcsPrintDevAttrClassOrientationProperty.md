---
title: PrintDevAttr.Orientation Property

Id: dcsPrintDevAttrClassOrientationProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 8

keywords: Orientation property
keywords: PrintDevAttr.Orientation property
keywords: PaperOrientation enumeration, used by
keywords: enumerations [DCS 16.0 PaperOrientation, used by
keywords: portrait orientation
keywords: landscape orientation
keywords: printing, orientation, about this property
keywords: printing, orientation, portrait
keywords: printing, orientation, landscape
keywords: printer device parameters, orientation
keywords: printers, device parameters, orientation
keywords: how to, determine printing orientation
keywords: print orientation, set/return values
keywords: print orientation, about

---

The **Orientation** property specifies the landscape/portrait orientation of paper in the printer. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public PaperOrientation Orientation { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property Orientation As [PaperOrientation](dcsPaperOrientationEnumeration.html)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Orientation Type(PaperOrientation) Access(*Public) <br />    BegGet,    BegSet** 
      </pre>

Property Value

[ASNA.DataGate.Common.PaperOrientation](dcsPaperOrientationEnumeration.html). Returns or sets an integer value indicating the orientation of the paper in the printer. 
Remarks

The paper orientation can be set to either <span style="FONT-WEIGHT: bold">Portrait</span> or <span style="FONT-WEIGHT: bold">Landscape</span> orientation.

<span style="FONT-WEIGHT: bold">Portrait</span> - The paper height is greater than the width.

<span style="FONT-WEIGHT: bold">Landscape - </span>The paper width is greater than the height. 
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
      [PaperOrientation Enumeration](dcsPaperOrientationEnumeration.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

