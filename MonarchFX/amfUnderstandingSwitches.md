---
title: Switch Controls

Id: amfUnderstandingSwitches
TocParent: amfASNAMobileSupport
TocOrder: 80

keywords: ASNA Mobile, Switch control
keywords: ASNA Mobile RPG, Switches
keywords: Swtich control
keywords: Switches

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# Switch Controls

### What is a DdsSwitch?
A [DdsSwitch control](amfDdsSwitchClass.html) is used to create the kind of slider-switches that are common in mobile apps. They can also be employed to create checkboxes. 

![](images/DdsSwitch.png)

**Applicability:** These controls can be used in Monarch, Wings, and Mobile RPG pages/apps.

### The Mechanics of a DdsSwitch
The DdsSwitch has two states, controlled by the ValueOn and ValueOff properties; these two states are definable by the developer. Each switch an be toggled by tapping or clicking on either the switch itself or the label attached to it. 
![](Images/DdsSwitchTasks.png)

### DdsSwitch Property Tasks
<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637"> <tbody><colgroup> <col width="30%" /> <col width="70%" /> </colgroup> <tr><th>Property</th> <th>Description</th> </tr> <tr> <td colspan="2" valign="top"> <p align="center"> **Appearance** 
</td>
			</tr>
			 <tr>
            <td style="height: 31px">
			<code> **[RenderAsCheckBox](amfDdsSwitchClassRenderAsCheckBoxProperty.html)** </code></td>
            <td style="height: 31px">Sets whether the control will be rendered as a classic checkbox or a toggle-switch.</td>
          </tr>	  
		  <tr>
            <td colspan="2" valign="top">

**Behavior** 
</td>
			</tr>
			  <tr><td><code> **[Protect](amfDdsDataFieldClassProtectProperty.html)** </code>
			</td>
			<td>Protects switch from user interaction.</td>
		   </tr>
		 <tr><td><code> **[Usage](amfDdsDataFieldClassUsageProperty.html)** </code>
			</td>
			<td>Sets whether the switch is input-only, input-output, or output only.</td>
		   </tr>
		   <tr>
            <td colspan="2" valign="top">

**External Description** 
</td>
			</tr>

<tr>
            <td><code> **[LabelText](amfDdsSwitchClassLabelTextProperty.html)** </code></td>
            <td>Sets the text for the Switch label.</td>
          </tr>
           <tr>
            <td><code> **[LabelTextField](amfDdsSwitchClassLabelTextFieldProperty.html) &amp; 
            [LabelTextFieldLength](amfDdsSwitchClassLabelTextFieldLengthProperty.html)** </code></td>
            <td>These properties define the name and length of the field that holds the label text.</td>
          </tr>

          <tr>
            <td style="height: 30px">
			<code> **[ValueDefault](amfDdsSwitchClassValueDefaultProperty.html)** </code>
			</td>
            <td style="height: 30px">Sets behavior for when the value is neither
              <code>[ValueOn](amfDdsSwitchClassValueOnProperty.html)</code>            
			nor
          	<code>[ValueOff](amfDdsSwitchClassValueOffProperty.html)</code>. </td>
          </tr>
          <tr>
            <td>
			<code> **[ValueField](amfDdsSwitchClassValueFieldProperty.html) 
			&amp;<br />[ValueFieldLength](amfDdsSwitchClassValueFieldLengthProperty.html)** </code>

            </td>
            <td>These properties define the name and length 
			of the field where the value for the field is held.</td>
          </tr>
		            <tr><td><code> **[ValueOff](amfDdsSwitchClassValueOffProperty.html)** </code>
			</td>
			<td>Sets the value for the '<code>Off</code>' state.</td>
		   </tr>
          <tr>
            <td><code> **[ValueOn](amfDdsSwitchClassValueOnProperty.html)** </code>           </td>
            <td>Sets the value for the '<code>On</code>' state.</td>
          </tr>

		   </tbody>
</table>
           </p>

### DdsSwitch Styles
The appearance of the DdsSwitch (aside from the label) is controlled by the following CSS styles (defined, by default in ~\Themes\Current\Styles\Framework.css): 
<pre>.ToggleSwitchLabel    
   .ToggleSwitchLabelFocus 
   .ToggleSwitch 
   .ToggleSwitch-wrapper &gt; *
   .ToggleSwitch &gt; .ToggleSwitch-wrapper 
   .ToggleSwitch-wrapper &gt; .ToggleSwitch-on 
   .ToggleSwitch-wrapper &gt; .ToggleSwitch-off 
   .ToggleSwitch-wrapper &gt; .ToggleSwitch-handle 
   .ToggleSwitchSwipeRight 
   .ToggleSwitchSwipeLeft 
   .ToggleSwitchCheckbox 
   .ToggleSwitchRenderAsCheckbox 
   .ToggleSwitchRenderAsCheckboxWrapper 
   .ToggleSwitchRenderAsCheckboxCheckbox 
</pre>

If the CSS styles listed above are not available, the switch will not render as intended and the website will not work correctly (a checkbox will still appear). If incorporating a DdsSwitch into a preexisting site (produced prior to version 7.0), these styles can be added by creating a new website and either copying them from the new Framework.css file, or simply copying the new file over the old one. 
