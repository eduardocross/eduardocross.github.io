---
title: PrintDevAttr.TopMargin Property

Id: dcsPrintDevAttrClassTopMarginProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 13

keywords: TopMargin property
keywords: PrintDevAttr.TopMargin property
keywords: printing, top margin, about this property
keywords: how to, set/return top margin
keywords: top margin, set/return values
keywords: printers, top margin
keywords: top margin, about
keywords: printer device parameters, top margin
keywords: printers, device parameters, top margin

---

The **TopMargin** specifies the size of top margin in output produced by the printer.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public int TopMargin { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property TopMargin As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp TopMargin Access(*Public) Type(*Integer) Len(4)
   BegGet,    BegSet** 
      </pre>

Property Value

Integer. Returns or sets the size of the top margin of the output by the specified printer. 
Remarks

Each printer has a default top margin in which output will not be printed, as well as a default [Left Margin](dcsPrintDevAttrClassLeftMarginProperty.html).
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
      [LeftMargin Property](dcsPrintDevAttrClassLeftMarginProperty.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

