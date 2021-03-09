---
title: DdsChart.DataLabelPosition Property

Id: amfDdsChartClassDataLabelPositionProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 46

keywords: DataLabelPosition property
keywords: DdsChart.DataLabelPosition property
keywords: field controls, DataLabelPosition

---

Gets or sets the position of the data label on the chart (numbering of each data point).

#### Syntax
<pre class="prettyprint"> **BegProp DataLabelPosition Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Possible values include:
- Above
- Below
- Center
- None

Defaults to **None** .

#### Remarks
Sets the position of the data label on each data point. Use with care for chart styles other than Column or Bar. Useful for matching site style or maximizing readability.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
