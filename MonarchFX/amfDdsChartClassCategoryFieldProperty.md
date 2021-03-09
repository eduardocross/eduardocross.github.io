---
title: DdsChart.CategoryField Property

Id: amfDdsChartClassCategoryFieldProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 14

keywords: CategoryField property
keywords: DdsChart.CategoryField property

---

Defines the name of a record field used to report the data for the Category.

#### Syntax
<pre class="prettyprint"> **BegProp CategoryField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of a record field used to report the category data. Requires [DdsChart.CategoryFieldLength](amfDdsChartClassCategoryFieldLengthProperty.html).

#### Remarks
This sets a field in an IBM i record to draw the data for the Category from. It must be used with [CategoryFieldLength](amfDdsChartClassCategoryFieldLengthProperty.html) in order to avoid throwing an error. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
