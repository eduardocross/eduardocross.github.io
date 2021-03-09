---
title: DdsChart Series List Editor

Id: amfUnderSeriesList
TocParent: amfUnderstandingCharts
TocOrder: 10

keywords: ASNA Chart Control
keywords: Series Data Storage
keywords: DdsChart Data Storage
keywords: DdsChart Series Dialog
keywords: Series List Editor
keywords: Series Collection Editor

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# DdsChart Series Collection Editor

### Series Collection
That data for each DdsChart is stored in Series, each of which reflects a single DataField on the IBM i. However, the presentation of these data fields is often more complex, as each series has its own properties that control the color and legend name associated with the series. To make these properties easier to work with, the Series Collection Editor (below) is available through the <code>SeriesList</code> property in the Property Tasks or Property Window. 

![](Images/SeriesCollectionEditor.png)
<br/>

The Series Collection Editor has two panes:

- The left pane &#8211; contains a dynamic list of each series included in the chart
- The right pane &#8211; displays the properties of the series currently selected in the left pane.

The left pane has only four buttons associated with it:

- **Add**  &#8211; Adds a new series with a generic name to the bottom of the collection.
- **Remove**  &#8211; Removes the selected series from the collction.
- **Up Arrow**  &#8211; Shifts the selected series up one rank in the collection.
- **Down Arrow**  &#8211; Shifts the selected series down one rank in the collection.

The right pane contains three headings, each with associated properties

- Appearance
					<ul>
					<li>[Color](amfDdsChartClassSeriesColorProperty.html) &#8211; Sets a fixed color for the series.
- [ColorField](amfDdsChartClassSeriesColorFieldProperty.html) &#8211; Sets a field to contain the color for the series.

</li>
				<li>Behavior

- [Legend](amfDdsChartClassSeriesLegendProperty.html) &#8211; Sets a fixed legend name for the series.
- [LegendField](amfDdsChartClassSeriesLegendFieldProperty.html) &#8211; Sets a field to contain the legend name for the series.
- [LegendFieldLength](amfDdsChartClassSeriesLegendFieldLengthProperty.html) &#8211; Sets the length (in characters)
					for the Legend Field of the series.

</li>
				<li>Data

- [DataField](amfDdsChartClassSeriesDataFieldProperty.html) &#8211; Sets a field to contain the data for the series.
- [DataFieldDecimals](amfDdsChartClassSeriesDataFieldDecimalsProperty.html) &#8211; Sets the decimals value for the data field.
- [LegendFieldLength](amfDdsChartClassSeriesDataFieldLengthProperty.html) &#8211; Sets the length (in characters)
					for the DataField of the series.

</li>
			</ul>

Clicking **Okay** will save any changes made to the series collection. Clicking **Close** will close the dialog without saving. 
