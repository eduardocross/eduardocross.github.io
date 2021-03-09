---
title: DdsChart.SelectSeriesField Property

Id: amfDdsChartClassSelectSeriesFieldProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 110

keywords: SelectSeriesField property
keywords: DdsChart.SelectSeriesField property

---

Sets the action to take when a series field on the chart is selected.

#### Syntax
<pre class="prettyprint"> **BegProp SelectSeriesField Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Defines the action to take when one of the chart's series fields is selected. Options include:
- None.
- ShowData.

#### Remarks
Sets action to take when a series field is selected. The ShowData option can be very useful for saving screenspace as it allows users to access precise data without showing it on the screen by default.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
