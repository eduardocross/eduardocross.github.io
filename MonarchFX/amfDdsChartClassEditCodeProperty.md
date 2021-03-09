---
title: DdsChart.EditCode Property

Id: amfDdsChartClassEditCodeProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 55

keywords: EditCode property
keywords: DdsChart.EditCode property
keywords: chart controls, EditCode

---

Gets or sets a string containing an edit code to punctuate numeric fields according to the standard RPG edit code rules.

#### Syntax
<pre class="prettyprint"> **BegProp EditCode Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String containing an edit code to punctuate numeric fields as noted in the first column of the [Edit Code Table](sharedEditCodeTable.html).

#### Remarks
**EditCode** allows you to punctuate numeric fields, including $ signs, commas, periods, minus sign, and floating minus according to the standard RPG edit code rules. To set this property at design time, click on the right side of the property window and enter a valid edit code as listed in the [Edit Code Table](sharedEditCodeTable.html) that gives you the desired display. For example, entering a **J** in the **EditCode** property will display .00, giving you commas, decimals points, and a minus sign when necessary.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
