---
title: PrintDevAttr Members

Id: dcsPrintDevAttrMembers
TocParent: dcsPrintDevAttrClass
TocOrder: 0

keywords: members [DCS 16.0 PrintDevAttr class
keywords: PrintDevAttr class, all members

---

For additional methods see [PrintDevAttr Overview](dcsPrintDevAttrClass.html).
Public Constructors

<br />

<table class="dtTABLE" id="table4" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ PrintDevAttr](dcsPrintDevAttrClassPrintDevAttrConstructors.html) 
</td>
            <td colspan="1" rowspan="1">

Initializes a new instance of the PrintDevAttr class.
</td>
          </tr>
</table>

Public Methods

<br />

<table class="dtTABLE" id="Table3" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ReadXml](dcsPrintDevAttrClassReadXmlMethod.html)
</td>
            <td colspan="1" rowspan="1">

Creates an instance of a **PrintDevAttr** XML object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [WriteXml](dcsPrintDevAttrClassWriteXmlMethod.html)
</td>
            <td colspan="1" rowspan="1">

Creates an XML object representing the **PrintDevAttr** object, using writer as its output channel.
</td>
          </tr>
</table>

Public Properties

<br />

<table class="dtTABLE" id="Table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Collate](dcsPrintDevAttrClassCollateProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Output produced by capable printers should be collated when this property is True.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Color](dcsPrintDevAttrClassColorProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Non-monochrome output is to be produced by color-capable printers when this property is True.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Copies](dcsPrintDevAttrClassCopiesProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Count of copies to be produced by the printer.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ DefaultSource](dcsPrintDevAttrClassDefaultSourceProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Standard tray source of paper in the printer. Valid values are defined by the System.Drawing.Printing.PaperSourceKind enumeration
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Duplex](dcsPrintDevAttrClassDuplexProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Standard duplex setting for use by capable printers. Valid values are defined by the System.Drawing.Printing.Duplex enumeration.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ FormName](dcsPrintDevAttrClassFormNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The name of the print format to use, such as "A4", "Letter", "Tabloid", "Ledger", "Envelope", etc. See Also the **Size** property below.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ LeftMargin](dcsPrintDevAttrClassLeftMarginProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Size of left margin in output produced by the printer.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Length](dcsPrintDevAttrClassLengthProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Length of paper in the printer.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [Orientation](dcsPrintDevAttrClassOrientationProperty.html)
</td>
            <td colspan="1" rowspan="1">

Landscape/portrait orientation of paper in the printer. Valid values are defined by the [PaperOrientation](dcsPaperOrientationEnumeration.html) enumeration.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ PrinterName](dcsPrintDevAttrClassPrinterNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The name of an accessible printer device.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Quality](dcsPrintDevAttrClassQualityProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Standard quality rating for output produced by the printer. Valid values are defined by the System.Drawing.Printing.PrinterResolutionKind enumeration.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Scale](dcsPrintDevAttrClassScaleProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The percentage factor by which the printed output is to be scaled. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [Size](dcsPrintDevAttrClassSizeProperty.html)
</td>
            <td colspan="1" rowspan="1">

Standard sheet size of paper in the printer. Valid values are defined by the System.Drawing.Printing.PaperKind Enumeration.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ TopMargin](dcsPrintDevAttrClassTopMarginProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Size of top margin in output produced by the printer.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ TTOption](dcsPrintDevAttrClassTTOptionProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Options for using TrueType fonts in documents output by capable printers. Valid values are defined by the [PrintTrueType](dcsPrintTrueTypeEnumeration.html) enumeration.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="height: 47px">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [Width](dcsPrintDevAttrClassWidthProperty.html)
</td>
            <td colspan="1" rowspan="1" style="height: 47px">

Width of paper in the printer.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ YResolution](dcsPrintDevAttrClassYResolutionProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The y-axis resolution (in dots-per-inch) when printing graphics. 
</td>
          </tr>
</table>

See Also

<dl />
      [PrintDevAttr Class](dcsPrintDevAttrClass.html)
      <br />System.Drawing.Printing.PaperSourceKind 
Enumeration
      <br />System.Drawing.Printing.Duplex 
Enumeration
      <br />[PaperOrientation Enumeration](dcsPaperOrientationEnumeration.html)<br />System.Drawing.Printing.PrinterResolutionKind 
Enumeration
      <br />System.Drawing.Printing.PaperKind 
Enumeration
      <br />[PrintTrueType Enumeration](dcsPrintTrueTypeEnumeration.html)

