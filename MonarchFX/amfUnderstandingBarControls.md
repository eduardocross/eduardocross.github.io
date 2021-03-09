---
title: Bar Controls

Id: amfUnderstandingBarControls
TocParent: amfASNAMobileSupport
TocOrder: 23

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG, Bar controls
keywords: ASNA Mobile RPG, bars
keywords: Mobile bar

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0
				   </span></td>
			    </tr>
</table>

# Bar Controls

### What is a DdsBar?
Mobile RPG includes the [DdsBar control](amfDdsBarClass.html) which allows users to create and customize the on-screen bars commonly seen in mobile applications. DdsBars have their positioning on the screen determined by the DdsRecord properties <code>[NavigationBarControlID](amfDdsRecordClassNavigationBarControlIDProperty.html)</code> and <code>[FooterBarControlID](amfDdsRecordClassNavigationBarControlIDProperty.html)</code>. Navigation Bars are locked to the top of the screen, Footer bars to the bottom.

**Applicability:** These controls can be used exclusively in Mobile RPG pages/apps.
<br />
			![](Images/DdsBarTasks.png)

#### DdsBar Property Task
<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637">
   						 <tbody>
							 <tr>
           						 <td valign="top" align="center" style="width: 117px">
 **Property** 
								</td>
								<td valign="top" style="width: 468px" align="center">
 **Notes** 
								</td>
							</tr>
							<tr><td><code> **[DdsBarSegments](amfDdsBarClassSegmentsProperty">Segments</a>** </code></td>
								<td>Contains the IDs of each BarSegment the Bar will contain.</td>
							</tr>
						</tbody>
</table>

#### DdsBarSegment Property Task
<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637">
   					<tbody>

							 <tr>
           						 <td valign="top" align="center" style="width: 117px">
 **Property** 
								</td>
								<td valign="top" style="width: 468px" align="center">
 **Notes** 
								</td>
							</tr>
						<tr><td><code> **<a href="amfDdsBarSegmentClassAlignmentProperty">Alignment</a>** </code></td>
							<td>Sets whether the contents of the segment will be aligned left, right, or center (defaults to center).</td>
						</tr>
					</tbody>
</table>

### The Mechanics of a DdsBar
Bars themselves can only contain one type of element: <a href="amfDdsBarSegmentClass.html). Each DdsBarSegment included in the bar has an ID property that is used as a value in the DdsBar's Segments property. The order of the IDs determines the order that the items will appear onscreen.

DdsBarSegments can be manipulated through the dedicated [DdsBarSegment Collection Editor](amfUnderSegmentsList.html) dialog. This dialog is accessed by clicking the question mark (?) button on the DdsBar Tasks window.

BarSegment objects define the layout of navigation or footer bars. The bar will be evenly divided into horizontal sections defined by the BarSegments; a bar can contain any number of BarSegments, although any more than four may become difficult to use on most smartphones. Common layouts include one segment (for just a title, copyright notice, or search bar), two segments (for a search bar and navigation buttons), or three segments (for a search bar, title, and navigation buttons). Using empty segments might be necessary to get an ideally formatted bar.

Each BarSegment can contain fields or buttons, and has an <code>Alignment</code> property that can be set to Left, Right, or Center to align its contents with the edges or center of the segment. 

For example, the bar shown below is divided into three segments: The first segment is aligned left; it contains a single DdsButton showing text drawn from a field. The second segment aligns its contents to the center; it holds the DdsConstant <code>'Job Detail'</code>. Finally the third segment aligns its contents to the right; it contains two DdsButtons with images pointing left and right. 

![](Images/DdsBar.jpg)
