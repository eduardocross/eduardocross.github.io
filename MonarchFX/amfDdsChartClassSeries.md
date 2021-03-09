---
title: DdsChart.Series Class

Id: amfDdsChartClassSeries
TocParent: amfDdsChartClassSeriesListProperty
TocOrder: 05

keywords: DdsCharField class, about DdsCharField class
keywords: classes [ASNA.Monarch.WebDspF], DdsCharField class

---

**Series** define the actual groups of data that make up a Chart.

For a list of all members of this type, see [ DdsSeries Members](amfDdsChartClassMembers.html).
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
    [ASNA.Monarch.WebDspF.DdsChart](amfDdsDataFieldClass.html)
 **ASNA.Monarch.WebDspF.DdsChart.Series** </pre>

#### Syntax
<pre class="syntax"> **public class DdsChart.Series** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of **DdsChart.Series** provides a set of data defined by the Subfile property, that helps populate the DdsChart control.

Each Series has the following properties:
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Property</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->
             <tr>
            <td style="height: 31px"><img alt="public property" src="../Images/property.bmp" />[
              Color](amfDdsChartClassSeriesColorProperty.html)</td>
            <td style="height: 31px">Gets or sets the color associated with the 
			series.</td>
          </tr>

             <tr>
            <td style="height: 31px"><img alt="public property" src="../Images/property.bmp" />[
             ColorField](amfDdsChartClassSeriesColorFieldProperty.html)</td>
            <td style="height: 31px">Gets or sets the IFS field from which the 
			data for the color will be drawn.</td>
          </tr>
              <tr>
            <td style="height: 31px"><img alt="public property" src="../Images/property.bmp" />[
              D<span class="auto-style1">ataField</span>](amfDdsChartClassSeriesDataFieldProperty.html)</td>
            <td style="height: 31px">Gets or sets the IFS field from which the 
			data for the series will be drawn.</td>
          </tr>
            <tr>
            <td style="height: 31px"><img alt="public property" src="../Images/property.bmp" />[
              D<span class="auto-style1">ecimals</span>](amfDdsChartClassSeriesDecimalsProperty.html)</td>
            <td style="height: 31px">Gets or sets the number of decimal places 
			to use (must be exact)</td>
          </tr>
                       <tr>
            <td style="height: 31px"><img alt="public property" src="../Images/property.bmp" />[
              Legend](amfDdsChartClassSeriesLegendProperty.html)</td>
            <td style="height: 31px">Gets or sets the text used to describe this 
			series in the legend.</td>
          </tr>

            <tr>
            <td style="height: 31px"><img alt="public property" src="../Images/property.bmp" />[
             LegendField](amfDdsChartClassSeriesLegendFieldProperty.html)</td>
            <td style="height: 31px">Gets or sets the IFS field from which the 
			Legend data will be drawn.</td>
          </tr>
               <tr>
            <td style="height: 31px"><img alt="public property" src="../Images/property.bmp" />[ 
			LegendFieldLength](amfDdsChartClassSeriesLegendFieldLengthProperty.html)</td>
            <td style="height: 31px">Gets or sets the length of IFS legend 
			field.</td>
          </tr>
            <tr>
            <td style="height: 31px"><img alt="public property" src="../Images/property.bmp" />[
              Length](amfDdsChartClassSeriesLengthProperty.html)</td>
            <td style="height: 31px">Gets or sets the length (in pixels) of the data field.</td>
          </tr>
</table>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl>
        <dd>
        [DdsChart Description](amfUnderstandingCharts.html)<br />
        [DdsChart Class](amfDdsChartClass.html)<br />
		[
        ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>
		[
        DdsChart Members](amfDdsChartClassMembers.html)</dd>
</dl>

