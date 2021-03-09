---
title: DdsChart.ChartType Property

Id: amfDdsChartClassChartTypeProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 31

keywords: ChartType property
keywords: DdsChart.ChartType property

---

Gets or sets the type of chart to display.

#### Syntax
<pre class="prettyprint"> **BegProp ChartType Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Sets the type of the chart. Defaults to **Column** .
- **Bar**  - Presents series as 
		   groups of horizontal bars.
- **Column**  &#8211; (Default) Presents series as groups 
	   of vertical columns.
- **Data**  &#8211; Presents the raw data.
- **Line**  - Presents series as points 
	   joined by lines.
- **Pie**  - Presents a single series as portions of 
	   a pie chart.

#### Remarks
Sets the type of the chart to be displayed on the mobile screen.

Note that the **pie** chart only displays the first series indicated; any other series will be ignored. Selecting the **pie** enumeration also causes the Series.Color property to behave differently; applying gradients of the chosen color. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
