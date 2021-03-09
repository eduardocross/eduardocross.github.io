---
title: DdsChart Class

Id: amfDdsChartClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 165

keywords: DdsCharField class, about DdsCharField class
keywords: classes [ASNA.Monarch.WebDspF], DdsCharField class

---

**DdsChart** is a container class that defines a chart populated by data from an IBM i Record.

For a list of all members of this type, see [ DdsChart Members](amfDdsChartClassMembers.html).

For a brief explanation of this control in action, see [DdsChart Description](amfUnderstandingCharts.html).

#### Applicable Products:
**Monarch, Wings, Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
 **ASNA.Monarch.WebDspF.DdsChart** </pre>

#### Syntax
<pre class="syntax"> **public class DdsChart** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of **DdsChart** represents an on-screen chart.

The default style for a **DdsChart** is a column chart. Each **DdsChart** is defined by a subfile controller that contains the following elements:
<pre>
Subfile Controller: **ControllerName** 
 **CatgoryTitle**  Field
 **ValueTitle**  Field
 **DataLabels**  Field
 *SeriesX*  **Legend** 
 *SeriesX*  **Color** </pre>

containing a **Category** and a number of **series** which describe the datapoints to be represented.

Each subfile record also contains the following syntax
<pre>Subfile Record **SubfileName** 
 *Series* 1
 *Series* 2
...
 *Series* N</pre>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro
<!-- end -->

#### See Also
<dl>
        <dd>
		[DdsChart Description](amfUnderstandingCharts.html)<br />
		[
        ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>
		[
        DdsChart Members](amfDdsChartClassMembers.html)</dd>
</dl>

