---
title: DdsChart.XAxisLabelRotation Property

Id: amfDdsChartClassXAxisLabelRotationProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 160

keywords: XAxisLabelRotation property
keywords: DdsChart.XAxisLabelRotation property

---

Sets the rotation (in degrees) of the label text for the x axis.

#### Syntax
<pre class="prettyprint"> **BegProp XAxisLabelRotation Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. This property can take any value between 90 and -90. 

#### Remarks
Sets the rotation (in degrees) of the text shown on the chart's x-axis. This is very useful for styling the chart and for tweaking the chart's spacing.<br /><br /> Negative values will cause the text to rotate counterclockwise, while positive values will cause the text to rotate clockwise. A value of either 90 or -90 will result in the text being vertical; with 90 facing straight down and -90 facing up.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
