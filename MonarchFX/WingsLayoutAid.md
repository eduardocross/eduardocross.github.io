---
title: Using Wings Layout Aid

Id: WingsLayoutAid
TocParent: amfASNAMobileSupport
TocOrder: 100

keywords: ASNA Wings
keywords: Wings
keywords: Wings Layout Aid
keywords: Layout Aid
keywords: Layout
keywords: Alignment
keywords: Alignment Aid
keywords: Page Layout
keywords: Aligning Elements	

---

<table>
			    <tr>

			       <td> <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span><br />
				   </td>
			    </tr>
</table>

# Using ASNA Wings&#8482; Layout Aid
Introduced in 8.0, the Wings Layout Aid (also applicable to Monarch) allows developers the option of manipulating visible controls directly through a debugging web browser. 
<!-- end of introduction -->

### The Layout Aid
After opening a browser via Visual Studio's Debug option, click the Edit Page link at the bottom of the page. Each DdsRecord will be highlighted with a distinct colored border, and a small icon tray will appear in the upper right.

#### The DdsRecord Blocks
Each DdsRecord is highlighted by a colored border to show which controls it contains. Any number of elements within a record can be selected either by clicking on them individually or by clicking and dragging to select all of the elements in an area. The first "anchor" element is highlighted by a solid dark blue border, and the others by dotted line borders.

![](images/WLAElements.png)

Controls can be moved around inside of the record, and records may be expanded to move controls to areas that are not included. Attempting to select elements that are in seperate records will fail (attempting to rubberband elements in multiple records will cause a pop up warning).

The layout assistant does not allow changes which violate [Wings Validation](awValidation.html).

All of the position changes performed by the Layout Assistant use Absolute Positioning.

#### The Icon Tray
The icon tray contains:
<table class="property table">
					<tr><th>Icon</th><th>Function</th><th>Description</th></tr>
					<tr><td>![](images/WLAHelp.png)</td><td>Help</td><td>Opens this webpage</td></tr>
					<tr><td>![](images/WLADistVertical.png)</td><td>Distribute Vertical</td><td>Arranges all selected elements into an evenly spaced vertical line.</td></tr>
					<tr><td>![](images/WLADistHorizontal.png)</td><td>Distribute Horizontal</td><td>Arranges all selected elements into an evenly spaced horizontal line.</td></tr>
					<tr><td>![](images/WLAEqHeight.png)</td><td>Equalize Height</td><td>Sets the height attribute of all selected elements to a median height.</td></tr>
					<tr><td>![](images/WLAEqWidth.png)</td><td>Equalize Width</td><td>Sets the width attribute of all selected elements to a median height.</td></tr>
					<tr><td>![](images/WLAAlignV.png)</td><td>Align Vertical</td><td>Arranges all selected elements in a vertical array on the center of the anchor element.</td></tr>
					<tr><td>![](images/WLAAlignH.png)</td><td>Align Horizontal</td><td>Arranges all selected elements in a horizontal array on the center of the anchor element.</td></tr>
					<tr><td>![](images/WLAAlignL.png)</td><td>Align Left</td><td>Arranges all selected elements in a vertical array justified by the left border of the anchor element.</td></tr>
					<tr><td>![](images/WLAAlignR.png)</td><td>Align Right</td><td>Arranges all selected elements in a vertical array justified by the right border of the anchor element.</td></tr>
					<tr><td>![](images/WLAAlignB.png)</td><td>Align Bottom</td><td>Arranges all selected elements in a horizontal array justified by the bottom border of the anchor element.</td></tr>
					<tr><td>![](images/WLAAlignT.png)</td><td>Align Top</td><td>Arranges all selected elements in a horizontal array justified by the top border of the anchor element.</td></tr>

					<tr><td>![](images/WLASync.png)</td><td>Sync</td><td>Saves all changes made with the Layout Aid.</td></tr>
					<tr><td>![](images/WLAExit.png)</td><td>Exit</td><td>Exits the Layout Aid. If you have made unsaved changes a dialog will appear asking if you wish to sync them.</td></tr>
</table>

The icon tray can be repositioned along the top and sides of the page by clicking and dragging its edges.

#### Subfiles
When clicking on a subfile a dialog will appear to determine whether an individual record or the entire subfile should be selected. The subfile as a whole can be repositioned or resized as normal.

Subfiles are handled differently from other elements, as are the records that they contain. Subfile records can't be moved or rearranged, but they can be resized by dragging an element outside of its cell. Resizing one cell will cause all other cells to be resized to match. 

#### WingsLayoutAidRsc.ashx
The data for the Wings Layout Aid is stored in a file named WingsLayoutAidRsc.ashx, which is kept in the Developer folder (visible in Visual Studio's Solution Explorer). This folder and its contents should **always** be deleted before deployment.

The following Web.config setting, found in older versions of Monarch, disables the "Saving" of the Layout changes:
<pre class="prettyprint"><code class="html">
  &lt;pages controlRenderingCompatibilityVersion="3.5" clientIDMode="AutoID"/&gt;
 </code></pre>

The WLA assumes "default" naming conventions for "client IDs" (HTML element id attribute). Running in compatibility mode with older ASP.NET versions produces "client IDs" differently, and since WLA needs to find the "server ID" associated with the modified "client IDs" to update the markup, the matching process fails and all layout changes are lost.

There is no need to use such a Web.config setting anymore, so if a developer wishes to use WLA on a very old Monarch Website, the can safely remove the setting, re-run the Website, and WLA will function properly.
