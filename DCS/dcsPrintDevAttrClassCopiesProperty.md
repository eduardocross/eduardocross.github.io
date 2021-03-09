---
title: PrintDevAttr.Copies Property

Id: dcsPrintDevAttrClassCopiesProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 2

keywords: Copies property
keywords: PrintDevAttr.Copies property
keywords: printing, copies
keywords: printer device parameters, copies
keywords: printers, device parameters, copies
keywords: how to, print multiple copies
keywords: copies, specifying number of

---

The **Copies** property indicates the number of copies to be printed.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public int Copies { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property Copies As Integer** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Copies Access(*Public) Type(*Integer) Len(4)
   BegGet,   BegSet** 
      </pre>

Property Value

Integer. Returns or sets the number of copies to print. 
Remarks

The default number of copies is 1. When you are printing multiple copies, you may want to use the [Collate](dcsPrintDevAttrClassCollateProperty.html) property to have the copies collated.
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
      [Collate Property](dcsPrintDevAttrClassCollateProperty.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

