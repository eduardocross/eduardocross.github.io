---
title: PrintDevAttr Class

Id: dcsPrintDevAttrClass
TocParent: dcsASNADataGateProvidersClasses
TocOrder: 4

keywords: classes [DCS 16.0 PrintDevAttr class
keywords: PrintDevAttr class
keywords: PrintDevAttr class, about PrintDevAttr class
keywords: printers, about device parameters
keywords: printer device parameters, about
keywords: printing, about device parameters

---

The <span> **PrintDevAttr** </span> class is a representation of the device parameters. 

For a list of all members of this type, see [PrintDevAttr Members](dcsPrintDevAttrMembers.html).

[ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) <br /> **ASNA.DataGate.Providers.<span>PrintDevAttr</span>** 
<pre class="prettyprint">[Prototype in C#]
  public class PrintDevAttr | System.Collections.Hashtable</pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

The **PrintDevAttr** class is a representation of the device parameters ([PrintDevAttr](dcsPrintDevAttrClassPrintDevAttrConstructor.html)) constructor used by [IPrintProperties](dcsIPrintPropertiesClass.html) object files, for the properties listed below.

[Collate](dcsPrintDevAttrClassCollateProperty.html) controls whether the output produced by capable printers should be collated or not. [Color](dcsPrintDevAttrClassColorProperty.html) controls whether non-monochrome output is to be produced by color-capable printers or not. [Copies](dcsPrintDevAttrClassCopiesProperty.html) sets the number of copies to be produced by the printer.

[DefaultSource](dcsPrintDevAttrClassDefaultSourceProperty.html) controls the tray source of paper in the printer. [ Duplex](dcsPrintDevAttrClassDuplexProperty.html) controls the standard duplex setting for use by capable printers. 

[FormName](dcsPrintDevAttrClassFormNameProperty.html) sets the name of the print format to use, such as "A4", "Letter", "Tabloid", "Ledger", "Envelope", etc. [LeftMargin](dcsPrintDevAttrClassLeftMarginProperty.html) sets the size of left margin in output produced by the printer. [ Length](dcsPrintDevAttrClassLengthProperty.html) sets the length of paper in the printer. [ Orientation](dcsPrintDevAttrClassOrientationProperty.html) controls the Landscape/portrait orientation of paper in the printer.

[PrinterName](dcsPrintDevAttrClassPrinterNameProperty.html) sets the name of an accessible printer device. [ Quality](dcsPrintDevAttrClassQualityProperty.html) controls the standard quality rating for output produced by the printer. [Scale](dcsPrintDevAttrClassScaleProperty.html) sets the percentage factor by which the printed output is to be scaled. [ Size](dcsPrintDevAttrClassSizeProperty.html) controls the standard sheet size of paper in the printer.

[TopMargin](dcsPrintDevAttrClassTopMarginProperty.html) sets the size of top margin in output produced by the printer. [ TTOption](dcsPrintDevAttrClassTTOptionProperty.html) controls the options for using TrueType fonts in documents output by capable printers. [ Width](dcsPrintDevAttrClassWidthProperty.html) sets the width of paper in the printer. [ YResolution](dcsPrintDevAttrClassYResolutionProperty.html) sets the y-axis resolution (in dots-per-inch) when printing graphics. 
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Providers

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [PrintDevAttr Members](dcsPrintDevAttrMembers.html)
      <br />
      [IPrintProperties Class](dcsIPrintPropertiesClass.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

