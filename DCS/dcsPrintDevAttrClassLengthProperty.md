---
title: PrintDevAttr.Length Property

Id: dcsPrintDevAttrClassLengthProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 7

keywords: Length property
keywords: PrintDevAttr.Length property
keywords: printing, paper length, about this property
keywords: printer device parameters, length of paper
keywords: printers, device parameters, length of paper
keywords: how to, set/return length of paper
keywords: length of paper, set size of
keywords: length of paper, return size of
keywords: length of paper, about property

---

The **Length** specifies the length of paper in the printer.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public int Length { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property Length As Integer** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Length Access(*Public) Type(*Integer) Len(4)
   BegGet,    BegSet** 
      </pre>

Property Value

Integer. Returns or sets the length of paper in the printer. 
Remarks

The default paper length will be based upon the [ Orientation](dcsPrintDevAttrClassOrientationProperty.html) property of the paper in the printer. These values are in tenths of a millimeter.
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
      [Orientation Property](dcsPrintDevAttrClassOrientationProperty.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

