---
title: DdsChart.Series.LegendField Property

Id: amfDdsChartClassSeriesLegendFieldProperty
TocParent: amfDdsChartClassSeries
TocOrder: 30

keywords: Series.LegendField property
keywords: DdsChart.Series.LegendField property

---

Defines the name of a record field used to report the data for the legend.

#### Syntax
<pre class="prettyprint"> **BegProp LegendField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the IFS location of the IBM i CharField that the legend is drawn from. Requires [DdsChart.Series.LegendFieldLength](amfDdsChartClassSeriesLegendFieldLengthProperty.html).

#### Remarks
This sets a CharField in an IBM i record to draw the data for the legend from. It must be used with [Series.LegendFieldLength](amfDdsChartClassValueSeriesLegendLengthProperty.html) in order to avoid throwing an error. This property is very useful if the series legend is likely to be changed or updated frequently, or if it will be used in multiple places throughout the site. Overrides [ASNA.Monarch.WebDspF](amfDdsChartClassSeriesLegendProperty">Legend</a>.

#### Requirements
**Namespace:** <a href="amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
