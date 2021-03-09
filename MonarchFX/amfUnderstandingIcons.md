---
title: Icon Controls

Id: amfUnderstandingIcons
TocParent: amfASNAMobileSupport
TocOrder: 47

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG Icons
keywords: ASNA Mobile RPG, Hosted Files
keywords: Mobile RPG
keywords: FileHolders

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# Icon Controls

### What is a DdsIcon?
A [DdsIcon](amfDdsIconClass.html) is a simple control used to present an icon from the [Icon ID Collection](amfIconIDCollection.html). These icons provide no interactivity beyond an informational tool tip. If more options are desired, consider using a [DdsButton](amfUnderstandingButtons.html). 

**Applicability:** These controls can be used in Wings, Mobile RPG, and Monarch pages/apps.

### The Mechanics of a DdsIcon.
The <code>IconID</code> property, or the <code>IconIDField</code> and <code>IconIDFieldLength</code> properties control which Icon will be displayed. 
![](Images/DdsIconTasks.png)

### DdsIcon Property Tasks
These are the DdsIcon's significant properties: 

<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637"> <tbody> <tr> <td valign="top" width="169"> <p align="center"> **Property** 
</td>
<td valign="top" width="468">

**Notes** 
</td>
</tr>
			<tr>
            <td colspan="2" valign="top">

**Appearance** 
</td>
			</tr>
			<tr>
<td valign="top" width="169">

<code> **[IconID](amfDdsIconClassIconIDProperty.html)** </code>

</td>
<td valign="top" width="468">

Sets a static IconID from the IconID Collection.

</td>
</tr>
<tr>
<td valign="top" width="169">

<code> **[IconIDField](amfDdsIconClassIconIDFieldProperty.html) &amp; 
[IconIDFieldLength](amfDdsIconClassIconIDFieldLengthProperty.html)** </code>

</td>
<td valign="top" width="468">

These properties define a character field whose runtime value is to be used as the full path to the IFS file. If these properties are set,
the <code> **IconID** </code> property is ignored.

</td>
</tr>
<tr>
<td valign="top" width="169">

<code> **[ToolTip](amfDdsIconClassTextProperty.html)** </code>

</td>
<td valign="top" width="468">

A constant that sets the tool tip text for the control.

</td>
</tr>
<tr>
<td valign="top" width="169">

<code> **[ToolTipField](amfDdsIconClassToolTipFieldProperty.html) &amp; 
[ToolTipFieldLength](amfDdsIconClassToolTipFieldLengthProperty.html)** </code>

</td>
<td valign="top" width="468">

These properties define a character field whose runtime value is to be used as the text for the ToolTip. 
If these properties are set, the **ToolTip**  property is ignored.

</td>
</tr>

	<tr>
            <td colspan="2" valign="top">

**Layout** 
</td>
			</tr>
<tr>
	<td valign="top" width="169">
		<code> **<a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.height(v=vs.110).aspx">Height</a>
		 &amp; 
		 <br /><a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.width(v=vs.110).aspx">Width</a>** 
		 </code>
	</td>
	<td valign="top" width="468">
		These properties set the height and width of the control in whichever unit is specified (pixels, by default).</td>
</tr>

</tbody>
</table>
</p>

