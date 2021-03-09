---
title: PrintDevAttr.Size Property

Id: dcsPrintDevAttrClassSizeProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 12

keywords: Size property
keywords: PrintDevAttr.Size property
keywords: printing, paper size, about this property
keywords: printer device parameters, paper size
keywords: printers, device parameters, paper size
keywords: how to, determine printing orientation
keywords: paper, specifying size
keywords: paper size, set/return values
keywords: paper size, about

---

The **Size** property specifies the standard sheet size of paper in the printer. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public System.Drawing.Printing.PaperKind Size { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property Size As 
System.Drawing.Printing.PaperKind** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Size Type(System.Drawing.Printing.PaperKind) Access(*Public) <br />    BegGet,    BegSet** 
      </pre>

Property Value

System.Drawing.Printing.PaperKind. The type of paper to use. 
Remarks

This property must be set prior to opening the printer file. If **Size** is not set, the paper size specified for the print file will be used. Please note that the printer must be capable of printing the size of paper 
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Providers

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [PrintDevAttr Class](dcsPrintDevAttrClass.html)
      <br />
      [PrintDevAttr Class Members](dcsPrintDevAttrMembers.html)
      <br />System.Drawing.Printing.PaperKind 
Enumeration
      <br />[ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

