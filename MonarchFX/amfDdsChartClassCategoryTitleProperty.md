---
title: DdsChart.CategoryTitle Property

Id: amfDdsChartClassCategoryTitleProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 16

keywords: CategoryTitle property
keywords: DdsChart.CategoryTitle property

---

Gets or sets the category title of the chart. This populates the on-screen category field (the x-axis on Column and Line Charts).

#### Syntax
<pre class="prettyprint"> **BegProp CategoryTitle Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. This value defines the category title for the chart. 

#### Remarks
Sets the category title field for the chart to a fixed string. This is best used if the category title is unique and unlikely to be used in other charts. This is overridden by [CategoryTitleField](amfDdsChartClassCategoryTitleFieldProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
