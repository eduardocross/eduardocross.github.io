---
title: DdsChart.CategoryTitleField Property

Id: amfDdsChartClassCategoryTitleFieldProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 17

keywords: CategoryTitleField property
keywords: DdsChart.CategoryTitleField property

---

Defines the name of a record field used to report the data for the Category Title (which marks the x-axis on Column and Line Charts).

#### Syntax
<pre class="prettyprint"> **BegProp CategoryTitleField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of a field used to report the data for the category title is drawn. Requires [DdsChart.CategoryTitleFieldLength](amfDdsChartClassCategoryTitleFieldLengthProperty.html).

#### Remarks
This sets a CharField in an IBM i record to draw the data for the Category Title from. It must be used with [CategoryTitleFieldLength](amfDdsChartClassCategoryTitleFieldLengthProperty.html) in order to avoid throwing an error. This property is very useful if the category title is likely to be changed or updated frequently, or if it will be used in multiple places throughout the site. Overrides [ASNA.Monarch.WebDspF](amfDdsCategoryTitleProperty">CategoryTitle</a>.

#### Requirements
**Namespace:** <a href="amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
