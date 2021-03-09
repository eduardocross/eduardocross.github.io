---
title: PrintDevAttr.Duplex Property

Id: dcsPrintDevAttrClassDuplexProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 4

keywords: Duplex property
keywords: PrintDevAttr.Duplex property
keywords: printing, duplex, about this property
keywords: printer device parameters, duplex
keywords: printers, device parameters, duplex
keywords: how to, print duplex
keywords: how to, print double-sided
keywords: double-sided printing
keywords: duplex, set/return print values
keywords: duplex, about

---

The **Duplex** property specifies the standard duplex (double-sided) setting for use by capable printers. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public System.Drawing.Printing.Duplex Duplex { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property Duplex As System.Drawing.Printing.Duplex** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Duplex Type(System.Drawing.Printing.Duplex) Access(*Public) <br /> BegGet,    BegSet** 
      </pre>

Property Value

System.Drawing.Printing.Duplex. Returns or sets an integer duplex setting that defines whether the file will be printed duplex and whether the duplex output will have horizontal or vertical binding. 
Remarks

The printer must be capable of printing duplex to use this property.
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Providers

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [PrintDevAttr Class](dcsPrintDevAttrClass.html)
      <br />
      [PrintDevAttr Class Members](dcsPrintDevAttrMembers.html)
      <br />System.Drawing.Printing.Duplex 
Enumeration
      <br />[ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

