---
title: Panel Controls

Id: amfUnderstandingPanels
TocParent: amfASNAMobileSupport
TocOrder: 75

keywords: Panel Controls
keywords: Wings Panels
keywords: ASNA Mobile RPG, Panels
keywords: Mobile RPG

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# Panel Controls

### What is a DdsPanel?
A [DdsPanel control](amfDdsPanelClass.html) is used to visually group a set of controls in an area of the screen. 

**Applicability:** These controls can be used in Monarch, Wings, and Mobile RPG pages/apps.

The Property Tasks of a DdsPanel are as follows:
![](Images/DdsPanelTasks.png)

<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637">
			<tbody>
				<tr>
				<td valign="top" width="169">

**Property** 
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
	<td>
   <code> **[GroupingText](amfDdsPanelClassGroupingTextProperty.html)** </code>

</td>
<td valign="top" width="468">

Sets the text to be displayed as a title on the panel.

</td>
</tr>
<tr>
	<td>
   <code> **[GroupingTextField](amfDdsPanelClassGroupingTextFieldProperty.html) &amp;
[GroupingTextFieldLength](amfDdsPanelClassGroupingTextFieldLengthProperty.html)** </code>
</td>
<td valign="top" width="468">

These properties can define a character field whose runtime value is to be used as the title for the panel. If these properties are set,
			the <code>GroupingText</code> property is ignored.

</td>
</tr>
<tr>
            <td colspan="2" valign="top">

**Layout** 
</td>
			</tr>
<tr>
	<td valign="top" width="169">
		<code> **[GroupingTextField](http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.height(v=vs.110).aspx">Height</a>
		 &amp; 
		 <br /><a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.width(v=vs.110).aspx">Width</a>** 
		 </code>
	</td>
	<td valign="top" width="468">
		These properties set the height and width of the control in whichever unit is specified (pixels, by default).</td>
</tr>
</tbody>
</table>

### The Mechanics of a DdsPanel
A panel may define, via the <code> **<a href="amfDdsPanelClassGroupingTextFieldProperty.html)** </code> and <code> **[GroupingTextFieldLength](amfDdsPanelClassGroupingTextFieldLengthProperty.html)** </code> properties, a character field which is included in the record format presented to RPG. It is through this field that a program can set the title of the panel to be presented to the user. 

The other interesting property of a panel (shared with some other controls) is **[<code>VisibleCondition</code>](amfDdsPanelClassVisibleConditionProperty.html).** Setting <code>VisibleCondition</code> allows the developer to provide a logical expression, involving indicators, controlling whether the panel and all of its contained controls is visible and rendered to the user screen. <br/> 

![](Images/DdsPanel.png)
