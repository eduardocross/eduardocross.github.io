---
title: PrintDevAttr.Width Property

Id: dcsPrintDevAttrClassWidthProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 15

keywords: Width property
keywords: PrintDevAttr.Width property
keywords: printing, width, about this property
keywords: how to, set/return width of paper
keywords: width, set/return values
keywords: printers, width of paper
keywords: paper width, specifying
keywords: printer device parameters, width
keywords: printers, device parameters, width

---

The **Width** specifies the width of paper in the printer.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public int Width { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property Width As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Width Access(*Public) Type(*Integer) Len(4)
   BegGet,    BegSet** 
      </pre>

Property Value

Integer. Returns or sets the width of the paper in the printer. 
Remarks

The default paper width will be based upon the [ orientation](dcsPrintDevAttrClassOrientationProperty.html) property of the paper in the printer. These values are in tenths of a millimeter.
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

