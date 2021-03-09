---
title: PrintDevAttr.DefaultSource Property

Id: dcsPrintDevAttrClassDefaultSourceProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 3

keywords: DefaultSource property
keywords: PrintDevAttr.DefaultSource property
keywords: printing, paper source, about this property
keywords: printer device parameters, paper source
keywords: printers, device parameters, paper source
keywords: how to, set paper source to be used
keywords: how to, return paper source to be used
keywords: paper source, set/return values
keywords: paper source, about

---

The **DefaultSource** property specifies the printer tray to be used when printing. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public System.Drawing.Printing.PaperSourceKind DefaultSource { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property DefaultSource As System.Drawing.Printing.PaperSourceKind** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp DefaultSource Type(System.Drawing.Printing.PaperSourceKind) Access(*Public) <br />      BegGet,    BegSet** 
      </pre>

Property Value

System.Drawing.Printing.PaperSourceKind. Returns or sets an interger value that determines the paper tray to use in the printer. 
Remarks

Common printer tray options include upper tray, lower tray, middle tray, manual feed, envelopes, etc. Please note that each printer will contain the paper tray options that are available for that printer.

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Providers

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [PrintDevAttr Class](dcsPrintDevAttrClass.html)
      <br />
      [PrintDevAttr Class Members](dcsPrintDevAttrMembers.html)
      <br />System.Drawing.Printing.PaperSourceKind Enumeration
      <br />[ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

