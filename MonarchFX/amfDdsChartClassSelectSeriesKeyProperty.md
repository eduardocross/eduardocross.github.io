---
title: DdsChart.SelectSeriesKey Property

Id: amfDdsChartClassSelectSeriesKeyProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 115

keywords: SelectSeriesKey property
keywords: DdsChart.SelectSeriesKey property

---

Gets or sets the action to take when a series key on the chart is selected.

#### Syntax
<pre class="prettyprint"> **BegProp SelectSeriesKey Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Defines which keystroke command to pass to the IBM i when a series from the chart is selected. The default is **Unknown** , which results in no particular keypresses. Options include:
- Attn
- Clear
- Enter
- F1- F24
- Help
- Home
- PageDown
- PageUp
- Print
- Reset
- Unknown.

#### Remarks
Sets which key to use when an onscreen series is selected.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
