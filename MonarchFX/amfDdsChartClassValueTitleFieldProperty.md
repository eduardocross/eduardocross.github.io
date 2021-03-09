---
title: DdsChart.ValueTitleField Property

Id: amfDdsChartClassValueTitleFieldProperty
TocParent: amfDdsChartClassPropertiesMain
TocOrder: 140

keywords: ValueTitleField property
keywords: DdsChart.ValueTitleField property

---

Defines the name of a record field used to report the value title (the y-axis on Column and Line Charts).

#### Syntax
<pre class="prettyprint"> **BegProp ValueTitleField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of a record field used to report the value title. Requires [DdsChart.ValueTitleFieldLength](amfDdsChartClassValueTitleFieldLengthProperty.html).

#### Remarks
This sets a Field in a record to draw the text for the value title from. It must be used with [ValueTitleFieldLength](amfDdsChartClassValueTitleFieldLengthProperty.html) in order to avoid throwing an error. This property is very useful if the Value Title is likely to be changed or updated frequently, or if it will be used in multiple places throughout the site or app. Overrides [ASNA.Monarch.WebDspF](amfDdsChartClassValueTitleProperty">ValueTitle</a>.

#### Requirements
**Namespace:** <a href="amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsChart Description](amfUnderstandingCharts.html)<br /> [ DdsChart Class](amfDdsChartClass.html) <br /> [ DdsChart Class Members](amfDdsChartClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
