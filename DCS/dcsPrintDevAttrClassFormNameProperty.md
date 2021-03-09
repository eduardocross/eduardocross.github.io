---
title: PrintDevAttr.FormName Property

Id: dcsPrintDevAttrClassFormNameProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 5

keywords: FormName property
keywords: PrintDevAttr.FormName property
keywords: printing, format name, about this property
keywords: printer device parameters, format name
keywords: printers, device parameters, format name
keywords: how to, return form names for printer
keywords: how to, set form names for printer
keywords: form names, set/return print values
keywords: form names, about print

---

The **FormName** specifies the name of the print format to use.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public String FormName { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property FormName As String** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp FormName Access(*Public) Type(*String) Len(4)
   BegGet,    BegSet** 
      </pre>

Property Value

String. Returns or sets the name of the print format to use, such as "A4", "Letter", "Tabloid", "Ledger", "Envelope", etc. 
Remarks

Refer to System.Drawing.Printing.PaperKind Enumeration for available print form names.
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

