---
title: PrintDevAttr.LeftMargin Property

Id: dcsPrintDevAttrClassLeftMarginProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 6

keywords: LeftMargin property
keywords: PrintDevAttr.LeftMargin property
keywords: printing, left margin, about this property
keywords: printer device parameters, left margin
keywords: printers, device parameters, left margin
keywords: how to, set/return left margin size
keywords: left margins, set size of
keywords: left margins, return size of
keywords: left margins, about

---

The **LeftMargin** returns or sets the left margin of the output by the specified printer.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public int LeftMargin { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property LeftMargin As Integer** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp LeftMargin Access(*Public) Type(*Integer) Len(4)
   BegGet,    BegSet** 
      </pre>

Property Value

Integer. Returns or sets the size of the left margin of the output by the specified printer. 
Remarks

Each printer has a default left margin in which output will not be printed, as well as a [TopMargin](dcsPrintDevAttrClassTopMarginProperty.html) property.
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
      [TopMargin Property](dcsPrintDevAttrClassTopMarginProperty.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

