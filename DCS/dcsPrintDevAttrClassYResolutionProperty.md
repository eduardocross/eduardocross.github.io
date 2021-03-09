---
title: PrintDevAttr.YResolution Property

Id: dcsPrintDevAttrClassYResolutionProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 16

keywords: YResolution property
keywords: PrintDevAttr.YResolution property
keywords: printing, y-resolution, about this property
keywords: printing, graphics, y-resolution
keywords: how to, set/return y-resolution
keywords: how to, print graphics faster
keywords: y-resolution, set/return values
keywords: printers, y-resolution
keywords: printers, dots-per-inch
keywords: y-resolution, about
keywords: printer device parameters, y-resolution
keywords: printers, device parameters, y-resolution

---

The **YResolution** specifies the y-axis resolution (in dots-per-inch) when printing graphics.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public int YResolution { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property YResolution As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp YResolution Access(*Public) Type(*Integer) Len(4)
   BegGet,    BegSet** 
      </pre>

Property Value

Integer. Returns or sets a value that defines the resolution in which graphics will be printed. 
Remarks

Printers support one or more horizontal and vertical resolutions for faster graphics output. A resolution is an integer value specified in dots-per-inch (dpi), which indicates the number of distinct dots that the print head or inkjet can apply along the x- or the y-axis.

Typically, the x-y resolutions will be the same, such as300 x 300, or 600 x 600, etc. Since the x-y resolutions are the same, you only need to specify one resolution.
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
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

