---
title: PrintDevAttr.TTOption Property

Id: dcsPrintDevAttrClassTTOptionProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 14

keywords: TTOption property
keywords: PrintDevAttr.TTOption property
keywords: PrintTrueType enumeration, used by
keywords: enumerations [DCS 16.0 PrintTrueType, used by
keywords: printing, true type fonts, about this property
keywords: printing, graphics, true type fonts
keywords: how to, specify true type font
keywords: true type fonts, set/return option
keywords: printers, true type font indicated
keywords: true type fonts, about
keywords: printer device parameters, true type font
keywords: printers, device parameters, true type font

---

The **TTOption** property specifies the option for using TrueType Fonts in documents output by capable printers. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public PrintTrueType TTOption { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property TTOption As [PrintTrueType](dcsPrintTrueTypeEnumeration.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp TTOption Type(PrintTrueType) Access(*Public) <br />    BegGet,    BegSet** 
      </pre>

Property Value

[ASNA.DataGate.Common.PrintTrueType](dcsPrintTrueTypeEnumeration.html). Returns or sets an interger value that defines how true type fonts will be printed. 
Remarks

True Type fonts can either be printed as graphics, downloaded as soft fonts, or substitute device fonts for true type fonts.
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
      [PrintTrueType Enumeration](dcsPrintTrueTypeEnumeration.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

