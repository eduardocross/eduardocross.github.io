---
title: Button Controls

Id: amfUnderstandingButtons
TocParent: amfASNAMobileSupport
TocOrder: 26

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG, Buttons
keywords: ASNA Mobile RPG, Button Controls
keywords: Mobile RPG

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# Button Controls

### What is a DdsButton?
The [DdsButton control](amfDdsButtonClass.html) allows programmers to create and customize the on-screen "buttons" commonly seen in mobile applications and on the web. 

**Applicability:** These controls can be used in Monarch, Wings, and Mobile RPG pages/apps.

### The Mechanics of a DdsButton
The DdsButton control is rendered to the user as a button with text, as a link, or as a clickable image. When the user touches or clicks the button, the screen's data is submitted back to the RPG program. Button properties determine where the 'cursor' was assumed to be at the moment of the submission and which function key is reported to have been activated.

![](Images/DdsButton.png)

**Warning &#8211;** Designers must ensure that the <code>[AidKey](amdDdsButtonClassAidKeyProperty.html)</code> property is also defined in the <code>[FuncKeys](amfDdsRecordClassFuncKeysProperty.html)</code> property of the <code>[DdsRecord](amfDdsRecordClass.html)</code> that contains it. Otherwise the button will not work.

### DdsButton Property Tasks
![](Images/DdsButtonTasks.png)

A button may define, via the <code>TextField</code> and <code>TextFieldLength</code>, a character field which is included in the record format presented to RPG. It is through this field that a program can set the text to be presented to the user. Other interesting properties are: <br/> <br/> 
<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637">
   						 <tbody>
				<tr>
				<td colspan="2" valign="top">

**Appearance** 
</td>
				</tr>
					<tr><td><code>[ButtonStyle](amfDdsButtonClassButtonStyleProperty.html)</code></td>
						<td>It can be one of: <code>Button, Link, Image, Icon</code>.</td></tr>
					<tr><td><code>[IconID](amfDdsButtonClassIconIDProperty.html)</code></td>
						<td>The ID of the Icon that will be displayed. This is often 
						most easily set using the [Icon Selection](amfIconSelection.html) dialogs.</td></tr>
					<tr><td><code>[Image](amfDdsButtonClassImageProperty.html)</code></td>
						<td>The path to the image used as the button. This path points to a location 
						on the Web server file system.</td></tr>
					<tr><td><code>[OnMouseOverImage](amfDdsButtonClassOnMouseOverImageProperty.html)</code></td>
						<td>Path to an image shown when the mouse pointer is over the
						button.</td></tr>
								<tr><td><code>[Text](amfDdsButtonClassTextProperty.html)</code></td>
						<td>Text to be shown in the button. This text is a constant established at design time.</td></tr>
					<tr><td><code>[TextField](amfDdsButtonClassTextFieldProperty.html)</code> &amp; <br /> 
					<code>[TextFieldLength](amfDdsButtonClassTextFieldLengthProperty.html)</code></td>
						<td>These properties define a character field whose runtime value is to be shown on
						the screen. If these properties are given, the <code>Text</code> property is 
						ignored.</td></tr>
						<tr>
				<td colspan="2" valign="top">

**Behavior** 
</td>
				</tr>
					<tr><td><code>[AidKey](amfDdsButtonClassAidKeyProperty.html)</code></td>
						<td>Attention Identifier (Function) Key to report back to RPG, via indicators or through the
						feedback information data structure (INFDS). Also see the warning above.</td></tr>

					<tr><td><code>[FieldName](amfDdsButtonClassFieldNameProperty.html)</code></td>
						<td>The name of the field to be reported back to RPG as having 'focus' when the screen 
						was submitted.</td></tr>

					<tr><td><code>[Protect](amfDdsButtonClassProtectProperty.html)</code></td>
						<td>Sets the 
 *RPG indicator*  expression that when evaluated,
      determines if the field is output-only (read-only).</td></tr>
			</tbody>
</table>

