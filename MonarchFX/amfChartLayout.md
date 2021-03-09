---
title: Laying Out a Chart

Id: amfChartLayout
TocParent: amfUnderstandingCharts
TocOrder: 10

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG, Chart Layout
keywords: ASNA Mobile RPG, Charts
keywords: Mobile RPG
keywords: Charts

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0
				   </span></td>
			    </tr>
</table>

# Laying Out a Chart
In the process of displaying a chart to a user, the data on the subfile goes through two major steps:
1. Chart Generation
2. Chart Rendering

### Chart Generation
Generating a chart involves creating the instructions (as a vector graphic) to draw the chart regardless of the device where it will be displayed. These instructions are made relative to a 'canvas'. Determining the location and size of each of the elements that will make up the final display requires determining the shape of the 'canvas'. It is also necessary to determine how much space within the canvas will be allocated to each element.

#### Generation Aspect Ratio
The chart control's canvas is a rectangle whose width and height proportion default to the wide screen aspect ratio of 16:9. This ratio can be controlled by the property <code>[GenerationAspectRatio](amfDdsChartClassGenerationAspectRatioProperty.html)</code>. For instance, a chart may look better when displayed as a square, in that case it should be generated in an even ratio, say of 16:16. On the other hand, a chart may look better when displayed in a 'portrait' layout, so a ratio of 9:16 may be a better fit.

#### Element Allocation
There can be up to seven element types that comprise a chart: 

3. Chart Title
4. Value Title
5. Category Title
6. Category Labels
7. Legend
8. The Data Graph

The position of each element in the chart depends on the chart type and the value of <code>LegendPosition</code>. Elements are placed on a horizontal or vertical direction. The following table describes the properties that control the size of the significant dimension (<code>Width</code> or <code>Height</code>).

<table border="1" cellpadding="0" cellspacing="0" style="width: 508.7pt; mso-border-alt: solid windowtext .5pt; mso-yfti-tbllook: 1184; mso-padding-alt: 0in 5.4pt 0in 5.4pt" width="678"> <tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;page-break-inside:avoid"> <td rowspan="2" style="width: 66.6pt; border: solid windowtext 1.0pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt" valign="top" width="89"> <p> <span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">Element</span>
</td>
							<td rowspan="2" style="width: 103.6pt; border: solid windowtext 1.0pt; border-left: none; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt" valign="top" width="138">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">Property</span>
</td>
							<td style="border-right: 1.0pt solid windowtext; border-top: 1.0pt solid windowtext; border-bottom: 1.0pt solid windowtext; width: 89pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium;" valign="top">
														</td>
							<td colspan="4" style="width: 249.3pt; border: solid windowtext 1.0pt; border-left: none; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt" valign="top" width="332">

<span style="font-size:9.0pt; mso-bidi-font-size:11.0pt;color:white;mso-themecolor:background1">Defaults</span>
</td>
						</tr>
						<tr style="mso-yfti-irow:1">
							<td style="width: 89pt; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">Chart Type →</span>
</td>
							<td style="width: 92pt; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">Column</span>
</td>
							<td style="width: 76.05pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt" valign="top" width="101">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">Bar</span>
</td>
							<td style="width: 89pt; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">Line</span>
</td>
							<td style="width: 47.3pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt" valign="top" width="63">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">Pie</span>
</td>
						</tr>
						<tr style="mso-yfti-irow:2">
							<td style="width:66.6pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt" valign="top" width="89">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt"> Chart Title </span>
</td>
							<td style="width:103.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="138">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt">[ChartTitleFontSize](amfDdsChartClassChartTitleFontSizeProperty.html)</span>
</td>
							<td rowspan="5" style="width:89pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top" />
													<td colspan="4" style="width:249.3pt;border-top:none;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="332">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt;mso-bidi-font-size:11.0pt"> Font Size (H)</span></b>
</td>
						</tr>
						<tr style="mso-yfti-irow:3">
							<td style="width:66.6pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt" valign="top" width="89">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt"> Value Title</span>
</td>
							<td style="width:103.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="138">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt">[AxisTitleFontSize](amfDdsChartClassAxisTitleFontSizeProperty.html)</span>
</td>
							<td style="width:92pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (W)</span></b>
</td>
							<td style="width:76.05pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="101">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (H)</span></b>
</td>
							<td style="width:89pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (W)</span></b>
</td>
							<td style="width:47.3pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="63">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">N/A</span></b>
</td>
						</tr>
						<tr style="mso-yfti-irow:4">
							<td style="width:66.6pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt" valign="top" width="89">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt"> Value Labels</span>
</td>
							<td style="width:103.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="138">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">[ValueLabelsSize](amfDdsChartClassValueLabelSizeProperty.html)</span></b><span style="font-size: 9.0pt;mso-bidi-font-size:11.0pt">*<b style="mso-bidi-font-weight:normal"></b></span>
</td>
							<td style="width:92pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">12.5% (W)</span></b>
</td>
							<td style="width:76.05pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="101">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (H)</span></b>
</td>
							<td style="width:89pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">12.5% (W)</span></b>
</td>
							<td style="width:47.3pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="63">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">N/A</span></b>
</td>
						</tr>
						<tr style="mso-yfti-irow:5">
							<td style="width:66.6pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt" valign="top" width="89">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt"> Category Title</span>
</td>
							<td style="width:103.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="138">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt">[AxisTitleFontSize](amfDdsChartClassAxisTitleFontSizeProperty.html)</span>
</td>
							<td style="width:92pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (H)</span></b>
</td>
							<td style="width:76.05pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="101">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (W)</span></b>
</td>
							<td style="width:89pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (H)</span></b>
</td>
							<td style="width:47.3pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="63">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">N/A</span></b>
</td>
						</tr>
						<tr style="mso-yfti-irow:6">
							<td style="border-left: 1.0pt solid windowtext; border-right: 1.0pt solid windowtext; border-bottom: 1.0pt solid windowtext; width:66.6pt; mso-border-top-alt:solid windowtext .5pt; mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt; height: 55px; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top" width="89">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt"> Category Labels</span>
</td>
							<td style="width:103.6pt;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; height: 55px; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top" width="138">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">[CategoryLabelsSize](amfDdsChartClassCategoryLabelSizeProperty.html)</span></b><span style="font-size:9.0pt;mso-bidi-font-size:11.0pt">*<b style="mso-bidi-font-weight: normal"></b></span>
</td>
							<td style="width:92pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; height: 55px; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (H)</span></b>
</td>
							<td style="width:76.05pt;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; height: 55px; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top" width="101">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">12.5% (W)</span></b>
</td>
							<td style="width:89pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; height: 55px; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (H)</span></b>
</td>
							<td style="width:47.3pt;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; height: 55px; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top" width="63">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">N/A</span></b>
</td>
						</tr>
						<tr style="mso-yfti-irow:7">
							<td colspan="2" style="width:66.6pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt" valign="top" width="89" />

							<td style="width: 89pt; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">LegendPosition↓</span>
</td>
							<td colspan="4" style="border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;">
														</td>

						</tr>
						<tr style="mso-yfti-irow:8">
							<td rowspan="2" style="width:66.6pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt" valign="top" width="89">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt"> Legend</span>
</td>
							<td rowspan="2" style="width:103.6pt;border-top:none;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" >

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">[LegendSize](amfDdsChartClassLegendSizeProperty.html)</span></b><span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">*<b style="mso-bidi-font-weight:normal"> </b></span>
</td>
							<td style="width: 89pt; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">Left or Right</span>
</td>
							<td colspan="4" style="width:249.3pt;border-top:none;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="332">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">25% (W)</span></b>
</td>
						</tr>
						<tr style="mso-yfti-irow:9">
							<td style="width: 89pt; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #4F81BD; mso-background-themecolor: accent1; padding: 0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt;color:white; mso-themecolor:background1">Top or Bottom</span>
</td>
							<td colspan="4" style="width:249.3pt;border-top:none;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="332">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Font Size (H)</span></b>
</td>
						</tr>
						<tr style="mso-yfti-irow:10;mso-yfti-lastrow:yes">
							<td style="width:66.6pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt" valign="top" width="89">

<span style="font-size:9.0pt;mso-bidi-font-size:11.0pt"> The Data Graph</span>
</td>
							<td style="width:103.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="138">
														</td>
							<td style="width:89pt; border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt; border-left-style: none; border-left-color: inherit; border-left-width: medium; border-top-style: none; border-top-color: inherit; border-top-width: medium;" valign="top">
														</td>
							<td colspan="4" style="width:249.3pt;border-top:none;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt" valign="top" width="332">

<b style="mso-bidi-font-weight:normal"> <span style="font-size:9.0pt; mso-bidi-font-size:11.0pt">Fills whatever space is left over from the other elements</span></b>
</td>
						</tr>
</table>
					</p>

**Value can be set as a percent or fixed unit. The Canvas has a height of 200 units.* 

### Chart Rendering
When the device is rendering the chart, it will stretch/shrink the chart to fit into the dimension of the control defined by the [Width](amfDdsChartClassWidthProperty.html) and [Height](amfDdsChartClassHeightProperty.html) properties. If only one of the dimensions is given, the other one will be computed to maintain the proportion stated in the [GenerationAspectRatio](amfDdsChartClassGenerationAspectRatioProperty.html) property.
