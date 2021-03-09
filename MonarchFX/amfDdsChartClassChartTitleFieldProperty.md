---
title: DdsChart.ChartTitleField Property

Id: amfDdsChartClassChartTitleFieldProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 20

keywords: ChartTitleField property
keywords: DdsChart.ChartTitleField property

---

Defines the name of a record field used to report the data for the Chart Title.

#### Syntax
<pre class="prettyprint"> **BegProp ChartTitleField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of a field used to report the chart title. Requires [DdsChart.ChartTitleFieldLength](amfDdsChartClassChartTitleFieldLengthProperty.html).

#### Remarks
This sets a CharField in an IBM i record to draw the data for the Chart Title from. It must be used with [ChartTitleFieldLength](amfDdsChartClassChartTitleFieldLengthProperty.html) in order to avoid throwing an error. This property is very useful if the chart title is likely to be changed or updated frequently, or if it will be used in multiple places throughout the site. Overrides [ASNA.Monarch.WebDspF](amfDdsChartTitleProperty">ChartTitle</a>.

#### Requirements
**Namespace:** <a href="amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [DdsChart Class](amfDdsChartClass.html) <br /> [DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
