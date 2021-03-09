---
title: DdsBarSegment Collection Editor

Id: amfUnderSegmentsList
TocParent: amfUnderstandingBarControls
TocOrder: 10

keywords: ASNA Bar Control
keywords: BarSegment
keywords: DdsBarSegment
keywords: DdsBar Segments Dialog
keywords: Segments List Editor
keywords: Segments Collection Editor
keywords: DdsBarSegments Collection Editor

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0
				   </span></td>
			    </tr>
</table>

# DdsBar Segment Collection Editor

### Segments Collection
That data for each DdsBar is stored in segments, each of which has properties of its own. To make these properties easier to work with, the Segments Collection Editor (below) is available through the <code>Segments</code> property in the Property Tasks or Property Window. 

![](Images/DdsBarSegmentEditor.png)
<br/>

The DdsBarSegment Collection Editor has two panes:

- The left pane &#8211; contains a dynamic list of each segment included in the chart
- The right pane &#8211; displays the properties of the segment currently selected in the left pane.

The left pane has only four buttons associated with it:

- **Add**  &#8211; Adds a new segment with a generic name to the bottom of the collection.
- **Remove**  &#8211; Removes the selected segment from the collection.
- **Up Arrow**  &#8211; Shifts the selected segment up one rank in the collection.
- **Down Arrow**  &#8211; Shifts the selected segment down one rank in the collection.

The right pane contains two headings, each with associated properties

- Behavior
					<ul>
					<li>[Alignment](amfDdsBarSegmentClassAlignmentProperty.html) &#8211; Sets the alignment for contents of the BarSegment.
- <a href="https://msdn.microsoft.com/en-us/library/system.web.ui.control.validaterequestmode(v=vs.110).aspx">ValidateRequestMode</a> 
					&#8211; Indicates whether the control checks client input from the browser.

</li>
				<li>Misc

- <a href="https://msdn.microsoft.com/en-us/library/system.web.ui.control.validaterequestmode(v=vs.110).aspx">(ID)</a> 
					&#8211; Programattic ID for the segment.

</li>
			</ul>

Clicking **Okay** will save any changes made to the segment collection. Clicking **Close** will close the dialog without saving. 
