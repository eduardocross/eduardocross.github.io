---
title: DdsChart.AxisLabelFontStyle Property

Id: amfDdsChartClassAxisLabelFontStyleProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 04

keywords: AxisLabelFontStyle property
keywords: DdsChart.AxisLabelFontStyle property

---

Gets or sets the font style for the chart's axis labels (the numbering on each axis).

#### Syntax
<pre class="prettyprint"> **BegProp AxisLabelFontStyle Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Defines the font style of the axis title. It can take any of the following values:

- **Bold**
- *Italic*
- Regular
- <strike>Strikeout</strike>
- <u>Underline</u>

Defaults to **Regular** .

#### Remarks
Sets the axis labels' font style. It may be desirable to match it with the font styles used in the AxisTitle, ChartTitle, et'c.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ Derived Classes](amfDdsChartDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
